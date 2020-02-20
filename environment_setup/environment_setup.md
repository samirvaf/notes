## Environment Setup (NodeJS, VS Code, Docker, Terminal)

> Extensões VS Code
- Dracula (theme)
- Material Icons

> Plugins VS Code
- Color Highlight
- Editor Config
- Eslint
- Prettier
- Rocketseat Snippets (procurar por rocketseat apenas)

> Terminal
- https://draculatheme.com/

> Extensões Chrome
- React Developer Tools

> Tools
- Insomnia
- DevDocs

> Instalando Node JS
- https://github.com/nvm-sh/nvm
- `nvm install {version}` -> Instala uma versão específica do nodejs
- https://nodejs.org/en/ -> Acessar para encontrar a versão a ser instalada
- `nvm alias default {version}` -> Marca a versão como default

> Instalando Yarn
- https://classic.yarnpkg.com/en/docs/install#debian-stable
- `yarn init {nome do projeto}`

> Instalando Nodemon
- `yarn add nodemon -D`

> Instalando Docker e criando novo container com Postgres
- https://docs.docker.com/v17.09/engine/installation/linux/docker-ce/ubuntu/
- https://hub.docker.com/_/postgres
- `docker run --name {nome do container} -e POSTGRES_PASSWORD={senha do BD} -p {porta na máquina:5432} -d postgres` ->  Para criar um novo container com postgres
- `docker start {nome do container}` -> Inicializar um container já criado
- `docker ps -a` -> Mostra todos os containers criados na máquina
- `docker logs {nome do container}` -> Mostra logs do container
- https://www.electronjs.org/apps/postbird -> Aplicação pra ver os dados no BD

> Instalando ESLint
- `yarn add eslint -D`
- `yarn eslint --init`
- Check syntax, find problems and enforce code style
- Use popular style guide (airbnb)
- Install depedencies with npm
- Remover package-lock.json e rodar `yarn` na pasta do projeto para mapear as dependências
- Copiar conteúdo do arquivo **eslintrc.js**
- `yarn eslint --fix {path} --ext .js` -> Fix automático de todos os arquivos .js dentro do {path}

> Instalando Prettier
- `yarn add prettier eslint-config-prettier eslint-plugin-prettier -D`
- Copiar conteúdo do arquivo **.prettierrc**

> Instalando Editor Config
- Instalar o plugin
- Clicar com o botão direito dentro do VS Code na opção **Generate .editorconfig**
- Ajustar as configurações de acordo com a preferência do time