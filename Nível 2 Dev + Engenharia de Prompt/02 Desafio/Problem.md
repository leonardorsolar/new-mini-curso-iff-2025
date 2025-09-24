## descrição da tarefa

Existe o botão "Gerenciar Tarefas" no painel principal, visível apenas para usuários logados.
Ao clicar, o usuário é direcionado para uma tela dedicada de gerenciamento de tarefas (TODOs).
Essa tela deve fornecer uma interface completa de CRUD, permitindo criar, listar, editar, marcar como concluída/não concluída e excluir tarefas.

---

## Requisitos Funcionais da tarefa

- Exibir um botão/card "Gerenciar Tarefas" no painel principal, seguindo o padrão visual existente.
- Clicar no botão deve navegar para a tela de gerenciamento de tarefas (CRUD).
- A tabela/lista de tarefas deve conter as colunas/campos:

  - _Título_
  - _Descrição_
  - _Data de criação_
  - _Criado por_
  - _Status_ (Concluída/Não concluída, com toggle)
  - _Ações_: Editar, Excluir

- Disponibilizar um campo de busca para filtrar tarefas pelo título.
- Disponibilizar um botão "Adicionar Tarefa".
- O botão "Adicionar Tarefa" deve abrir um formulário com os campos:

  - _Título_ (obrigatório, mínimo 3 caracteres)
  - _Descrição_ (opcional)

- A ação "Editar" deve abrir o mesmo formulário preenchido com os dados da tarefa.
- A ação "Excluir" deve solicitar confirmação antes da remoção.
- A tabela deve ser atualizada automaticamente após qualquer operação de CRUD.

---

## Comportamentos Esperados (Expected Behaviors)

- O botão "Gerenciar Tarefas" aparece no painel principal e segue o estilo dos outros cards.
- Ao clicar no botão, o usuário acessa a tela de gerenciamento de tarefas.
- A lista exibe todas as tarefas com os campos especificados.
- A busca filtra as tarefas pelo título.
- O formulário de adicionar/editar valida o campo obrigatório "Título".
- O toggle de status marca a tarefa como concluída/não concluída em tempo real.
- As ações de editar e excluir funcionam corretamente e atualizam a lista.
- Mensagens de sucesso ou erro são exibidas em todas as operações.
- Somente usuários logados podem acessar essa funcionalidade.

---

## Diretrizes Técnicas (Technical Guidelines)

- Reutilizar o componente de formulário existente para adicionar/editar tarefas, adaptando-o conforme necessário.
- Seguir os padrões visuais e de navegação já utilizados no painel principal.
- Garantir validação de campos obrigatórios no frontend e backend.
- Restringir acesso à tela apenas para usuários autenticados.
- As tarefas criadas devem ser persistidas no banco de dados e refletidas em tempo real na lista.

---

## Critérios de Aceite (Acceptance Criteria)

- O botão "Gerenciar Tarefas" está visível no painel principal.
- O botão leva para a tela CRUD de tarefas.
- A lista mostra Título, Descrição, Data de criação, Criado por, Status e Ações.
- A busca por título funciona corretamente.
- O formulário de adicionar/editar valida o campo obrigatório "Título" (mín. 3 caracteres).
- O toggle de status funciona e atualiza a lista.
- Editar e excluir tarefas funciona corretamente e a lista é atualizada.
- Mensagens de sucesso/erro aparecem em todas as ações.
- Apenas usuários logados têm acesso à tela.
