---
name: paid-ads
description: "Gestao de trafego pago Meta Ads — estrutura de campanhas, escala, analise diaria, metodologia Pedro Sobral."
user-invocable: true
allowed-tools:
  - Read
  - Write
  - Edit
  - Bash
  - Grep
  - Glob
  - WebSearch
  - WebFetch
---

# Paid Ads — Skill de Gestao de Trafego Meta Ads

## Contexto

**Pixel ID:** YOUR_PIXEL_ID
**Page ID:** YOUR_PAGE_ID
**Conta de anuncios:** Via Meta Business Suite
**Metodologia base:** Pedro Sobral + Alex Hormozi + Brian Manon + Motion

---

## Estrutura de Campanha Padrao

### Configuracao Obrigatoria
| Parametro | Valor |
|-----------|-------|
| Tipo de compra | AUCTION |
| Objetivo | OUTCOME_LEADS (OFFSITE_CONVERSIONS) |
| Orcamento | CBO (Campaign Budget Optimization) |
| Otimizacao | Advantage+ |
| Publico | 25-65 anos |
| Posicionamento | Advantage+ Placements (automatico) |
| Evento de conversao | Lead (formulario na LP) |

### Estrutura Hierarquica
```
Campanha (CBO — orcamento aqui)
├── Conjunto de Anuncios 1 (segmentacao A)
│   ├── Anuncio 1A (criativo variacao A)
│   ├── Anuncio 1B (criativo variacao B)
│   └── Anuncio 1C (criativo variacao C)
├── Conjunto de Anuncios 2 (segmentacao B)
│   ├── Anuncio 2A
│   └── Anuncio 2B
└── Conjunto de Anuncios 3 (lookalike/retargeting)
    ├── Anuncio 3A
    └── Anuncio 3B
```

---

## Regras de Segmentacao

### Configuracao Advantage+
```json
{
  "targeting": {
    "age_min": 25,
    "age_max": 65,
    "genders": [0],
    "geo_locations": {
      "countries": ["BR"]
    },
    "publisher_platforms": ["facebook", "instagram"],
    "flexible_spec": [
      {
        "interests": [
          {"id": "INTEREST_ID", "name": "Interest Name"}
        ]
      }
    ]
  },
  "optimization_goal": "OFFSITE_CONVERSIONS",
  "billing_event": "IMPRESSIONS",
  "bid_strategy": "LOWEST_COST_WITHOUT_CAP"
}
```

### Exclusoes Obrigatorias
- Ja convertidos (custom audience de leads)
- Menores de 25 anos
- Publicos irrelevantes

---

## Metodologia Sobral — Regras de Escala

### Regra de Ouro: NUNCA Aumentar Orcamento em Campanha Vencedora

**ERRADO:**
```
Campanha CPL R$4 → Aumentar orcamento de R$30 para R$60
Resultado: CPL sobe para R$8-12 (piora 2-3x)
```

**CORRETO:**
```
Campanha CPL R$4 → DUPLICAR campanha inteira com mesmo orcamento
Resultado: 2 campanhas a R$30 cada, CPL mantem ~R$4
```

### Protocolo de Duplicacao
1. Duplicar a **CAMPANHA INTEIRA** (nao apenas o conjunto de anuncios)
2. Manter **MESMO orcamento** da original
3. Manter **MESMOS criativos** da original
4. Agendar inicio para **00:05h do dia seguinte**
5. Nomear: `{Nome Original} Copia{N}` (ex: "V3 LP Copia2")
6. Esperar **48h** antes de avaliar performance da copia

### Regras de Decisao Diaria

| Metrica | Acao | Condicao |
|---------|------|----------|
| CPL < alvo por 3+ dias | **ESCALAR** — Duplicar campanha | CPL consistente |
| CPL entre alvo e 1.5x | **MANTER** — Observar mais 24h | Pode ser flutuacao |
| CPL entre 1.5x e 2x alvo | **ALERTA** — Observar mais 24h | Se nao melhorar, pausar |
| CPL > 2x alvo por 2 dias | **PAUSAR** — Desligar imediatamente | Nao tem recuperacao |
| Frequencia > 3.0 | **PAUSAR** — Fadiga de criativo | Publico saturado |
| CTR < 0.8% | **TROCAR CRIATIVO** | Hook fraco |
| CTR > 2.0% | **VENCEDOR** — Considerar escala | Criativo forte |

### Analise Diaria Obrigatoria (Checklist)
Todos os dias as 10h, revisar:
- [ ] CPL de cada campanha ativa
- [ ] CTR de cada anuncio
- [ ] Frequencia de cada conjunto
- [ ] Gasto acumulado vs budget planejado
- [ ] Leads captados vs meta
- [ ] Projecao de leads ate fim do periodo

### Nota de Conta
- Conta nova: CPL mais alto nas primeiras 2 semanas
- Conta com historico: CPL mais estavel
- **NUNCA pausar todas as campanhas de uma vez** — mata a nota
- Sempre manter pelo menos 1 campanha rodando (mesmo que R$10/dia)

---

## Transicao de Angulos

### Framework de Angulos
| Tipo | Exemplo | Quando Usar |
|------|---------|-------------|
| **Dinheiro direto** | "De R$3K a R$30K com IA" | Sempre funciona, angulo campeao |
| **Oportunidade oculta** | "O mercado que ninguem ve" | Curiosidade, topo de funil |
| **Medo de perder** | "Enquanto voce espera, outros lucram" | Urgencia, retargeting |
| **Prova social** | "218 pessoas ja se inscreveram" | Meio/fundo de funil |
| **Transformacao** | "Antes: CLT R$3K. Depois: R$30K/mes" | Aspiracional, topo |
| **Autoridade** | "Testei 47 ferramentas de IA" | Credibilidade, educativo |

---

## Regras de Orcamento

### Distribuicao de Budget
| Fase | % do Budget | Foco |
|------|------------|------|
| Teste de criativos | 20% | 3-5 criativos, R$15-20/dia cada |
| Validacao | 30% | Duplicar vencedores, confirmar CPL |
| Escala | 50% | Duplicacoes dos validados |

### Limites
- Orcamento minimo por campanha: R$20/dia
- Orcamento maximo por campanha: R$100/dia (para conta atual)
- Nunca gastar mais que 30% do budget em um unico dia
- Sempre manter reserva de 20% para oportunidades

---

## Padrao de Criativos para Ads

### Formato Obrigatorio
- **Dimensao:** 1080x1920 (9:16) — Stories/Reels
- **Formato feed (quando solicitado):** 1080x1080 (1:1)
- **Design campeao:** Fundo escuro (#0D0D0D) + destaques verde (#00FF88 ou #39FF14)
- **Texto:** Branco sobre fundo escuro, fonte bold

### Regras de Criativo
- SEMPRE com acentos corretos
- NUNCA recortar foto de dentro de outro criativo
- NUNCA usar a mesma imagem em multiplos anuncios
- Maximo 20% de texto na imagem (regra Meta)
- CTA visivel e contrastante

---

## Meta API — Rate Limits e Boas Praticas

### Limites
- **200 chamadas/hora** por conta de anuncios
- **Batch requests:** Maximo 50 por batch
- **Rate limit 429:** Cooldown global de 5 minutos

### Boas Praticas
- Usar batch requests para multiplas operacoes
- Implementar exponential backoff em erros
- Cachear dados de campanhas localmente
- NUNCA fazer polling agressivo de metricas (maximo 1x/hora)
- Usar webhooks quando disponivel

---

## Processo de Criacao de Campanha

1. **Definir objetivo** — Leads, vendas, trafego
2. **Selecionar angulo** — Usar framework de angulos acima
3. **Criar criativos** — 3-5 variacoes do angulo (usar skill `ad-creative`)
4. **Configurar campanha** — CBO, Advantage+, segmentacao padrao
5. **Definir orcamento** — R$20-45/dia para teste
6. **Agendar** — Inicio as 00:05h do dia seguinte
7. **Monitorar** — Analise diaria por 48h antes de qualquer decisao
8. **Decidir** — Escalar, manter ou pausar conforme regras acima
