# Sistema de Agentes — App Starter

> Template reutilizável para criar ou evoluir qualquer app com documentação completa para Claude Code ou Figma Make.

---

> ⚠️ **Este repositório é um template — nunca abra esta pasta no Claude Code.**
> Use-o apenas para consultar e copiar os arquivos necessários.
> Crie uma pasta separada para cada projeto e cole os arquivos gerados pelo Agente 06 lá.

---

## Para quem nunca usou (pré-requisitos e instalação)

### O que você precisa ter instalado
1. **VS Code** — [code.visualstudio.com](https://code.visualstudio.com/)
2. **Claude Code** — extensão/CLI oficial da Anthropic. Guia oficial: [claude.com/claude-code](https://claude.com/claude-code). Requer uma conta com acesso ao Claude (assinatura Pro/Max, ou uma API key da Anthropic).
3. **Git** (opcional, só se for clonar em vez de baixar ZIP) — [git-scm.com](https://git-scm.com/)

### Como baixar este repositório
**Opção A — sem usar linha de comando (mais simples):**
1. Nesta página do GitHub, clique no botão verde **"Code"** → **"Download ZIP"**.
2. Extraia o ZIP em qualquer pasta do seu computador (ex: `Downloads/Inicio_de_Projetos`).

**Opção B — clonando com git:**
```
git clone https://github.com/jeffreiry/Inicio_de_Projetos.git
```

**Opção C — usar como template (recomendado se você vai customizar o template para seu próprio uso):**
No GitHub, clique em **"Use this template"** → **"Create a new repository"**. Isso cria uma cópia independente na sua própria conta, que você pode editar sem afetar o repositório original.

### Regra mais importante deste repositório
> ⚠️ Depois de baixar, **nunca abra a pasta `Inicio_de_Projetos` diretamente no Claude Code/VS Code como se fosse o seu projeto**. Ela é só uma "prateleira" de onde você copia arquivos. Cada app que você for criar precisa da **sua própria pasta separada**.

### Primeiro uso, passo a passo
1. Crie uma pasta nova para o seu app (ex: `MeuApp/`) e abra **essa pasta** no VS Code.
2. Volte na pasta `Inicio_de_Projetos` e copie o arquivo `APP_BRIEFING.md` para dentro da pasta do seu app.
3. Renomeie a cópia para `briefing-[nome-do-app].md` e responda as perguntas (pode ser aos poucos).
4. Abra o Claude Code dentro da pasta do seu app e cole o conteúdo do agente `agents/01-produto.md`, seguido do seu briefing respondido, numa única mensagem.
5. Siga a sequência de agentes (02, 03, 04, 05, 06) descrita na seção "Trilha A" abaixo — cada um lê o output do anterior e você vai colando/copiando os arquivos gerados dentro da pasta do seu app.
6. No final, o Agente 06 gera `CLAUDE.md`, `app.md`, `SETUP.md` e `DESIGN.md` prontos. Com esses arquivos na raiz do seu projeto, instrua o Claude Code: *"Leia o CLAUDE.md e comece pela Etapa 1 do SETUP.md."*

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

### 2. Rode os agentes em sequência

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

## Arquitetura de tokens (usada pelo Agente 04 em ambas as trilhas)

Todo projeto gerado por este template segue duas camadas de tokens:

**Camada 1 — Primitivos** (não usar diretamente em componentes)
- Paleta de cores escolhida para o produto
- Neutros (quentes ou frios, conforme o tom do produto)
- Escala tipográfica completa
- Raios semânticos
- Espaçamento
- Motion tokens

**Camada 2 — Semânticos** (estes os componentes usam)
- Hierarquia de texto (`--text-heading`, `--text-primary`...)
- Fundos (`--bg-page`, `--bg-surface`...)
- Acento com regras WCAG (`--accent-deco`, `--accent-text`, `--accent-btn`)

**Regras WCAG AA obrigatórias:**
- A cor de acento nunca vira texto sem contraste calculado e documentado
- Todo par texto/fundo relevante tem o ratio real auditado
- `prefers-reduced-motion` desativa todas as animações

Cada projeto tem sua própria paleta — os tokens nascem do zero a cada uso (Trilha A) ou são reverse-engineered do código existente (Trilha B). Não há um arquivo global compartilhado neste template.

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
briefing-existente.md
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
O 04 (Visual) — porque precisa reverse-engineer os tokens a partir do código existente e exige atenção a cada componente.

**Preciso ter um design system pronto antes de começar?**
Não. Na Trilha A, o Agente 04 gera a paleta e os tokens do zero com base no seu briefing. Na Trilha B, ele audita o que já existe no código, mesmo que nunca tenha sido formalizado em tokens.