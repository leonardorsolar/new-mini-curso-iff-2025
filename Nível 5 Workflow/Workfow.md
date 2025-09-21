## **Workflow de Dev com IA**

### **Objetivo**

Construir um **workflow completo** que use IA para automatizar **planejamento, desenvolvimento, testes, revisão, deploy e manutenção** de um projeto real (ex.: gerenciador de tarefas).

---

**Para iniciantes**:

1. Comece com **Context7** para organizar ideias
2. Use **Spec Kit** para transformar ideias em especificações técnicas
3. Experimente **Cursor** para gerar código automaticamente
4. Teste com **MCP Playwright** para verificar se funciona
5. Conforme ganhar experiência, adicione as outras ferramentas ao workflow

### **Resumo Visual do Loop**

```
PRD (Context7/Zen MCP) -> TechSpec (Spec Kit) -> Design (ShadCN/v0) -> Código (Cursor/Windsurf) -> Testes (Playwright) -> Review (CodeRabbit) -> Deploy (Vercel/Railway) -> Monitoramento (Serena)
       ↑--------------------------------------------------------------------------------------------------------------------------------------------------------↓
                                                           Feedback Loop (Melhorias contínuas)
```

### **Etapas do Workflow avançado**

1. **Planejamento**

    - **Ferramentas/IA**: Context7, Zen MCP
    - **Uso**: Criar PRD (Product Requirements Document) e especificações iniciais usando contexto armazenado.
    - **Exemplo**: Definir funcionalidades do gerenciador de tarefas (criar, editar, deletar tarefas, categorias).
    - **Links**:
        - Context7: https://github.com/upstash/context7
        - Zen MCP: https://github.com/BeehiveInnovations/zen-mcp-server

2. **Especificação Técnica**

    - **Ferramentas/IA**: Spec Kit, Context7
    - **Uso**: Converter o PRD em especificações técnicas detalhadas (APIs, banco de dados, arquitetura).
    - **Exemplo**: Transformar "gerenciar tarefas" em especificações de endpoints REST, modelos de dados e fluxos.
    - **Link**: https://github.com/specmatic/specmatic-mcp-sample-with-spec-kit

3. **Design/Prototipagem**

    - **Ferramentas/IA**: ShadCN MCP, v0 by Vercel
    - **Uso**: Criar componentes de UI padronizados e protótipos visuais.
    - **Exemplo**: Montar interface com botões, formulários e cards para as tarefas.
    - **Links**:
        - ShadCN MCP: https://ui.shadcn.com/docs/mcp
        - v0: https://v0.dev

4. **Desenvolvimento**

    - **Ferramentas/IA**: Cursor AI, Claude code, Codeium, Windsurf
    - **Uso**: Gerar código backend, frontend e integrações automaticamente a partir de especificações.
    - **Exemplo**: Criar API REST com rotas CRUD, frontend React e integração com banco de dados.

5. **Testes**

    - **Ferramentas/IA**: MCP Playwright, Serena
    - **Uso**: Criar e executar testes automatizados (unitários, end-to-end).
    - **Exemplo**: Testar se consegue adicionar uma nova tarefa e se ela aparece na lista.
    - **Links**:
        - MCP Playwright: https://github.com/microsoft/playwright-mcp
        - Serena: https://github.com/oraios/serena

6. **Review / Revisão de Código**

    - **Ferramentas/IA**: CodeRabbit, SonarQube AI
    - **Uso**: Revisar PRs automaticamente, sugerir melhorias de código, identificar problemas de estilo, performance ou lógica.
    - **Exemplo**: Validar PR do gerenciador de tarefas antes do merge, garantindo que todas as funcionalidades estão corretas e consistentes.
    - **Links**:
        - CodeRabbit: https://coderabbit.ai
        - SonarQube: https://www.sonarsource.com

7. **Documentação**

    - **Ferramentas/IA**: Context7, Mintlify, GitBook AI
    - **Uso**: Gerar documentação técnica e manuais automaticamente.
    - **Exemplo**: Criar guia de como usar a API e manual do usuário.
    - **Links**:
        - Mintlify: https://mintlify.com
        - GitBook: https://www.gitbook.com

8. **Deploy**

    - **Ferramentas/IA**: Vercel AI, Railway, GitHub Actions
    - **Uso**: Automatizar deploy em ambientes de staging e produção.
    - **Exemplo**: Publicar o gerenciador de tarefas automaticamente quando código é aprovado.
    - **Links**:
        - Vercel: https://vercel.com
        - Railway: https://railway.app
        - GitHub Actions: https://github.com/features/actions

9. **Monitoramento**

    - **Ferramentas/IA**: Serena, Context7, DataDog AI
    - **Uso**: Coletar logs, métricas de performance e alertas de erro. Acompanhar performance, erros e uso do sistema com análise inteligente.
    - **Exemplo**: Monitorar erros de tarefas não salvas e performance do backend. Receber alertas se muitos usuários não conseguem salvar tarefas.
    - **Links**:
        - Serena: https://github.com/oraios/serena
        - DataDog: https://www.datadoghq.com

10. **Manutenção / Feedback Loop**

    - **Uso**: Atualizar features, corrigir bugs e refinar prompts para IA.
    - **Exemplo**: Melhorar prompts para geração de código, adicionar novas funcionalidades no gerenciador de tarefas, Adicionar função de lembrete nas tarefas baseado no feedback dos usuários.

---

### **Resumo Visual do Loop**

```
PRD (Context7/Zen MCP) -> TechSpec (Spec Kit) -> Design (ShadCN/v0) -> Código (Cursor/Windsurf) -> Testes (Playwright) -> Review (CodeRabbit) -> Deploy (Vercel/Railway) -> Monitoramento (Serena)
       ↑--------------------------------------------------------------------------------------------------------------------------------------------------------↓
                                                           Feedback Loop (Melhorias contínuas)
```

-   **PRD (Non-tech)**: documento inicial de requisitos simples.
-   **TechSpec**: especificações técnicas detalhadas geradas via IA.
-   **Tasks**: tarefas geradas automaticamente para Devs.
-   **Dev**: código gerado automaticamente com Spec Kit ou Claude Code.
-   **Testes**: execução automatizada com MCP Playwright e Serena.
-   **Review**: CodeRabbit revisa PRs e sugere melhorias.
-   **Deploy**: entrega em produção.
-   **Feedback Loop**: manutenção contínua baseada em métricas, logs e melhorias de prompts.

---

https://github.com/BeehiveInnovations/zen-mcp-server
https://github.com/upstash/context7
https://ui.shadcn.com/docs/mcp
https://github.com/specmatic/specmatic-mcp-sample-with-spec-kit
https://github.com/SuperClaude-Org/SuperClaude_Framework
https://github.com/microsoft/playwright-mcp
https://github.com/oraios/serena

### **Explicação das Ferramentas Principais**

**Context7**: Armazena conversas e contexto para reutilizar em projetos futuros. É como ter uma "memória" das suas ideias e decisões.

**Zen MCP**: Facilita a criação de PRDs estruturados e organizados, transformando ideias soltas em documentos profissionais.

**Spec Kit**: Converte PRDs em especificações técnicas detalhadas (APIs, banco de dados, arquitetura), como um "tradutor" de requisitos de negócio para linguagem técnica.

**ShadCN MCP**: Biblioteca de componentes visuais prontos (botões, formulários, etc.) que se integra com IA para criar interfaces rapidamente.

**Cursor/Windsurf**: Editores de código com IA integrada que escrevem código automaticamente baseado nas especificações.

**MCP Playwright**: Automação de testes que simula um usuário real usando seu site/app, verificando se tudo funciona corretamente.

**CodeRabbit**: Revisor automático de código que encontra bugs, problemas de segurança e sugere melhorias.

**Serena**: Sistema de monitoramento que usa IA para analisar logs e alertar sobre problemas no seu sistema.
