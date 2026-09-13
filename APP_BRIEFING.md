# App Briefing — Template

> Responda este arquivo antes de iniciar qualquer projeto de app. As respostas serão usadas para gerar os arquivos `app.md`, `SETUP.md`, `DESIGN.md` e `CLAUDE.md` prontos para o VS Code.
>
> Não precisa responder tudo de uma vez. Comece pelo Bloco 1 e avance conforme o projeto toma forma.

---

## Bloco 1 — Conceito

> O objetivo aqui é entender o que o app faz e por que ele existe.

**1.1** Em uma frase, o que o app faz?
```
Ex: "Registrar e compartilhar cada cafeteria que você já visitou."
```

**1.2** Qual o problema real que ele resolve? Para quem?
```
Ex: "Quem gosta de café não tem onde guardar a memória das cafeterias que
     visitou — só existe app de review genérico, não um focado na experiência."
```

**1.3** Existe algum app parecido no mercado? O que falta neles?
```
Ex: "Existem apps de review de estabelecimentos em geral. Nenhum foca na
     experiência de cafeteria como coleção pessoal."
```

**1.4** Se fosse descrever o app como "o [referência] para [nicho]", como seria?
```
Ex: "O Letterboxd para cafeterias." / "O Vivino para cervejas artesanais."
```

**1.5** Qual o loop principal do usuário? (o que ele faz repetidamente)
```
Ex: Descobrir → Registrar → Avaliar → Compartilhar
```

---

## Bloco 2 — Público

> Entender quem usa define tom, complexidade e features prioritárias.

**2.1** Quem é o usuário principal? Descreva em uma linha.
```
Ex: "Entusiasta de café, 20–40 anos, que viaja e gosta de descobrir lugares novos."
```

**2.2** O app é para um nicho raiz ou para um público mais amplo?
```
Ex: "Nicho raiz no início, mas a linguagem deve ser acessível para qualquer
     pessoa que já tomou um café fora de casa."
```

**2.3** O usuário é técnico (entende do assunto) ou casual?
```
Ex: "Técnico — vai notar se o método de extração estiver errado na ficha."
```

**2.4** Qual o contexto de uso? Quando e onde o usuário abre o app?
```
Ex: "Dentro da cafeteria, logo após pedir, ou em viagens explorando a cidade."
     → Implica: entrada rápida de dados, uso com uma mão, boa localização.
```

---

## Bloco 3 — Nome e Identidade verbal

> O nome e o tom de voz são decisões de produto, não de marketing.

**3.1** Já tem um nome? Se sim, qual e por quê esse?
```
Ex: "Grão — a menor unidade do café, o começo de tudo. Funciona como
     vocabulário do universo cafeeiro e como conceito para qualquer pessoa."
```

**3.2** Se não tem nome, qual o território que você quer explorar?
```
Opções de território:
[ ] Ação/verbo                (ex: Sipped, Brewed, Steeped)
[ ] Vocabulário técnico        (ex: Grão, Espresso, Crema)
[ ] Conceito/metáfora          (ex: Refúgio, Pausa, Aroma)
[ ] Funcional/descritivo       (ex: Cafelog, Coffeelist, Cupboard)
[ ] Invented/brandável         (ex: Brewly, Cuppa, Grindly)
```

**3.3** Qual o subtítulo? (aparece abaixo do nome, explica o que é)
```
Ex: "Sua vida em cafés." — possessivo, afetivo, claro.
    Modelo Letterboxd: "Your life in film."
```

**3.4** Qual a tagline de campanha? (emoção, não descrição)
```
Ex: "Cada xícara tem sua história."
```

**3.5** Como a voz do app deve soar? Marque o que se aplica:
```
Tom:
[ ] Caloroso e acolhedor      [ ] Técnico e preciso
[ ] Bem-humorado              [ ] Sério e contido
[ ] Entusiasta / animado      [ ] Minimalista / seco

Evitar:
[ ] Corporativo               [ ] Gírias forçadas
[ ] Snob / exclusivo          [ ] Genérico demais
```

**3.6** Escreva 2–3 exemplos de microcopy no tom certo:
```
Ex:
- Onboarding:      "Qual foi a cafeteria que te marcou?"
- Empty state:     "Toda coleção começa com uma primeira xícara."
- Após registrar:  "Registrado. Mais um grão na sua coleção."
```

---

## Bloco 4 — Features

> Definir o escopo evita que o Claude Code tente construir tudo de uma vez.

**4.1** Quais são as 3–5 features sem as quais o app não existe (MVP)?
```
Ex:
1. Buscar e registrar uma cafeteria com status e nota
2. Perfil público com histórico e stats
3. Feed de atividades de amigos
4. Listas curadas pelo usuário
5. Login com Google/Apple
```

**4.2** O que fica para a Fase 2? (depois do MVP validado)
```
Ex: Reviews com texto, fotos, conquistas, mapa de cafeterias visitadas, notificações push
```

**4.3** O que está explicitamente fora do escopo?
```
Ex: "Não é sobre venda de café ou assinatura de grãos. Não é agenda de eventos.
     Não é marketplace de cafeterias."
```

**4.4** Tem alguma feature de diferenciação — algo que nenhum concorrente faz?
```
Ex: "Registrar cafeterias visitadas em viagens (não só as da sua cidade) com
     contexto (sozinho, trabalho, com amigos) e avaliação por dimensão (ambiente, café, atendimento)."
```

---

## Bloco 5 — Direção Visual

> Estas respostas viram diretamente o DESIGN.md.

**5.1** Qual o tom visual geral? Marque um por coluna:

```
Energia:
[ ] Vibrante / festival        [ ] Contido / elegante
[ ] Bold / agressivo           [ ] Suave / acolhedor

Acabamento:
[ ] Premium / luxury           [ ] Popular / acessível
[ ] Editorial / magazine       [ ] Técnico / funcional
[ ] Lo-fi / retro              [ ] Clean / moderno
```

**5.2** Quais apps ou produtos (fora do seu nicho) têm o visual que você quer?
```
Ex: "Letterboxd (hierarquia editorial), Vivino (clareza + foto como herói),
     Notion (minimalismo funcional)"
```

**5.3** Tema padrão:
```
[ ] Dark mode (primário) com opção light
[ ] Light mode (primário) com opção dark
[ ] Apenas dark
[ ] Apenas light
[ ] Segue o sistema do dispositivo
```

**5.4** Tem alguma cor já definida ou em mente?
```
Ex: "Marrom-café (#6F4E37) como acento. Fundo bege quente (#F5F2EA).
     No dark: marrom bem escuro, nunca preto puro."
```

**5.5** Tem alguma cor que você quer evitar?
```
Ex: "Nada de roxo, gradientes coloridos ou azul corporativo."
```

**5.6** Como o nome/logo do app deve aparecer? (wordmark, ícone, combinação)
```
Ex: "Wordmark do nome em peso 700 + mark geométrico simples ao lado."
```

**5.7** Tipografia — tem preferência ou deixa o Claude sugerir?
```
Ex: "Display: uma serifada para títulos.
     Corpo: uma sans-serif legível. Dados/specs: uma monoespaçada."
```

---

## Bloco 6 — Arquitetura

> Estas respostas viram o SETUP.md.

**6.1** Qual o target do app?
```
[ ] Mobile (iOS + Android)
[ ] Web app (desktop + mobile browser)
[ ] Ambos
```

**6.2** Framework preferido (ou deixa o Claude decidir)?
```
Ex: "React Native + Expo para mobile. Supabase como backend."
[ ] React Native + Expo
[ ] Flutter
[ ] React (web)
[ ] Next.js (web)
[ ] Deixa o Claude decidir baseado no escopo
```

**6.3** Precisa de backend próprio ou um BaaS resolve?
```
[ ] BaaS (Supabase, Firebase) — recomendado para MVP
[ ] API própria (NestJS, Fastify) — para escala ou necessidades específicas
[ ] Sem backend (client-only, dados locais)
```

**6.4** Autenticação: quais provedores são obrigatórios?
```
[ ] Google OAuth        (alta conversão Android)
[ ] Apple Sign In       (obrigatório App Store se tiver social login)
[ ] Email + senha
[ ] Magic link (email sem senha)
[ ] Outro: ___________
```

**6.5** O app precisa funcionar offline?
```
[ ] Sim — funcionalidade principal deve funcionar sem internet
[ ] Parcialmente — leitura offline, escrita com sync
[ ] Não — requer conexão
```

**6.6** Vai ter upload de fotos/mídia pelo usuário?
```
[ ] Sim
[ ] Não
[ ] Talvez (fase 2)
```

**6.7** Vai ter notificações push?
```
[ ] Sim (MVP)
[ ] Sim (fase 2)
[ ] Não
```

**6.8** Tem alguma integração externa já mapeada?
```
Ex: "Google Places API para buscar e importar dados de estabelecimentos.
     Mapbox para o mapa de lugares visitados."
```

---

## Bloco 7 — Ambiente de Desenvolvimento

> Define quais arquivos serão gerados e como.

**7.1** Qual ferramenta será usada para desenvolver?
```
[ ] Claude Code no VS Code      → gera CLAUDE.md + SETUP.md + DESIGN.md + app.md
[ ] Figma Make                  → gera Guidelines.md + theme.css + MAKE_PROMPT.md
[ ] Ambos (protótipo no Make, produção no Claude Code)
```

**7.2** Tem alguma convenção de código ou preferência de estilo?
```
Ex: "TypeScript strict. NativeWind para estilos (nunca StyleSheet.create).
     Zustand para estado global. TanStack Query para cache."
```

**7.3** Tem alguma restrição de licença, compliance ou privacidade relevante?
```
Ex: "LGPD — usuário brasileiro. Obrigatório: export de dados, direito ao
     esquecimento, remoção de EXIF das fotos."
```

---

## Bloco 8 — Negócio (opcional, mas útil)

**8.1** O app é gratuito, pago ou freemium?
```
Ex: "Freemium — funcionalidades básicas gratuitas, plano premium para
     estatísticas avançadas e sem anúncios."
```

**8.2** Como o app ganha dinheiro (se ganhar)?
```
Ex: "Assinatura mensal + parcerias com cafeterias para destaque no app."
```

**8.3** Qual o critério de sucesso do MVP?
```
Ex: "100 usuários ativos registrando pelo menos 1 visita por semana."
```

---

## Output esperado

Com este briefing respondido, o Claude irá gerar:

| Arquivo | Conteúdo |
|---|---|
| `app.md` | Produto completo — conceito, entidades, telas, regras de negócio, gamificação |
| `SETUP.md` | Stack, estrutura de pastas, schema SQL, variáveis de ambiente, ordem de implementação |
| `DESIGN.md` | Tokens de cor (dark/light), tipografia, componentes, do's and don'ts |
| `CLAUDE.md` | Instruções automáticas para o agente — lido ao abrir o projeto no VS Code |

Se o destino for **Figma Make**, também serão gerados:

| Arquivo | Conteúdo |
|---|---|
| `Guidelines.md` | Versão das diretrizes visuais no formato que o Make lê |
| `theme.css` | Tokens CSS em HSL + classes utilitárias prontas |
| `MAKE_PROMPT.md` | Prompt inicial + prompts de iteração tela a tela |

---

## Como usar este arquivo

1. Duplique este arquivo e renomeie para `briefing-[nome-do-app].md`
2. Responda os blocos na ordem — pode pular os opcionais
3. Cole o arquivo respondido em uma nova conversa com o Claude com a instrução:

```
Leia o briefing abaixo e gere os arquivos de projeto:
app.md, SETUP.md, DESIGN.md e CLAUDE.md prontos para o VS Code.
Se o destino for Figma Make, gere também Guidelines.md, theme.css e MAKE_PROMPT.md.

[cole o briefing aqui]
```

4. O Claude irá fazer perguntas de esclarecimento se alguma resposta estiver ambígua antes de gerar os arquivos.
ENDOFFILE