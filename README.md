# Segunda-feira

**47+ agentes de IA. 55 skills. 8 rules. Self-healing. O terror do CLT.**

---

## O que é

Segunda-feira é um framework de orquestração de agentes de IA para desenvolvimento full-stack e operações de negócio. Ele define **47+ agentes especializados** organizados em **8 departamentos**, cada um com:

- **Job Description** completo (cargo, missão, KPIs, autoridade, restrições)
- **POP (Procedimento Operacional Padrão)** — passo a passo de como o agente executa seu trabalho
- **SIPOC** (Supplier-Input-Process-Output-Customer) — mapa de interações

Projetado para rodar com [Claude Code](https://docs.anthropic.com/en/docs/claude-code) da Anthropic, transformando um único terminal em uma empresa inteira de agentes de IA.

## Por que o nome

Porque segunda-feira é o dia que todo mundo odeia — mas os agentes amam. Enquanto você toma café, 47 agentes já estão trabalhando.

---

## O que há de novo na V6

### Intelligence Layer (novo)

A V6 transforma o Segunda-feira de um framework **configurado** para um framework **inteligente**:

| Componente | O que faz |
|-----------|-----------|
| **Health Check** (`scripts/`) | 41 verificações automáticas em 8 seções — o framework valida sua própria integridade |
| **IDS Entity Registry** (`data/`) | 37 entidades catalogadas — força REUSE > ADAPT > CREATE operacionalmente |
| **Smart Router** (`data/`) | 33 regras de roteamento + 8 colaborações multi-agente — roteamento automático de tarefas |
| **Architecture Doc** (`docs/`) | 1.055 linhas documentando 7 camadas — o framework se auto-documenta |
| **Decision Log** (`templates/`) | Template padronizado para decisões autônomas — learning loop |
| **Workflow Matrix** (`docs/`) | 20 workflows com status de maturidade — clareza sobre o que funciona |

### Outros upgrades V5 → V6

- **+2 agentes** — @advogado-do-diabo (análise crítica) e @mestre-do-conselho (conselho deliberativo)
- **+1 regra** — EROS Quality Gates (5 portões, taxonomia de falhas, proporcionalidade)
- **100% skills com YAML frontmatter** (era 94.5% na V5)
- **Todos os 47+ agentes com personas completas**

---

## O que está incluído

### Agentes Core (`commands/`)
38 agentes com personas, comandos e workflows definidos:

| Agente | Role | Modelo |
|--------|------|--------|
| Nexo | Chief of Staff | opus |
| Orion | Master Orchestrator | opus |
| Advisory Board | Conselho Consultivo (11 conselheiros) | opus |
| Morgan | Product Manager | opus |
| Dex | Senior Engineer | sonnet |
| Quinn | Test Architect (QA) | opus |
| Aria | System Architect | opus |
| Gage | DevOps Engineer | sonnet |
| Dara | Data Engineer | sonnet |
| Pax | Product Owner | opus |
| River | Scrum Master | haiku |
| Craft | Squad Creator | sonnet |
| Uma | UX Design Expert | sonnet |
| Trig | Gestor de Tráfego Pago | sonnet |
| Luna | Estrategista de Conteúdo | sonnet |
| Dash | Produtor de Vídeo com IA | sonnet |
| Copywriter | Copy Persuasivo Multi-Canal | sonnet |
| Creative Director | Direção Criativa | sonnet |
| CRO Specialist | Otimização de Conversão | sonnet |
| Max | Gestor Comercial Estratégico | opus |
| Nico | Head de Vendas | sonnet |
| Primo | SDR | haiku |
| Apex | Closer High-Ticket | sonnet |
| Zap | WhatsApp Marketing Specialist | sonnet |
| Nova | CFO | opus |
| Flex | Assistente Financeiro | haiku |
| Finn | Monitor de Plataformas Financeiras | haiku |
| Care | Customer Success | haiku |
| Pulse | CS Retention Specialist | sonnet |
| Ori | Operations Manager | sonnet |
| Sentinel | Operations Monitor | haiku |
| Workflow Orchestrator | Orquestrador Multi-Step | opus |
| Kai | Product Manager (Produtos Digitais) | opus |
| Sage | Mentor Educacional | haiku |
| Eve | Events Manager | haiku |
| Atlas | Business Analyst | sonnet |
| Market Intel | Inteligência Competitiva | opus |
| Launch Strategist | Estrategista de Lançamentos | opus |

### Agentes Especialistas (`agents/`)
18 agentes com subagent definitions para domínios específicos:

| Agente | Persona | Domínio |
|--------|---------|---------|
| Automation Architect | Wire | n8n, Make, webhooks, pipelines |
| Cold Outreach | Hunter | Prospecção B2B, cold email |
| Copywriter | — | Copy persuasivo, ads, LPs |
| Creative Director | — | Direção criativa, criativos ads |
| CRO Specialist | — | Otimização de conversão |
| Growth Hacker | Surge | Algoritmos sociais, crescimento |
| Launch Strategist | — | Estratégia de lançamento |
| Market Intel | — | Inteligência de mercado |
| Offer Engineer | Forge | Ofertas irrecusáveis, stack de valor |
| Prompt Engineer | Prism | Prompts avançados, safety |
| RAG Architect | Sage | RAG, vector stores, memória dual |
| Swarm Simulator | Swarm | MiroFish, simulação multi-agente |
| Vibe Coder | Blast | B.L.A.S.T., context engineering |
| Voice AI Specialist | Vox | Voice AI, dublagem, TTS, ASR |
| WhatsApp Specialist | Zap | WhatsApp Bot, automações |
| Workflow Orchestrator | — | Workflows multi-step |
| **Advogado do Diabo** | — | **Análise crítica, riscos, suposições ocultas** |
| **Mestre do Conselho** | — | **Conselho deliberativo multi-perspectiva** |

### Skills (`skills/`)
20 skills especializadas que os agentes podem invocar:

| Skill | Descrição |
|-------|-----------|
| `ad-creative` | Geração de criativos para anúncios Meta Ads |
| `agent-council` | Conselho deliberativo multi-perspectiva |
| `agent-engineer` | Projeta agentes e squads |
| `algorithm-hack` | Engenharia reversa de algoritmos sociais |
| `cold-outreach-campaign` | Campanhas cold email B2B |
| `copywriting` | Copy persuasivo — AIDA, PAS, BAB, hooks, CTAs |
| `launch-strategy` | Estratégia de lançamento digital em 5 fases |
| `lead-magnets` | Criação de iscas digitais e LPs de captação |
| `marketing-psychology` | 18 gatilhos mentais e persuasão ética |
| `n8n-workflows` | Biblioteca de workflows n8n prontos |
| `offer-optimizer` | Framework 4-critérios + stack Hormozi |
| `ops-catalog` | Catálogo operacional de ferramentas e scripts |
| `page-cro` | Otimização de landing pages (CRO) — 7 pilares |
| `paid-ads` | Gestão de tráfego pago Meta Ads (metodologia Sobral) |
| `rag-builder` | Pipelines RAG de produção |
| `skill-creator` | Cria skills modulares padrão |
| `social-content` | Conteúdo para Instagram — posts, reels, carrosséis |
| `swarm-simulation` | Simulação MiroFish multi-agente |
| `voice-dubbing` | Pipeline de dublagem 10 etapas |
| `vps-setup` | Setup VPS Docker completo |

### Comandos Operacionais (`commands/`)
7 comandos standalone para operações do dia a dia:

| Comando | Descrição |
|---------|-----------|
| `/analyze-competitors` | Análise competitiva completa de concorrentes |
| `/campaign-report` | Relatório de campanha Meta Ads com análise Sobral/Hormozi |
| `/conteúdo-semanal` | Pesquisa + estratégia + criativos + upload Instagram |
| `/fix-instagram` | Diagnostica e corrige posts Instagram falhos |
| `/plan-launch` | Planeja lançamento digital completo |
| `/research` | Pesquisa profunda multi-fonte |
| `/whatsapp-bot` | Gerencia WhatsApp Bot com Claude AI |

### V6 Intelligence Layer (`docs/`, `data/`, `scripts/`, `templates/`)

| Arquivo | Descrição |
|---------|-----------|
| `docs/architecture.md` | Arquitetura completa do framework (7 camadas, 1055 linhas) |
| `docs/workflow-validation-matrix.md` | Status de maturidade de 20 workflows |
| `data/entity-registry.yaml` | IDS Registry com 37 entidades reutilizáveis |
| `data/smart-router.yaml` | Roteamento automático de tarefas (33 regras) |
| `templates/decision-log-template.md` | Template para registro de decisões autônomas |
| `scripts/health-check.sh` | Health check do framework (41 verificações) |

### Estrutura Organizacional (`organization/`)
8 departamentos com POPs e SIPOCs completos:

| Departamento | Agentes | Foco |
|-------------|---------|------|
| Diretoria | Nexo, Orion, Advisory Board | Estratégia, governança, orquestração |
| Engenharia | Morgan, Dex, Quinn, Aria, Gage, Dara, Pax, River, Craft, Uma | Desenvolvimento full-stack |
| Marketing & Conteúdo | Trig, Luna, Dash, Copywriter, Creative Director, CRO Specialist | Demanda e autoridade de marca |
| Comercial & Vendas | Max, Nico, Primo, Apex, Zap | Pipeline de vendas |
| Financeiro | Nova, Flex, Finn | Saúde financeira |
| CS & Retenção | Care, Pulse | Satisfação e retenção |
| Operações | Ori, Sentinel, Workflow Orchestrator | Processos e infraestrutura |
| Produto & Educação | Kai, Sage, Eve, Atlas, Market Intel, Launch Strategist | Produtos digitais e eventos |

### Rules (`rules/`)
8 regras que governam o framework:

| Rule | Governa |
|------|---------|
| `workflow-execution.md` | SDC phases, QA Loop, Spec Pipeline, Brownfield Discovery |
| `story-lifecycle.md` | Status progression, validation checklist, QA gate decisions |
| `agent-authority.md` | Delegation matrix — quem pode fazer o quê |
| `ids-principles.md` | REUSE > ADAPT > CREATE hierarchy |
| `coderabbit-integration.md` | Self-healing config, severity handling |
| `external-api-patterns.md` | SYNC > CACHE > REAL-TIME for API integrations |
| `mcp-usage.md` | MCP server governance and tool selection |
| **`eros-quality.md`** | **5 quality gates, failure taxonomy, proportionality** |

---

## Como usar

### Pré-requisitos

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) instalado
- Node.js 18+
- Git

### Instalação

```bash
# Clone o repositório
git clone https://github.com/DOMINA-IA/segunda-feira.git

# Copie os arquivos para sua configuração Claude Code
cp -r segunda-feira/commands/ ~/.claude/commands/
cp -r segunda-feira/agents/ ~/.claude/agents/
cp -r segunda-feira/skills/ ~/.claude/skills/
cp -r segunda-feira/rules/ ~/.claude/rules/
cp -r segunda-feira/organization/ ~/.claude/organization/
cp segunda-feira/CLAUDE.md ~/.claude/CLAUDE.md

# V6 Intelligence Layer (opcional mas recomendado)
cp -r segunda-feira/scripts/ ~/.claude/scripts/
cp -r segunda-feira/templates/ ~/.claude/templates/
cp -r segunda-feira/data/ ~/.claude/data/
cp -r segunda-feira/docs/ ~/.claude/docs/
```

### Uso básico

```bash
# No Claude Code, ative um agente
@dev           # Ativa o engenheiro sênior
@content       # Ativa a estrategista de conteúdo
@aios-master   # Ativa o master orchestrator

# Use comandos de agente
*help          # Mostra comandos disponíveis
*create-story  # Cria nova story
*task dev-develop-story  # Executa task de desenvolvimento

# Use skills
/paid-ads      # Gestão de tráfego pago
/copywriting   # Copy persuasivo
/launch-strategy  # Estratégia de lançamento

# V6: Health check do framework
bash ~/.claude/scripts/health-check.sh
```

### Personalização

Os agentes usam placeholders que você deve substituir:

| Placeholder | Substitua por |
|------------|--------------|
| `@your-handle` | Seu @ do Instagram |
| `your-domain.com` | Seu domínio |
| `YOUR_COMPANY` | Nome da sua empresa |
| `YOUR_NAME` | Seu nome |
| `YOUR_PIXEL_ID` | Seu Pixel Meta |
| `YOUR_PAGE_ID` | Seu Page ID Meta |
| `YOUR_APP_PATH` | Path da sua aplicação |
| `YOUR_VPS_IP` | IP do seu servidor |
| `YOUR_VPS_PASSWORD` | Senha do seu servidor |
| `YOUR_BOT_PORT` | Porta do seu bot |

---

## Estrutura do repositório

```
segunda-feira/
├── README.md
├── CLAUDE.md                              # Constituição v6.0
├── agents/                                # 18 agentes especialistas
├── commands/                              # 38 agentes core + 7 operacionais
├── skills/                                # 20 skills invocáveis
├── organization/                          # 8 departamentos
├── rules/                                 # 8 regras do framework
├── docs/                                  # [V6] Arquitetura + Workflow Matrix
│   ├── architecture.md                    # 7 camadas, 1055 linhas
│   └── workflow-validation-matrix.md      # 20 workflows com maturidade
├── data/                                  # [V6] IDS Registry + Smart Router
│   ├── entity-registry.yaml              # 37 entidades reutilizáveis
│   └── smart-router.yaml                 # 33 regras de roteamento
├── templates/                             # [V6] Decision Log
│   └── decision-log-template.md          # Template para decisões autônomas
└── scripts/                               # [V6] Health Check
    └── health-check.sh                   # 41 verificações automáticas
```

---

## Changelog

### V6.0 (2026-03-29) — Intelligence Layer
- **Health Check** — 41 verificações automáticas de integridade do framework
- **IDS Entity Registry** — 37 entidades catalogadas, REUSE > ADAPT > CREATE operacional
- **Smart Router** — 33 regras de roteamento + 8 colaborações multi-agente
- **Architecture Doc** — Documentação completa de 7 camadas (1055 linhas)
- **Decision Log Template** — Learning loop para decisões autônomas
- **Workflow Validation Matrix** — 20 workflows com status de maturidade
- **+2 agentes** — @advogado-do-diabo, @mestre-do-conselho
- **+1 regra** — EROS Quality Gates
- **100% skills padronizadas** com YAML frontmatter

### V5.0 (2026-03-20) — Consolidation
- Bump de versão, sanitização completa, 47 agentes, 20 skills

### V3.0 (2026-03-18) — Foundation
- Release inicial: 38 agentes, estrutura base

---

## Metodologias integradas

- **Pedro Sobral** — Escala e pausa de campanhas Meta Ads
- **Alex Hormozi** — Ofertas irrecusáveis e escala
- **Brian Manon** — Criativos de alta performance
- **Motion** — Analytics de criativos
- **SPIN Selling** — Discovery e fechamento high-ticket
- **CodeRabbit** — Self-healing de código com análise estática
- **IDS (Incremental Development System)** — REUSE > ADAPT > CREATE
- **MiroFish** — Simulação multi-agente e inteligência coletiva
- **B.L.A.S.T.** — Context engineering para desenvolvimento AI-first
- **EROS** — 5 portões de qualidade integrados em todos os workflows

---

## Licença

MIT License — use, modifique e distribua livremente.

---

*Segunda-feira v6.0 — 47+ agentes de IA. 55 skills. 8 rules. Self-healing. O terror do CLT.*
