# Sistema de Agentes — App Starter

> Template reutilizável para criar ou evoluir qualquer app com documentação completa para Claude Code ou Figma Make.

---

> ⚠️ **Este repositório é um template — nunca abra esta pasta no Claude Code.**
> Use-o apenas para consultar e copiar os arquivos necessários.
> Crie uma pasta separada para cada projeto e cole os arquivos gerados pelo Agente 06 lá.

---

## Duas trilhas de uso

### Trilha A — Projeto novo
Para apps que ainda não existem. Os agentes descobrem, decidem e documentam.

### Trilha B — Projeto existente
Para apps que já existem. Os agentes auditam, corrigem e evoluem.

---

## Estrutura de pastas

```
/                              ← este repositório (template)
├── README.md                  ← este arquivo
├── APP_BRIEFING.md            ← briefing para projeto novo
├── design-tokens-global.css   ← fonte de verdade da identidade base (ecossistema)
├── design-tokens-global.json  ← mesmos tokens em JSON (W3C DTCG) — pra importar como Figma Variables de verdade
│
├── agents/                    ← Trilha A — projeto novo
│   ├── 01-produto.md
│   ├── 02-benchmark.md
│   ├── 03-identidade.md
│   ├── 04-visual.md
│   ├── 05-arquitetura.md
│   └── 06-gerador.md
│
└── agents-existente/          ← Trilha B — projeto existente
    ├── BRIEFING-EXISTENTE.md  ← briefing específico para auditoria
    ├── 01-produto.md          ← auditoria de produto
    ├── 02-benchmark.md        ← mercado atualizado
    ├── 03-identidade.md       ← consistência de marca
    ├── 04-visual.md           ← auditoria de design + tokens
    ├── 05-arquitetura.md      ← reverse engineering + dívida técnica
    └── 06-gerador.md          ← gera docs atualizados + CHANGELOG
```

---

## Trilha A — Projeto novo

### 1. Preencha o briefing
Duplique o `APP_BRIEFING.md`, renomeie para `briefing-[nome].md` e responda os blocos.

### 2. Rode os agentes em sequência

```
01-produto.md     → lê: briefing.md
                  → gera: 01-produto-output.md

02-benchmark.md   → lê: briefing + output 01
                  → gera: 02-benchmark-output.md

03-identidade.md  → lê: outputs 01 + 02
                  → gera: 03-identidade-output.md

04-visual.md      → lê: outputs 01 + 02 + 03
                  → gera: 04-visual-output.md

05-arquitetura.md → lê: outputs 01 a 04
                  → gera: 05-arquitetura-output.md

06-gerador.md     → lê: todos os outputs (01 a 05)
                  → gera: CLAUDE.md, app.md, SETUP.md, DESIGN.md
```

### 3. Use os arquivos gerados

**Claude Code:** coloque na raiz do projeto e instrua:
> *"Leia o CLAUDE.md e comece pela Etapa 1 do SETUP.md."*

**Figma Make:** substitua `guidelines/Guidelines.md` e `src/styles/theme.css`. Use o `MAKE_PROMPT.md` para gerar telas em sequência.

---

## Trilha B — Projeto existente

### 1. Preencha o briefing de auditoria
Duplique o `agents-existente/BRIEFING-EXISTENTE.md` e responda com foco no estado atual — não no que foi planejado.

### 2. Disponibilize o design-tokens-global.css
Se o projeto faz parte do ecossistema, o Agente 04 usa este arquivo como fonte de verdade para auditar os tokens.

### 3. Rode os agentes em sequência

```
01-produto.md     → auditoria de produto: real vs planejado
02-benchmark.md   → mercado atualizado: novos concorrentes, novo posicionamento
03-identidade.md  → consistência de marca: nome, tom, microcopy
04-visual.md      → auditoria de design: tokens, componentes, WCAG, dark mode
05-arquitetura.md → reverse engineering: stack real, dívida técnica, plano do ciclo
06-gerador.md     → docs atualizados + CHANGELOG
```

### 4. Use os arquivos gerados

**Claude Code:** atualize os arquivos na raiz do projeto e instrua:
> *"Leia o CLAUDE.md, consulte o CHANGELOG.md para entender o que mudou, e comece pela Etapa 1 da ordem de implementação deste ciclo."*

---

## O arquivo design-tokens-global.css

É a fonte de verdade da identidade visual do ecossistema. Contém:

**Camada 1 — Primitivos** (não usar diretamente em componentes)
- Paleta brasileira: Chá Mate, Jambu, Azul Pantanal, Figo
- Neutros quentes (nunca branco puro ou cinza frio)
- Escala tipográfica completa
- Raios semânticos
- Espaçamento
- Motion tokens

**Camada 2 — Semânticos** (estes os componentes usam)
- Hierarquia de texto (`--text-heading`, `--text-primary`...)
- Fundos (`--bg-page`, `--bg-surface`...)
- Acento com regras WCAG (`--accent-deco`, `--accent-text`, `--accent-btn`)
- `--structural` — sobrescrito por produto

**Camada de produto** (cada projeto define a sua)
- Sobrescreve apenas `--structural` e tokens específicos do domínio
- Não cria novos primitivos — reutiliza os existentes

**Regras WCAG AA auditadas:**
- Nunca `--color-jambu` puro como texto sobre fundo claro
- Nunca texto branco sobre `--color-jambu` puro
- `--accent-text` (jambu-text) sobre `--bg-page`: 5.84:1
- `prefers-reduced-motion` desativa todas as animações

---

## Fluxo visual — Trilha A

```
briefing.md
    │
    ▼
[01] Produto ──────────────────────────────┐
    │                                      │
    ▼                                      │
[02] Benchmark ──────────────────────────┐ │
    │                                    │ │
    ▼                                    │ │
[03] Identidade ────────────────────────┐│ │
    │                                   ││ │
    ▼                                   ││ │
[04] Visual ───────────────────────────┐││ │
    │                                  │││ │
    ▼                                  │││ │
[05] Arquitetura                       │││ │
    │                                  │││ │
    └──────────────────────────────────┘││ │
                                        ││ │
    ▼                                   ││ │
[06] Gerador ◄───────────────────────────┘┘─┘
    │
    ▼
CLAUDE.md + app.md + SETUP.md + DESIGN.md
```

## Fluxo visual — Trilha B

```
briefing-existente.md + design-tokens-global.css
    │
    ▼
[01] Auditoria Produto ─────────────────────┐
    │                                       │
    ▼                                       │
[02] Benchmark Atualizado ─────────────────┐│
    │                                      ││
    ▼                                      ││
[03] Consistência Identidade ─────────────┐││
    │                                     │││
    ▼                                     │││
[04] Auditoria Visual + Tokens ──────────┐│││
    │                                    ││││
    ▼                                    ││││
[05] Reverse Eng. + Dívida Técnica       ││││
    │                                    ││││
    └────────────────────────────────────┘│││
                                          │││
    ▼                                     │││
[06] Gerador ◄─────────────────────────────┘┘┘
    │
    ▼
CLAUDE.md + app.md + SETUP.md + DESIGN.md + CHANGELOG.md
```

---

## Dicas

**Pode pular agentes?**
Sim, se já tiver clareza. Mas o 06 precisa de todos os outputs. Se pular um agente, crie um output manual.

**Pode rodar tudo em uma conversa?**
Sim. Cole os agentes em sequência passando os outputs de um para o próximo.

**Pode iterar num agente sem refazer os outros?**
Sim. Se o visual mudar, só re-roda o 04 e o 06.

**Qual agente dá mais trabalho na Trilha B?**
O 04 (Visual) — porque cruza o código existente com o `design-tokens-global.css` e exige atenção a cada token.

**O design-tokens-global.css é obrigatório?**
Só se o projeto fizer parte do ecossistema. Para projetos isolados, o Agente 04 da Trilha A gera os tokens do zero.