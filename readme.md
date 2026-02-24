# 🧩 Copiloto Multi-Stack — Ask, Edit, Plan, Agent e Study

![dio/me](https://img.shields.io/badge/dio-me-ff2d55)
![IA](https://img.shields.io/badge/IA-Assistente%20Inteligente-blue)
![Prompt](https://img.shields.io/badge/Prompt-engineering-yellow)
![PHP](https://img.shields.io/badge/Stack-PHP-777BB4?logo=php&logoColor=white)
![.NET](https://img.shields.io/badge/Stack-.NET-512BD4?logo=dotnet&logoColor=white)
![Java](https://img.shields.io/badge/Stack-Java-ED8B00?logo=openjdk&logoColor=white)

O Copiloto oferece diferentes **modos de interação** para você escolher como quer trabalhar: desde **tirar dúvidas sem mexer no código**, até **planejar mudanças maiores** ou **delegar tarefas autônomas**. Os prompts suportam **PHP, .NET (C#) e Java**, além de uma opção **Custom** para qualquer outra linguagem ou framework.

> **Personalidade:** todos os modos operam com a personalidade **J.A.R.V.I.S.** — formal, sofisticado, analítico e preciso.

---

## 🖥️ Seletor de Stack

Todos os prompts possuem um bloco de seleção no topo. Basta marcar `[x]` na linguagem desejada:

```md
- [ ] PHP    → Laravel / Symfony / Slim — PHP 8.x, Composer, PHPUnit
- [ ] .NET   → ASP.NET Core / Minimal API — C# 12, .NET 8, EF Core
- [ ] Java   → Spring Boot / Quarkus — Java 21, Maven/Gradle, JUnit 5
- [ ] Custom → Linguagem: ___ | Framework: ___ (só o nome já basta)
```

> Se nenhuma opção for marcada, o padrão é **Java + Spring Boot**.

---

## ❓ Ask

Modo **somente leitura** — responde dúvidas, explica código e diagnostica erros sem alterar nada.

- Diagnóstico direcionado à linguagem ativa (stack trace PHP · `dotnet-trace` · `jstack`)
- Seção **"WHEN TO ESCALATE"**: se a resposta exigir >3 arquivos, sugere mudar para PLAN ou AGENT
- Links para documentação oficial em cada referência de API
- Máximo de 2 perguntas quando faltar contexto — assume e declara o restante

📄 **Prompt:** [prompts/prompt-ask.md](prompts/prompt-ask.md)

---

## ✏️ Edit

Modo para **alterar código existente**. Selecione um trecho, descreva a mudança e o Copiloto aplica diretamente.

Ideal para: refactors · ajustes de lógica · melhoria de performance · conversão de linguagem · adicionar logs · tratar erros.

📄 **Prompt:** [prompts/prompt-edit.md](prompts/prompt-edit.md)

---

## 🧭 Plan

Modo de **planejamento revisável** — pensa antes de codar. Produz um plano estruturado com:

- 🏷️ **Convenções da stack** (naming, estrutura de pastas, comando de bootstrap)
- ⏱️ **Estimativa de complexidade** por passo: `S / M / L / XL`
- ✅ **Definition of Done** como checklist de critérios de aceite
- 🔄 **Estratégia de rollback** para mudanças de banco ou infra
- Aguarda aprovação explícita antes de gerar qualquer código

📄 **Prompt:** [prompts/prompt-plan.md](prompts/prompt-plan.md)

---

## 🤖 Agent

Modo mais **autônomo** — navega pelo projeto, cria arquivos e modifica múltiplos pontos para atingir um objetivo.

- Regras de stack por ecossistema com comandos reais (`composer install` / `dotnet restore` / `mvn install`)
- Diretivas de DI, ORM, Auth e Segurança para cada linguagem
- Sugere **Conventional Commits** em inglês a cada entrega (`feat:` / `fix:` / `refactor:`)
- Inclui **estratégia de rollback** para mudanças de schema ou infra

📄 **Prompt:** [prompts/prompt-agent.md](prompts/prompt-agent.md)

---

## 📚 Study

Modo de **aprendizado ativo** — ensina conceitos com progressão de nível e prática guiada.

- Progressão explícita: 🟢 Iniciante · 🟡 Intermediário · 🔴 Sênior
- Exemplo mínimo sempre na linguagem da stack ativa
- **Anti-patterns**: erros comuns e o que NÃO fazer
- **Comparativo entre linguagens**: mesmo conceito em PHP, .NET e Java
- **Exercício prático** com dica desbloqueável ("digita 'dica'")
- Checkpoint de compreensão ao final de cada bloco

📄 **Prompt:** [prompts/prompt-study.md](prompts/prompt-study.md)

---

## 🧠 Resumo mental rápido

| Modo | Para quê |
|------|----------|
| **Ask** | Entender, diagnosticar, tirar dúvidas |
| **Plan** | Planejar antes de agir, validar abordagem |
| **Edit** | Mudar código existente |
| **Agent** | Executar tarefas grandes com autonomia |
| **Study** | Aprender ativamente com tutoria guiada |
