# Linter-Code

Este é um projeto de configuração e integração de linters para as linguagens Python e JavaScript. O objetivo deste projeto é garantir que o código do repositório esteja formatado corretamente e siga as melhores práticas de cada linguagem.

## Estrutura do Projeto

A estrutura do projeto é a seguinte:

Linter-Code/ 

│ 

├── node_modules/            # Dependências do Node.js 

├── src/ 

│   ├── python/              # Código Python 

│   └── javascript/          # Código JavaScript 

├── .github/                 # Arquivos de configuração do GitHub Actions 

├── .pylintrc                # Configuração do pylint para Python 

├── eslint.config.mjs        # Configuração do eslint para JavaScript 

├── package-lock.json        # Bloqueio das versões do npm 

├── package.json             # Arquivo de dependências e scripts do npm 

└── README.md                # Este arquivo de documentação

## Instalação

### Pré-requisitos

Certifique-se de ter os seguintes softwares instalados no seu sistema:

- [Node.js](https://nodejs.org/) (para rodar o linter JavaScript)
- [Python](https://www.python.org/downloads/) (para rodar o linter Python)
- [npm](https://www.npmjs.com/) (gerenciador de pacotes para o Node.js)

### Instalação do Projeto

1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/linter-code.git

2. Navegue para o diretório do projeto:
   
   ```bash
   cd linter-code


3. Instale as dependências:

   ```bash
   npm install


4. Instale as dependências do Python (caso ainda não tenha o pylint instalado):

   ```bash
   pip install pylint


Como Usar

Linter para Python

Para rodar o linter Python, execute o seguinte comando:

    python -m pylint src/python

Ou, se você preferir rodar via npm:

    npm run lint:python

Linter para JavaScript

Para rodar o linter JavaScript, execute o seguinte comando:

    npx eslint src/javascript

Ou, se você preferir rodar via npm:

    npm run lint:javascript

O ESLint será executado conforme a configuração do arquivo eslint.config.mjs, que define as regras de linting para o JavaScript.

Integração Contínua (CI)

Este projeto está configurado com GitHub Actions para rodar automaticamente o linting em cada pull request. Os linters Python e JavaScript são executados conforme configurado nos workflows no diretório .github/workflows.

Como Funciona a Integração Contínua (CI)

O workflow de integração contínua foi configurado dentro da pasta .github/workflows para garantir que o código enviado ao repositório esteja sempre validado pelos linters, sem precisar de ação manual.

O GitHub Actions executa as configurações do pylint para Python e eslint para JavaScript toda vez que um pull request é criado, ou uma mudança é feita no repositório.


Exemplos de Fluxos de Trabalho:

1. Quando alguém cria um pull request ou faz push para o repositório, o GitHub Actions executa o CI para rodar o linter de Python e JavaScript.


2. Se houver erros ou alertas de estilo, eles serão registrados nos logs da execução do CI, e o pull request pode ser impedido de ser mesclado até que os problemas sejam resolvidos.
