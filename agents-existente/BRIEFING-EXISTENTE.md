# Briefing — Projeto Existente

> Preencha este arquivo antes de rodar os agentes de auditoria.
> Foque no estado atual — não no que foi planejado originalmente.

---

## Identificação

**Nome do app:** ___________
**Versão atual:** ___________
**Em produção desde:** ___________
**Plataformas:** ___________

---

## Estado atual

**1. O que já foi construído e está funcionando?**
```
[liste as features que existem e funcionam]
```

**2. O que foi planejado mas não foi implementado?**
```
[features que ficaram no backlog]
```

**3. O que foi implementado mas foi abandonado ou removido?**
```
[features que existiram e foram retiradas, e por quê]
```

**4. O que mudou de direção desde o início?**
```
[decisões que foram revertidas ou pivotadas]
```

---

## Usuários

**5. Quantos usuários ativos tem hoje?**
```
```

**6. Qual feature os usuários mais usam?**
```
```

**7. Qual feature os usuários mais reclamam ou pedem?**
```
```

**8. Tem feedback qualitativo relevante (reviews, entrevistas, suporte)?**
```
[cole aqui ou resuma]
```

---

## Produto

**9. O que está funcionando bem e você não quer mexer?**
```
```

**10. O que você removeria do app hoje se pudesse?**
```
```

**11. Qual a maior dívida de produto hoje?**
```
[decisão passada que está te atrapalhando]
```

**12. O que você quer evoluir neste ciclo?**
```
[as 3-5 coisas mais importantes para fazer agora]
```

**13. O que está explicitamente fora do escopo desta evolução?**
```
[o que não vai mudar agora, mesmo que seja importante]
```

---

## Identidade

**14. O nome ainda faz sentido para o produto que o app virou?**
```
[ ] Sim, mantém
[ ] Precisa de ajuste
[ ] Não faz mais sentido
Observação: ___________
```

**15. O tom de voz está sendo aplicado de forma consistente no produto?**
```
[ ] Sim
[ ] Parcialmente — onde está inconsistente?
[ ] Não
```

**16. Tem algum copy que te incomoda no produto atual?**
```
[telas, mensagens, CTAs que parecem errados]
```

---

## Design

**17. O sistema de design está sendo seguido? (tokens, componentes, espaçamento)**
```
[ ] Sim, tudo usando tokens semânticos
[ ] Parcialmente — tem hardcoded / primitivos diretos
[ ] Não, muita inconsistência
```

**18. Tem algum componente visualmente inconsistente ou fora do padrão?**
```
[lista os componentes problemáticos]
```

**19. O dark mode está funcionando corretamente em todas as telas?**
```
[ ] Sim
[ ] Parcialmente — onde quebra?
[ ] Não implementado
```

**20. Tem alguma violação de contraste (WCAG) conhecida?**
```
[lista se souber]
```

---

## Arquitetura

**21. Qual a stack atual com versões reais?**
```
Framework: ___________
Backend/BaaS: ___________
Banco: ___________
Outras dependências relevantes: ___________
```

**22. Tem alguma dependência desatualizada ou com problema de segurança?**
```
```

**23. Qual a maior dívida técnica hoje?**
```
[o que mais te atrapalha no código]
```

**24. Tem queries lentas ou problemas de performance conhecidos?**
```
```

**25. O RLS está implementado em todas as tabelas?**
```
[ ] Sim, todas
[ ] Parcialmente — quais faltam?
[ ] Não
```

**26. As fontes estão self-hosted (woff2 local)?**
```
[ ] Sim
[ ] Não — usando Google Fonts ou CDN
```

---

## Ecossistema (se aplicável)

**27. Este projeto faz parte de um ecossistema com outros projetos?**
```
[ ] Sim — quais outros projetos compartilham tokens/componentes?
[ ] Não
```

**28. O `design-tokens-global.css` está importado e sendo usado como base?**
```
[ ] Sim
[ ] Não — tem tokens próprios desconectados do global
[ ] Parcialmente
```

**29. A camada de produto está definida (--structural, tokens específicos)?**
```
[ ] Sim — qual o --structural deste produto?
[ ] Não definida
```

---

## Destino de desenvolvimento

**30. Qual ferramenta será usada para implementar as mudanças deste ciclo?**
```
[ ] Claude Code no VS Code
[ ] Figma Make
[ ] Ambos
```
