## 1- AI_GUIDE.md: **documentação de referência de arquitetura para a IA**

## 2-task_1.md e task_2.md: **documentação de referência para realização da tarefa pela IA**

Aqui está a versão já pronta para **copiar/colar no Cursor IDE** como contexto, em dois arquivos: `@tasks/task_1.md` (backend) e `@tasks/task_2.md` (frontend).

Criando novas tasks:

# Prompt Dev:

```bash
Leia a tarefa descrita em tasks/task_1.md e implemente o que está sendo pedido.
Caso necessário, use também informações de docs/AI_GUIDE.md
```

Você também pode usar @ para referenciar arquivos dentro do chat.
Exemplo dentro do Cursor:

```bash
Implemente a tasks/task_1.md com base em @docs/AI_GUIDE.md e @QA/QA_MANUAL_TESTS.md
```

## 3- Manual de Testes - Sistema de Tarefas

# Prompt QA: modelo melhores: o3 gemini gpt5 - > cursor com gpt5

```bash
A minha tarefa X foi realizada no front e no backen. Agora gere um arquivo para mim com os testes manuais que o QA deveria fazer para garantir a integridade desse software. O arquivo pode ficar na raiz do projeto.
```
