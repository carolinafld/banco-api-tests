# banco-api-tests

## 📘 Objetivo
Este projeto realiza testes automatizados na API REST do [banco-api](https://github.com/juliodelimas/banco-api), validando suas funcionalidades e contribuindo a qualidade de suas operações.

Os testes foram desenvolvidos em **JavaScript**, utilizando o framework **Mocha** e as bibliotecas **Chai** e **Supertest**, entre outras, para estruturar, executar e validar os cenários de teste de forma eficiente.

## 🧰 Stack Utilizada
- **Linguagem:** JavaScript (Node.js)
- **Framework de testes:** [Mocha](https://mochajs.org/)
- **Biblioteca de asserções:** [Chai](https://www.chaijs.com/)
- **Biblioteca de requisições HTTP:** [Supertest](https://github.com/visionmedia/supertest)
- **Relatórios:** [Mochawesome](https://github.com/adamgruber/mochawesome)
- **Gerenciador de variáveis de ambiente:** [dotenv](https://github.com/motdotla/dotenv)

## 🗂️ Estrutura de Diretórios
```
banco-api-tests/
├── test/               # Testes organizados por funcionalidades
│   ├── login.test.js
│   └── transferencias.test.js
├── mochawesome-report/ # Diretório gerado automaticamente com o relatório HTML dos testes
├── .env                # Arquivo para configuração da variável BASE_URL
├── .gitignore
├── package.json
└── README.md
```

## ⚙️ Arquivo `.env`
Antes de rodar os testes, crie um arquivo chamado `.env` na raiz do projeto com o seguinte conteúdo:

```env
BASE_URL=http://localhost:3000
```

Substitua `http://localhost:3000` pela URL onde a API **banco-api** está rodando.

> 🔹 A variável **BASE_URL** deve conter o endpoint base da API que será testada.


## ▶️ Comandos para execução

### 1️⃣ Instale as dependências
```bash
npm install
```

### 2️⃣ Execute todos os testes
```bash
npm test
```

### 3️⃣ Geração automática do relatório HTML:
O relatório em HTML será automaticamente gerado no diretório `mochawesome-report` após a execução dos testes com `npm test`.

Sugestão: para executar os testes e abrir o relatório HTML automaticamente, adicione um script no package.json:
```bash
"scripts": {
  "test:report": "npm test && open mochawesome-report/mochawesome.html"
}
```
(Em Windows, substitua open por start.)

Para visualizar o relatório:
- Abra o arquivo `mochawesome-report/mochawesome.html` em seu navegador.


## 📄 Documentações das Dependências

- [Mocha](https://mochajs.org/#getting-started)  
- [Chai](https://www.chaijs.com/guide/)  
- [Supertest](https://github.com/visionmedia/supertest#readme)  
- [Mochawesome](https://github.com/adamgruber/mochawesome)  
- [dotenv](https://github.com/motdotla/dotenv#readme)
