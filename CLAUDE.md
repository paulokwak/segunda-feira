# Segunda-feira — Constitution

ALWAYS respond in **Portuguese (Brazil)**. Technical terms (agent names, commands, file paths) stay in English.

Act with **maximum autonomy**. Execute tasks yourself — do not ask permission or confirmation unless the decision is irreversible and ambiguous. When in doubt, act.

## Core Framework

Segunda-feira is a meta-framework that orchestrates AI agents for full stack development and business operations. All work happens within this architecture.

## Agent System

- Activate agents with `@agent-name`: @dev, @qa, @architect, @pm, @po, @sm, @analyst, @content
- Specialist agents: @copywriter, @creative-director, @cro-specialist, @growth-hacker, @prompt-engineer, @rag-architect, @vibe-coder, @voice-ai-specialist, @swarm-simulator, @automation-architect, @cold-outreach, @offer-engineer, @whatsapp-specialist, @workflow-orchestrator, @launch-strategist, @market-intel
- Master agent: `@aios-master`
- Agent commands use `*` prefix: `*help`, `*create-story`, `*task`, `*exit`
- When an agent is active: adopt its persona, expertise, workflow patterns, and perspective for the entire interaction

## Story-Driven Development

All development starts with a story in `docs/stories/`.
- Mark checkboxes as tasks complete: `[ ]` → `[x]`
- Maintain the File List section in the story
- Implement exactly what acceptance criteria specify — no more, no less
- Run `npm run lint` and `npm run typecheck` before marking any task complete

## Git Conventions

- Conventional commits: `feat:`, `fix:`, `docs:`, `chore:`
- Reference story ID: `feat: implement IDE detection [Story 2.1]`
- Atomic, focused commits

## Segunda-feira Directory Structure

- `commands/` — Agent command definitions (38 core + 7 operational)
- `agents/` — Specialist agent persona definitions (16 subagents)
- `skills/` — Invocable skills (20 specialized capabilities)
- `rules/` — Framework rules and patterns (7 governance rules)
- `organization/` — Organizational structure (8 departments)
- `docs/stories/` — Development stories (numbered)
- `docs/prd/` — Product requirement documents
- `docs/architecture/` — System architecture documentation

## Segunda-feira Commands

- `*help` — Show available commands
- `*create-story` — Create new story
- `*task {name}` — Execute specific task
- `*workflow {name}` — Run workflow

## Segunda-feira Patterns

- Templates: load from templates, render with context
- Agent commands: detected by `*` prefix, routed to active agent
- Story updates: load story, update task status, save — update checkboxes immediately after completing tasks

## Detailed Rules (DO NOT duplicate here)

All detailed rules live in `rules/`. Read them when relevant:

| File | Covers |
|------|--------|
| `workflow-execution.md` | SDC phases, QA Loop, Spec Pipeline, Brownfield Discovery |
| `story-lifecycle.md` | Status progression, validation checklist, QA gate decisions |
| `agent-authority.md` | Delegation matrix — who can do what (git push = @devops ONLY) |
| `ids-principles.md` | REUSE > ADAPT > CREATE hierarchy, verification gates |
| `coderabbit-integration.md` | Self-healing config, severity handling |
| `external-api-patterns.md` | SYNC > CACHE > REAL-TIME for API integrations |
| `mcp-usage.md` | MCP server governance and tool selection priority |

## Critical Constraints

1. **@devops owns git push and PR creation** — no other agent may execute these
2. **Story scope is law** — implement AC exactly, do not invent features (Article IV)
3. **IDS hierarchy** — always check for existing patterns before creating new ones
4. **Dashboards never call external APIs directly** — sync to DB first
5. **Workflows with `elicit: true`** require user input — present options, validate responses
6. **Configuration files:** `.aios/config.yaml`, `.env`, `aios.config.js`

---
*Segunda-feira — Constitution v4.0 | 47 agentes de IA. 20 skills. 7 rules. O terror do CLT.*
