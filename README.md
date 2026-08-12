# meu-projeto_backend
# Backend com Express e TypeScript

Este projeto apresenta a configuração de um ambiente backend utilizando **Node.js, TypeScript e Express**, desde a preparação do ambiente até a execução de um servidor web.

## Preparação do ambiente

Para iniciar o projeto, execute os seguintes comandos no terminal:

```bash
npm init -y
npm i -D typescript @types/node tsx
npx tsc --init
```

## Instalação do Express

Para preparar o framework Express, execute:

```bash
npm install express
npm install -D @types/express
```

## Estrutura do projeto

Crie uma pasta `src` e, dentro dela, o arquivo `app.ts`.

A estrutura ficará assim:

```text
meu-projeto-backend/
├── node_modules/
├── src/
│   └── app.ts
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
└── tsconfig.json
```

## Criando o servidor com Express

No arquivo `src/app.ts`, adicione o seguinte código:

```typescript
// Importa a biblioteca Express e também o tipo Express
// O Express será utilizado para criar o servidor web
import express from "express";
import type { Express } from "express";

// Cria uma aplicação Express
// A função express() devolve um objeto que representa o servidor da aplicação
const app: Express = express();

// Define a porta onde o servidor ficará disponível
// Neste caso, o servidor poderá ser acessado pela porta 8081
const PORT: number = 8081;

// Inicializa o servidor utilizando a porta definida
// O método listen() faz o servidor começar a "escutar" requisições HTTP
app.listen(PORT, () => {
    console.log(`Servidor rodando em http://localhost:${PORT}`);
});
```

### Funcionamento do código

* `express` importa a biblioteca Express.
* `Express` define o tipo utilizado pela aplicação.
* `express()` cria a aplicação do servidor.
* `PORT` define a porta `8081`.
* `app.listen()` inicia o servidor.
* `console.log()` informa no terminal que o servidor foi iniciado.

## Configurando o script de execução

Abra o arquivo `package.json` e configure a seção `"scripts"`:

```json
"scripts": {
    "dev": "tsx watch src/app.ts"
}
```

O comando `tsx watch` permite executar o arquivo TypeScript e reiniciar automaticamente o servidor sempre que houver alterações no código.

## Executando o servidor

No terminal, execute:

```bash
npm run dev
```

Se tudo estiver configurado corretamente, o terminal exibirá:

```text
Servidor rodando em http://localhost:8081
```

O servidor estará disponível no endereço:

**[http://localhost:8081](http://localhost:8081)**

## Tecnologias utilizadas

* **Node.js** — ambiente de execução.
* **TypeScript** — linguagem utilizada no desenvolvimento.
* **Express** — framework utilizado para criação do servidor.
* **TSX** — ferramenta utilizada para executar arquivos TypeScript.
* **npm** — gerenciador de pacotes.

---

**Desenvolvido por Arthur Sudário Bonatto Reis**
