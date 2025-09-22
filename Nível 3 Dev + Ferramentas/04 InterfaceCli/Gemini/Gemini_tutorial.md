# Roteiro: Introdução ao Gemini CLI no Projeto React

## O que é o Gemini CLI?

O **Gemini CLI** é um agente de inteligência artificial open-source da Google que permite acessar os modelos Gemini diretamente pelo terminal.  
Ele pode:

- Escrever e revisar código
- Corrigir bugs
- Gerar conteúdo
- Fazer buscas na web
- Manipular arquivos e executar comandos do sistema

Tudo isso usando linguagem natural ([Google Cloud][1], [The Verge][2], [Indiatimes][3]).

**Vantagens principais**:

- Modelos avançados, como o **Gemini 2.5 Pro**, com contexto de até 1 milhão de tokens
- Gratuito para uso com conta Google pessoal (60 requisições/min e até 1.000/dia) ([blog.google][4])
- Extensível com ferramentas internas (Google Search, MCP, Veo/Imagen)
- Full open-source (licença Apache 2.0) — ideal para personalizar e contribuir ([GitHub][5])

---

- **Gemini CLI** → interface para enviar comandos.
- **LLM Gemini** → interpreta, gera respostas e pode executar “agentes internos” para tarefas

## 🌱 Gemini CLI e "agentes internos"

1. **Você envia um comando ou prompt** pelo CLI.
2. **O LLM Gemini interpreta** o que você quer.
3. Dependendo do tipo de prompt e do ambiente (ex: VS Code), o Gemini pode **acionar funcionalidades internas do modelo** que são como mini-agentes:

   - Autocompletar código.
   - Refatorar arquivos.
   - Gerar funções ou testes.

4. Esses “agentes internos” **não são processos separados** rodando no seu computador.

   - Eles são **sub-rotinas do próprio LLM** que decidem os passos para cumprir sua tarefa.
   - O modelo faz a análise do que precisa fazer e devolve o resultado, às vezes com múltiplos passos “internos”.

---

## Como instalar

### 1. Pré-requisitos

- **Node.js** ≥ 18 ([milvus.io][6], [DataCamp][7])
- Acesso ao **terminal** (Linux/Ubuntu) ([Google Codelabs][8])

### 2. Instalação

#### a) Via npx (sem instalação permanente)

```bash
npx https://github.com/google-gemini/gemini-cli
```

> Isso abre o Gemini CLI na pasta atual do projeto, podendo ler e editar os arquivos.

#### b) Via npm (instalação global)

```bash
npm install -g @google/gemini-cli
```

#### c) Alternativa via Homebrew (macOS/Linux)

```bash
brew install gemini-cli
```

### 3. Executar o Gemini CLI

```bash
gemini
```

> Na primeira execução, você escolherá tema visual e método de autenticação.

---

## Autenticação e uso gratuito

- Faça login com **conta Google pessoal**:

  - 60 requisições por minuto
  - 1.000 requisições por dia ([blog.google][4])

- Para limites maiores ou modelos específicos:

  1. Gere **API Key** no **Google AI Studio**
  2. Exporte como variável de ambiente:

  ```bash
  export GEMINI_API_KEY="SUA_CHAVE"
  ```

## Como usar no terminal interativo

1. Digite `gemini` no terminal.
2. Converse usando linguagem natural, por exemplo:

digite

```text
 @Nível\ 3\ Dev\ +\ Ferramentas/04\ InterfaceCli/Teste\ Prático.md
```

Outros exemplos:

```text
Analise este código e me diga o que ele faz: @meu_codigo.py
```

```text
Explique o que o arquivo App.js faz neste projeto.
```

depois

```text
Resuma o funcionamento do TaskForm.jsx em poucas palavras.
```

### Comandos úteis

- `/help` → lista comandos disponíveis
- `/quit` ou `Ctrl+C` → sair do modo interativo

No Gemini CLI, a barra / inicia os comandos para interagir com o agente e ferramentas, como /tools para listar ferramentas disponíveis ou /mcp para gerir servidores MCP.

Comandos:
https://github.com/google-gemini/gemini-cli/blob/main/docs/cli/commands.md

### Exemplos de uso

- Rodar o programa: `npm start`
- Pedir melhorias (refatoração)
- Editar arquivos:

```text
@src/App.js refatore este arquivo e inclua um título
@src/components/TaskForm.js refatore e adicione um design mais moderno
```

> Após o Gemini sugerir mudanças, você escolhe:
> 1- Yes, allow once
> 2- Yes, allow always
> 3- No

---

## 📌 O que o `init` faz

Quando você roda:

```bash
gemini init
```

O CLI:

1. **Escaneia o projeto** (arquivos `.md`, `.json`, `.js`, `.py`, etc.).
2. **Gera um arquivo `GEMINI.md`** com:

   - Contexto do projeto.
   - Estrutura de pastas.
   - Sugestões de como usar o Gemini para aquele projeto.
   - Configuração inicial para IA entender os objetivos.

3. Esse arquivo pode ser editado por você para **personalizar as instruções** (por exemplo: “use Node.js”, “arquitetura em camadas”, “padrão MVC”).

E rode:

```bash
gemini init
```

Isso vai gerar um **`GEMINI.md`** nessa pasta.
👉 A partir daí, sempre que você usar o **Gemini CLI**, ele já vai ler esse `GEMINI.md` como **contexto inicial** junto com seus arquivos.

## GEMINI.md

O **GEMINI.md** é um arquivo que fornece instruções fixas ao Gemini CLI. Ele é lido automaticamente dentro da pasta do projeto.

### Como criar

**Maneira 1:** criar arquivo no diretório raiz com descrição do projeto e instruções didáticas.

**Maneira 2:** usar terminal:

```bash
cd frontend-react
nano GEMINI.md
```

Exemplo de conteúdo para um projeto React de tarefas:

```markdown
# Contexto

Este é um projeto em React chamado **Gestão de Tarefas**.
O aplicativo permite:

- Criar novas tarefas
- Listar tarefas existentes
- Atualizar tarefas
- Excluir tarefas

# Regras para o Gemini

- Explique o código de forma didática, como se fosse para alunos iniciantes
- Sugira boas práticas de React (hooks, componentização, estilos)
- Use código limpo e comentado
- Prefira exemplos simples que os alunos possam entender

# Objetivos

Este projeto será usado em aulas de programação para ensinar:

- React básico
- Consumo de serviços (taskService)
- Uso de IA como apoio no desenvolvimento
```

> Salve o arquivo e rode `gemini` dentro da pasta. O CLI seguirá o contexto definido.

---

## Atividade complementares:

1. Perguntar ao Gemini como funciona o `useState` no React.
2. Pedir que sugira uma nova feature para o app.
3. Implementar a sugestão no código com ajuda do Gemini.
4. Rodar o projeto e validar a mudança:

```bash
npm start
```

# vídeo:

https://www.youtube.com/watch?v=0oHbRWy64sU

# 🚀 **Tutorial: Usando o Gemini CLI para Resolver um Desafio**

## 1. Entrar na pasta do projeto

No terminal, vá até a pasta onde está seu desafio:

```bash
cd "Nível 3 Dev + Ferramentas/04 InterfaceCli"
```

---

## 2. Iniciar o Gemini no projeto (opcional, mas recomendado)

Crie um `GEMINI.md` com contexto inicial:

```bash
gemini init
```

👉 Isso ajuda o Gemini a entender a estrutura do seu projeto.

---

## 3. Abrir o chat com o Gemini

Inicie uma sessão interativa:

```bash
gemini chat
```

---

## 4. Incluir o arquivo do desafio

Carregue o enunciado para o contexto da IA:

```bash
/file "Teste Prático.md"
```

Você pode confirmar se foi carregado:

```bash
/files
```

---

## 5. Pedir a solução em código

Agora é só dar instruções. Por exemplo:

```
Gere a solução completa do Teste Prático.md em HTML, CSS e JavaScript puro.
Use localStorage para salvar os dados.
```

Ou mais específico:

```
Crie apenas o esqueleto inicial do projeto em Node.js com Express.
```

---

## 6. Refinar o código

Peça ajustes iterativos:

```
Adicione comentários explicando cada parte do código.
```

```
Refatore para separar em camadas (controller, service, repository).
```

```
Gere testes unitários para a função principal.
```

---

## 7. Finalizar

Quando terminar, salve o código que o Gemini gerar no seu editor.
E se quiser encerrar o chat:

```bash
/exit
```

---

# 📌 Resumindo o fluxo

1. `cd pasta` → entrar no projeto
2. `gemini init` → criar contexto inicial (opcional)
3. `gemini chat` → abrir sessão interativa
4. `/file "Teste Prático.md"` → carregar enunciado
5. Dar prompts → pedir o código
6. `/exit` → sair
