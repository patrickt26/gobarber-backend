<h1 align="center">
    <img alt="GoBarber API" src="./asset/gobarber_gostack.png" />
    <br>
    GoBarber API
</h1>

<h4 align="center">
  API REST, desenvolvida em Node.js, de uma aplicação de agendamento de barbearia que permite aos usuários agendar uma consulta com seu barbeiro favorito e mostra ao barbeiro sua agenda para o dia.
</h4>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/patrickt26/gobarber-backend.svg">

  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/patrickt26/gobarber-backend.svg">

  <img alt="GitHub" src="https://img.shields.io/github/license/patrickt26/gobarber-backend.svg">
</p>

<p align="center">
  <a href="#clipboard-executando">Executando</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#busstop-rotas">Rotas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#rocket-tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

  ## :clipboard: Executando

  <h3>
  - Docker
  </h3>

  Para esse projeto foi utilizado um container de Docker de PostgreSQL.

  Para executar o projeto assim como foi desenvolvido, crie um container Docker com o comando:
  ```
  docker run --name postgresDB -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres:11
  ```

  Caso já possua um banco PostgreSQL, um container de Docker para o mesmo ou até mesmo utiliza de outro banco de dados relacional, basta apenas alterar as credenciais de conexão com o banco no arquivo [database.js][database.js].

  <h3>
  - Node.js
  </h3>

  Com o projeto em sua máquina, execute na pasta raiz do projeto, para baixar todas as depêndencias necessárias para rodar a aplicação, o comando:
  ```
  yarn
  ```

  Inicie o projeto em ambiente de desenvolvimento com o comando:
  ```
  yarn dev
  ```
  (Obs.: o projeto estará rodando em http://localhost:3333)

  ## :busstop: Rotas

  Por meio desta API, é possível realizar requisições para:

  Usuário
  - Criar
  ```
  POST: http://localhost:3333/users
  ```
  - Atualizar *
  ```
  PUT: http://localhost:3333/users
  ```

  Sessão
  - Criar
  ```
  POST: http://localhost:3333/sessions
  ```

  </br>
  (*) - Rotas em que só é possível realizar requisicões estando autenticado**.
  </br>
  (**) - Ao realizar a requisição de Sessão, é retornado um Token, que deve ser utilizado em requisições para rotas em que é necessário um usuário autenticado.

## :rocket: Tecnologias

Esse é um projeto desenvolvido no [RocketSeat GoStack Bootcamp](https://rocketseat.com.br/bootcamp) com as seguintes tecnologias:

-  [Node.js][nodejs](v12.14.0)
-  [Express](https://expressjs.com/)(v.4.17.1)
-  [nodemon](https://nodemon.io/)(v.2.0.2)
-  [Sucrase](https://github.com/alangpierce/sucrase)(v.3.12.1)
-  [Docker](https://www.docker.com/docker-community)(v.19.03.5)
-  [Sequelize](http://docs.sequelizejs.com/)(v.5.21.3)
-  [PostgreSQL](https://www.postgresql.org/)(v.11)
-  [node-postgres](https://www.npmjs.com/package/pg)(v.7.18.1)
-  [Yup](https://github.com/jquense/yup)(v.0.28.1)
-  [VS Code][vc] com [ESLint][vceslint](v.6.8.0) e [EditorConfig][vceditconfig](v.0.14.4)
-  [Prettier][prettier](v.1.19.1)

## :memo: Licença
Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](https://github.com/patrickt26/gobarber-backend/blob/master/LICENSE) para mais detalhes.

---

Feito com ♥ por Patrick Thomaz :wave: [Get in touch!](https://www.linkedin.com/in/patrick-thomaz/)

[nodejs]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[vc]: https://code.visualstudio.com/
[vceditconfig]: https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig
[vceslint]: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint
[prettier]: https://prettier.io
[database.js]: https://github.com/patrickt26/gobarber-backend/blob/master/src/config/database.js
