# External API Integration Patterns — Framework Rules

> **Severity:** MUST | **Applies to:** @architect, @dev, @data-engineer, @devops

## Core Principle: SYNC > CACHE > REAL-TIME

Every integration with an external API in dashboards, reports or query interfaces must follow this decision hierarchy:

### SYNC (default for dashboards)
- Data synced periodically to local DB
- Frontend queries DB only — **zero external API calls on user access**
- Sync runs in background via cron/scheduler with its own rate limit
- **When to use:** Dashboards, reports, analytics, listings, kanban

### CACHE (when real-time is needed but data changes infrequently)
- Cache in DB (not in memory) — survives restarts
- TTL proportional to data change frequency
- **When to use:** Data that changes a few times per hour and needs to be "near real-time"

### REAL-TIME (exception, requires justification)
- Direct call to external API at time of access
- **Only for:** User actions (create invoice, send payment, incoming webhook)
- **Never for:** Listings, reports, dashboards, filters

---

## Decision Matrix

| Scenario | Pattern | Rate Limit Risk | Latency |
|---------|--------|----------------|----------|
| Financial dashboard | SYNC → DB | None | <100ms |
| Monthly report | SYNC → DB | None | <100ms |
| Invoice kanban | SYNC → DB | None | <100ms |
| Create new invoice | REAL-TIME | Low (1 call) | 1-3s |
| Payment webhook | REAL-TIME (incoming) | None | Async |
| Search customer by ID | CACHE → DB | None | <50ms |
| Filter/period change | DB QUERY | None | <100ms |

---

## Anti-Patterns (PROHIBITED)

### 1. Real-Time Dashboard
```
BAD:  User opens page → External API (hundreds of calls)
GOOD: User opens page → query local DB (1 query)
```

### 2. Force Refresh on Filter
```
BAD:  Change period filter → bypass cache → External API
GOOD: Change filter → new DB query (same data, different WHERE)
```

### 3. In-Memory Cache for Critical Data
```
BAD:  const cache = new Map() → lost on PM2 restart
GOOD: Data in PostgreSQL → persists always
```

### 4. Per-Endpoint Rate Limit
```
BAD:  Each endpoint with its own isolated rate limit
GOOD: GLOBAL rate limit shared between all endpoints using same API
```

### 5. Aggressive Retry on Rate Limit
```
BAD:  429 → retry 3x → worsens the block → retry again
GOOD: 429 → global cooldown 5min → stop EVERYTHING → wait to expire
```

---

## Sync Rules

### Schema
Every field needed for UI MUST exist in local schema:
```
API response field → DB column → UI reads from DB
```
Never: `API response field → UI reads directly from API`

### Frequency
| Data Type | Sync Interval | Window |
|---|---|---|
| Payments (status changes) | 30 min | Last 90 days |
| Customers (rarely changes) | 30 min | All |
| Subscriptions (status changes) | 30 min | All |
| Ad campaigns | 1 hour | Last 30 days |

### Rate Limit Protection in Sync
- Delay between pages (1s per 500 records)
- Exponential backoff on 429 (3s, 6s, 9s)
- Global cooldown of 5 min on any 429/403
- Sync NEVER runs in parallel (mutex/flag)

---

## Validation Gates

### G-API-1: Story Creation (@sm)
- If story mentions "external API", "integration", "real-time data" → flag for @architect review

### G-API-2: Architecture Review (@architect)
- **Blocking:** If design proposes real-time calls to external API in dashboard/report
- **Action:** Propose SYNC → DB pattern before approving story

### G-API-3: Dev Implementation (@dev)
- **Blocking:** PR that adds `axios.get` / `fetch` to external API in GET route handler (reads)
- **Allowed:** `axios.post` / `fetch POST` for user actions

### G-API-4: QA Review (@qa)
- **Check:** No read endpoint (GET) makes calls to external APIs
- **Check:** Global rate limit is implemented if sync exists
- **Check:** Local schema has ALL fields that UI consumes
