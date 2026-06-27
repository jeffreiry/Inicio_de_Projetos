# App Briefing — Template

> Responda este arquivo antes de iniciar qualquer projeto de app. As respostas serão usadas para gerar os arquivos `app.md`, `SETUP.md`, `DESIGN.md` e `CLAUDE.md` prontos para o VS Code.
>
> Não precisa responder tudo de uma vez. Comece pelo Bloco 1 e avance conforme o projeto toma forma.

---

## Bloco 1 — Conceito

> O objetivo aqui é entender o que o app faz e por que ele existe.

**1.1** Em uma frase, o que o app faz?
```
Ex: "Registrar e compartilhar cada carro que você já dirigiu."
```

**1.2** Qual o problema real que ele resolve? Para quem?
```
Ex: "Entusiastas automotivos não têm onde guardar a memória das experiências
     de dirigir — só existe app para o carro que você TEM, não para os que já dirigiu."
```

**1.3** Existe algum app parecido no mercado? O que falta neles?
```
Ex: "Existe spotting (ver carros) e logbook (quilômetros). Nenhum foca na
     experiência de dirigir como coleção pessoal."
```

**1.4** Se fosse descrever o app como "o [referência] para [nicho]", como seria?
```
Ex: "O Letterboxd para carros." / "O Vivino para cervejas artesanais."
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
Ex: "Entusiasta automotivo, 25–45 anos, que vai a track days e lê FlatOut."
```

**2.2** O app é para um nicho raiz ou para um público mais amplo?
```
Ex: "Nicho raiz no início, mas a linguagem deve ser acessível para qualquer
     pessoa que já dirigiu um carro."
```

**2.3** O usuário é técnico (entende do assunto) ou casual?
```
Ex: "Técnico — vai notar se o V6 biturbo estiver errado na ficha do carro."
```

**2.4** Qual o contexto de uso? Quando e onde o usuário abre o app?
```
Ex: "Após um test drive, em eventos automotivos, viagens de estrada."
     → Implica: dark mode nativo, uso noturno, entrada rápida de dados.
```

---

## Bloco 3 — Nome e Identidade verbal

> O nome e o tom de voz são decisões de produto, não de marketing.

**3.1** Já tem um nome? Se sim, qual e por quê esse?
```
Ex: "Apex — o ponto exato da curva onde tudo se encaixa. Funciona como
     vocabulário de pista e como 'ápice' para qualquer pessoa."
```

**3.2** Se não tem nome, qual o território que você quer explorar?
```
Opções de território:
[ ] Ação/verbo de pilotagem  (ex: Shifted, Floored, Sent)
[ ] Vocabulário técnico      (ex: Apex, Redline, Heel-Toe)
[ ] Conceito/metáfora        (ex: Overdrive, Sunday, Backroads)
[ ] Funcional/descritivo     (ex: Carlog, Drivelog, Garage)
[ ] Invented/brandável       (ex: Shiftify, Revved, Drivend)
```

**3.3** Qual o subtítulo? (aparece abaixo do nome, explica o que é)
```
Ex: "Sua vida em carros." — possessivo, afetivo, claro.
    Modelo Letterboxd: "Your life in film."
```

**3.4** Qual a tagline de campanha? (emoção, não descrição)
```
Ex: "Toda volta tem seu ápice."
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
- Onboarding:      "Qual foi o carro que te marcou?"
- Empty state:     "Toda coleção começa com uma primeira volta."
- Após registrar:  "Registrado. Mais um ápice na sua coleção."
```

---

## Bloco 4 — Features

> Definir o escopo evita que o Claude Code tente construir tudo de uma vez.

**4.1** Quais são as 3–5 features sem as quais o app não existe (MVP)?
```
Ex:
1. Buscar e registrar um carro com status e nota
2. Perfil público com histórico e stats
3. Feed de atividades de amigos
4. Listas curadas pelo usuário
5. Login com Google/Apple
```

**4.2** O que fica para a Fase 2? (depois do MVP validado)
```
Ex: Reviews com texto, fotos, conquistas, mapa de drives, notificações push
```

**4.3** O que está explicitamente fora do escopo?
```
Ex: "Não é sobre tuning ou customização. Não é mileage tracker.
     Não é marketplace de carros."
```

**4.4** Tem alguma feature de diferenciação — algo que nenhum concorrente faz?
```
Ex: "Registrar carros que você dirigiu (não só os seus) com contexto
     (test drive, aluguel, amigo) e avaliação por dimensão (fun, sound, comfort)."
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
Ex: "Forza Horizon (energia + amarelo), Gran Turismo 7 (precisão + carro como herói),
     Super Woden GP (calor lo-fi), Letterboxd (hierarquia editorial)"
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
Ex: "Amarelo campeonato (#FFD60A) como acento. Fundo midnight (#0D1117).
     No light: pergaminho (#F5F2EA), nunca branco puro."
```

**5.5** Tem alguma cor que você quer evitar?
```
Ex: "Nada de roxo, gradientes coloridos ou azul corporativo."
```

**5.6** Como o nome/logo do app deve aparecer? (wordmark, ícone, combinação)
```
Ex: "Wordmark 'APEX' em peso 900 + mark geométrico do apex de curva à esquerda."
```

**5.7** Tipografia — tem preferência ou deixa o Claude sugerir?
```
Ex: "Display: Barlow Condensed 900 para nomes de carros.
     Corpo: DM Sans. Specs técnicas: Roboto Mono."
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
Ex: "CarQuery API para dados técnicos de carros. Mapbox para o mapa de drives."
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
Ex: "Freemium — funcionalidades básicas gratuitas, plano Apex+ para
     estatísticas avançadas e sem anúncios."
```

**8.2** Como o app ganha dinheiro (se ganhar)?
```
Ex: "Assinatura mensal + parcerias com concessionárias para agendamento
     de test drives."
```

**8.3** Qual o critério de sucesso do MVP?
```
Ex: "100 usuários ativos registrando pelo menos 1 drive por semana."
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