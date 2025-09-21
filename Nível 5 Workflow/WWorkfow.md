## **Workflow de Dev com IA**

### **Objetivo**

Construir um **workflow completo** que use IA para automatizar **planejamento, desenvolvimento, testes, revisão, deploy e manutenção** de um projeto real (ex.: gerenciador de tarefas).

---

### **Etapas do Workflow**

1. **Planejamento**

    - **Ferramentas/IA**: Zen MCP, Context7
    - **Uso**: Criar PRD (Product Requirements Document) e especificações iniciais a partir de prompts e contextos armazenados.
    - **Exemplo**: Gerar lista de features do gerenciador de tarefas (CRUD, notificações, categorias).

2. **Arquitetura**

    - **Ferramentas/IA**: FigmaMCP, ShadCN MCP
    - **Uso**: Criar protótipos de UI e estrutura de front-end/back-end.
    - **Exemplo**: Protótipo visual da interface web do gerenciador de tarefas e diagrama de APIs.

3. **Desenvolvimento**

    - **Ferramentas/IA**: Spec Kit, Super claude
    - **Uso**: Gerar código backend, frontend e integrações automaticamente a partir de especificações.
    - **Exemplo**: Criar API REST com rotas CRUD, frontend React e integração com banco de dados.

4. **Testes**

    - **Ferramentas/IA**: MCP Playwright, Serena
    - **Uso**: Criar e executar testes automatizados (unitários, end-to-end).
    - **Exemplo**: Testar funcionalidades de adicionar, editar e deletar tarefas.

5. **Review / Revisão de Código**

    - **Ferramentas/IA**: CodeRabbit
    - **Uso**: Revisar PRs automaticamente, sugerir melhorias de código, identificar problemas de estilo, performance ou lógica.
    - **Exemplo**: Validar PR do gerenciador de tarefas antes do merge, garantindo que todas as funcionalidades estão corretas e consistentes.

6. **Documentação**

    - **Ferramentas/IA**: Context7, Claude Code
    - **Uso**: Gerar documentação técnica e guias para usuários automaticamente.
    - **Exemplo**: Documentação da API, instruções de uso da UI e notas de release.

7. **Deploy**

    - **Ferramentas/IA**: Spec Kit + agentes
    - **Uso**: Automatizar deploy em ambientes de staging e produção.
    - **Exemplo**: Deploy do gerenciador de tarefas em um host cloud.

8. **Monitoramento**

    - **Ferramentas/IA**: Serena, Context7
    - **Uso**: Coletar logs, métricas de performance e alertas de erro.
    - **Exemplo**: Monitorar erros de tarefas não salvas e performance do backend.

9. **Manutenção / Feedback Loop**

    - **Uso**: Atualizar features, corrigir bugs e refinar prompts para IA.
    - **Exemplo**: Melhorar prompts para geração de código, adicionar novas funcionalidades no gerenciador de tarefas.

---

### **Resumo Visual do Loop**

```
PRD (Non-tech) -> TechSpec -> Tasks -> Dev (Spec Kit/Claude Code) -> Testes -> Review (CodeRabbit) -> Deploy
       ↑-------------------------------------------------------------------------------↓
                       Feedback Loop (Monitoramento + Manutenção)
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
