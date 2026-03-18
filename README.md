# Segunda-feira

**38 agentes de IA. O terror do CLT.**

---

## O que e

Segunda-feira e um framework open-source de orquestracao de agentes de IA para desenvolvimento full-stack e operacoes de negocio. Ele define **38 agentes especializados** organizados em **8 departamentos**, cada um com:

- **Job Description** completo (cargo, missao, KPIs, autoridade, restricoes)
- **POP (Procedimento Operacional Padrao)** — passo a passo de como o agente executa seu trabalho
- **SIPOC** (Supplier-Input-Process-Output-Customer) — mapa de interacoes

Projetado para rodar com [Claude Code](https://docs.anthropic.com/en/docs/claude-code) da Anthropic, transformando um unico terminal em uma empresa inteira de agentes de IA.

## Por que o nome

Porque segunda-feira e o dia que todo mundo odeia — mas os agentes amam. Enquanto voce toma cafe, 38 agentes ja estao trabalhando.

---

## O que esta incluido

### Agentes (`commands/`)
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
| Trig | Gestor de Trafego Pago | sonnet |
| Luna | Estrategista de Conteudo | sonnet |
| Dash | Produtor de Video com IA | sonnet |
| Copywriter | Copy Persuasivo Multi-Canal | sonnet |
| Creative Director | Direcao Criativa | sonnet |
| CRO Specialist | Otimizacao de Conversao | sonnet |
| Max | Gestor Comercial Estrategico | opus |
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
| Workflow Orchestrator | Orchestrador Multi-Step | opus |
| Kai | Product Manager (Produtos Digitais) | opus |
| Sage | Mentor Educacional | haiku |
| Eve | Events Manager | haiku |
| Atlas | Business Analyst | sonnet |
| Market Intel | Inteligencia Competitiva | opus |
| Launch Strategist | Estrategista de Lancamentos | opus |

### Skills (`skills/`)
8 skills especializadas que os agentes podem invocar:

| Skill | Descricao |
|-------|-----------|
| `ad-creative` | Geracao de criativos para anuncios Meta Ads |
| `copywriting` | Copy persuasivo — AIDA, PAS, BAB, hooks, CTAs |
| `launch-strategy` | Estrategia de lancamento digital em 5 fases |
| `lead-magnets` | Criacao de iscas digitais e LPs de captacao |
| `marketing-psychology` | 18 gatilhos mentais e persuasao etica |
| `page-cro` | Otimizacao de landing pages (CRO) — 7 pilares |
| `paid-ads` | Gestao de trafego pago Meta Ads (metodologia Sobral) |
| `social-content` | Conteudo para Instagram — posts, reels, carrosseis |

### Estrutura Organizacional (`organization/`)
8 departamentos com POPs e SIPOCs completos:

| Departamento | Agentes | Foco |
|-------------|---------|------|
| Diretoria | Nexo, Orion, Advisory Board | Estrategia, governanca, orquestracao |
| Engenharia | Morgan, Dex, Quinn, Aria, Gage, Dara, Pax, River, Craft, Uma | Desenvolvimento full-stack |
| Marketing & Conteudo | Trig, Luna, Dash, Copywriter, Creative Director, CRO Specialist | Demanda e autoridade de marca |
| Comercial & Vendas | Max, Nico, Primo, Apex, Zap | Pipeline de vendas |
| Financeiro | Nova, Flex, Finn | Saude financeira |
| CS & Retencao | Care, Pulse | Satisfacao e retencao |
| Operacoes | Ori, Sentinel, Workflow Orchestrator | Processos e infraestrutura |
| Produto & Educacao | Kai, Sage, Eve, Atlas, Market Intel, Launch Strategist | Produtos digitais e eventos |

### Rules (`rules/`)
Regras do framework que governam workflows, ciclo de vida de stories, autoridade de agentes, integracao com CodeRabbit e padroes de API.

---

## Como usar

### Pre-requisitos

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) instalado
- Node.js 18+
- Git

### Instalacao

```bash
# Clone o repositorio
git clone https://github.com/YOUR_USERNAME/segunda-feira.git

# Copie os arquivos para sua configuracao Claude Code
cp -r segunda-feira/commands/ ~/.claude/commands/
cp -r segunda-feira/skills/ ~/.claude/skills/
cp -r segunda-feira/rules/ ~/.claude/rules/
cp -r segunda-feira/organization/ ~/.claude/organization/
cp segunda-feira/CLAUDE.md ~/.claude/CLAUDE.md
```

### Uso basico

```bash
# No Claude Code, ative um agente
@dev           # Ativa o engenheiro senior
@content       # Ativa a estrategista de conteudo
@aios-master   # Ativa o master orchestrator

# Use comandos de agente
*help          # Mostra comandos disponiveis
*create-story  # Cria nova story
*task dev-develop-story  # Executa task de desenvolvimento
```

### Personalizacao

Os agentes usam placeholders que voce deve substituir:

| Placeholder | Substitua por |
|------------|--------------|
| `@your-handle` | Seu @ do Instagram |
| `your-domain.com` | Seu dominio |
| `YOUR_PIXEL_ID` | Seu Pixel Meta |
| `YOUR_PAGE_ID` | Seu Page ID Meta |
| `YOUR_APP_PATH` | Path da sua aplicacao |

---

## Estrutura do repositorio

```
segunda-feira/
├── README.md
├── CLAUDE.md                          # Constituicao do framework
├── agents/                            # Agentes especializados (subagents)
│   ├── copywriter.md
│   ├── creative-director.md
│   ├── cro-specialist.md
│   ├── launch-strategist.md
│   ├── market-intel.md
│   ├── whatsapp-specialist.md
│   └── workflow-orchestrator.md
├── commands/                          # 38 comandos de agente
│   ├── aios-master.md
│   ├── dev.md
│   ├── qa.md
│   ├── architect.md
│   ├── traffic.md
│   ├── content.md
│   └── ... (35 mais)
├── skills/                            # 8 skills invocaveis
│   ├── ad-creative.md
│   ├── copywriting.md
│   ├── launch-strategy.md
│   ├── lead-magnets.md
│   ├── marketing-psychology.md
│   ├── page-cro.md
│   ├── paid-ads.md
│   └── social-content.md
├── organization/                      # Estrutura organizacional
│   ├── INDEX.md
│   ├── organograma.md
│   ├── cultura-organizacional.md
│   └── departamentos/
│       ├── diretoria.md
│       ├── engenharia.md
│       ├── marketing-conteudo.md
│       ├── comercial-vendas.md
│       ├── financeiro.md
│       ├── cs-retencao.md
│       ├── operacoes.md
│       └── produto-educacao-eventos.md
└── rules/                             # Regras do framework
    ├── workflow-execution.md
    ├── story-lifecycle.md
    ├── agent-authority.md
    ├── ids-principles.md
    ├── coderabbit-integration.md
    └── external-api-patterns.md
```

---

## Metodologias integradas

- **Pedro Sobral** — Escala e pausa de campanhas Meta Ads
- **Alex Hormozi** — Ofertas irrecusaveis e escala
- **Brian Manon** — Criativos de alta performance
- **Motion** — Analytics de criativos
- **SPIN Selling** — Discovery e fechamento high-ticket
- **CodeRabbit** — Self-healing de codigo com analise estatica
- **IDS (Incremental Development System)** — REUSE > ADAPT > CREATE

---

## Licenca

MIT License — use, modifique e distribua livremente.

---

*Segunda-feira v1.0 — 38 agentes de IA. O terror do CLT.*
