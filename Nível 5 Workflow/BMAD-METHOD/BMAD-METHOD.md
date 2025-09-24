# BMAD-METHOD

[d](https://github.com/bmad-code-org/BMAD-METHOD)

O **BMAD-METHOD** (ou **BMAD-Method**, ou “Breakthrough Method for Agile AI-Driven Development”) é uma metodologia / framework para estruturar o uso de agentes de IA (IA “personificados”) em um fluxo de trabalho ágil e organizado. ([GitHub][1])

Aqui está um panorama mais detalhado:

---

## O que é

- BMAD é uma sigla para **Breakthrough Method for Agile AI-Driven Development**. ([GitHub][1])
- A ideia central é não tratar a IA como uma “caixa preta” ou um único modelo “falar com você”, mas sim organizar múltiplos agentes de IA com papéis (“personas” ou “agentes”) definidos (Analista, Arquiteto, Desenvolvedor, QA, Gerente de Produto, Scrum Master, etc.). ([GitHub][1])
- Cada agente tem responsabilidades específicas, e há um fluxo de trabalho planejado para que eles interajam, se passem contexto (context engineering) e colaborem de forma mais organizada. ([Python in Plain English][2])
- O método tenta mitigar dois grandes problemas em projetos assistidos por IA: **inconsistência no planejamento / especificações** e **perda de contexto** na transição entre etapas de desenvolvimento. ([GitHub][1])

---

## Como funciona (aspectos práticos)

Alguns dos componentes / fases típicas do BMAD:

1. **Planejamento com agentes especializados**

   - O agente “Analyst” ou “Business Analyst” investiga mercado, concorrentes, requisitos de negócio. ([Medium][3])
   - O agente “Architect” define a arquitetura técnica do sistema (camadas, componentes, integração, padrões) ([Medium][3])
   - O agente “PM / Product Manager / PO” elabora PRDs (Product Requirement Documents), épicos, backlog, prioridades ([Medium][3])
   - “Scrum Master” prepara as histórias de usuário de forma que o agente Dev possa implementá-las com clareza de contexto e requisitos. ([GitHub][1])

2. **Desenvolvimento com entrega orientada a histórias**

   - Cada “story” (história de usuário) é preparada de modo que o agente de desenvolvimento (Dev) tenha todo o contexto necessário para executar. ([GitHub][1])
   - O agente QA revisa, testa, propõe verificações de qualidade e validações ao final de cada história ou iteração. ([Medium][4])

3. **Fluxo de entrega consistente e manutenção de contexto**

   - O método busca evitar que agentes em fases posteriores “esqueçam” do que foi decidido anteriormente, mantendo o contexto estruturado (documentos, checagens, passagens claras de artefatos). Isso é parte do “context engineering”. ([Python in Plain English][2])
   - Versões mais novas do BMAD (por exemplo, V2 ou V3) incluem ajustes para otimizar o tamanho dos documentos, usar listas de verificação (“checklists”) e modularizar agentes para melhor performance. ([Cursor - Community Forum][5])

4. **Integração em editores / ferramentas**

   - A instalação do BMAD geralmente cria uma estrutura de arquivos (“.bmad-core”, arquivos Markdown com definição de agentes) que podem ser usados por ferramentas de IA ou ambientes de desenvolvimento. ([Medium][3])
   - Em alguns fluxos, agentes podem ser ativados diretamente no IDE ou em ferramentas de IA (por exemplo, uso de “modes” ou “personas” nos chats de IA) para mudança de contexto. ([Medium][6])

---

## Vantagens esperadas e limitações

**Vantagens / pontos positivos:**

- Mais **organização** e disciplina no uso de IA em projetos complexos, evitando que prompts “soltos” acabem confusos. ([Medium][4])
- Melhora na **consistência de contexto** entre fases (o que é vital em projetos de software com muitos detalhes). ([Python in Plain English][2])
- Reuso de “métodos de pensamento” / “rotinas” de agentes, definidas uma vez e usadas repetidas vezes. ([Medium][4])
- Potencial para acelerar o planejamento e a produção de documentos de arquitetura e requisitos. ([Medium][4])

**Limitações / desafios apontados:**

- Requer configuração inicial relativamente complexa (projeto de agentes, definição de passagens de contexto).
- Pode consumir muitos tokens ou recursos, dependendo de quantos agentes e a quantidade de contexto usado. De fato, alguns usuários relatam alto uso de tokens quando experimentam essa abordagem. ([Reddit][7])
- Ainda não é “mágico” — o BMAD não substitui o julgamento humano, nem produz código totalmente pronto sem supervisão. ([Medium][4])
- Em projetos muito grandes ou com múltiplos módulos interdependentes (microserviços, integrações complexas) pode haver dificuldades para manter a coerência entre agentes de diferentes domínios. ([Medium][4])
- Pode haver sobrecarga de documentação ou duplicação, que versões mais recentes do método tentam mitigar com checklists e modularização. ([Cursor - Community Forum][5])

---
