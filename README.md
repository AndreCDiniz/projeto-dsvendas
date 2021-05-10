<h1 align="center">
    <a href="https://andre-dashvendas.netlify.app/">🔗 PROJETO-SDS3
</a>
</h1>


## Descrição do Projeto
🚀 Projeto desenvolvido durante a [Semana Spring React da DevSuperior](https://github.com/devsuperior/sds3).

&nbsp;&nbsp;&nbsp;

## 🛠 Ferramentas necessárias/utilizadas:
- [x] Git
- [x] Java JDK 11
- [x] Maven
- [x] STS
- [x] Insomnia
- [x] Postgresql e pgAdmin
- [x] Heroku CLI
- [x] Node & NPM
- [x] YARN (Caso queira usar ao invés do NPM)
- [x] VS Code
- [x] STS (Spring Tool Suite) 

### Tecnologias utilizadas :

As seguintes ferramentas foram usadas na construção do projeto:

- [React](https://pt-br.reactjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [PostgreSQL](https://www.postgresql.org/)
- [Spring Data JPA - JpaRepository + JPQL](https://spring.io/)


### Demonstração da Aplicação

#### Link do Projeto Netlify
https://andre-dashvendas.netlify.app/


#### Home Page:
<img src="https://github.com/AndreCDiniz/projeto-dsvendas/blob/master/frontend/src/assets/img/Home.png" width=80% >

#### Dashboard Page:
<img src="https://github.com/AndreCDiniz/projeto-dsvendas/blob/master/frontend/src/assets/img/Dashboard.png" width=80% >

### Badges
[![Netlify Status](https://api.netlify.com/api/v1/badges/a40749b2-82ce-4ff6-8d49-504aeba8e5e8/deploy-status)](https://app.netlify.com/sites/andre-dashvendas/deploys)

&nbsp;&nbsp;&nbsp;

## ⏲️ Etapas
### Criação do Projeto (monorepo)
   #### 1) Frontend
   - Criar o React App no diretório do projeto:

   `npx create-react-app frontend --template typescript`
        
   Lembrar de remover o arquivo .git

   - Adicionar Bootstrap para utiliziar no projeto:

   `yarn add bootstrap`

   - Adicionar biblioteca de gráficos estáticos: Apex Charts

   `yarn add apexcharts react-apexcharts`

   #### 2) Backend
   Criado projeto Spring Boot no *[Spring Initializr](https://start.spring.io/)* com as seguintes dependências:
   - Web
   - JPA
   - H2
   - Postgres
   - Security

   ##### Deploy da Aplicação com Netlify: :dash:
   Configurações para a Publicação no Netlify:
   - Site -> *New site from Git*
     
   - Basic build settings
        - Build Comand: yarn build
        - Publish Directory: build
        - *Deploy site*
        
        Deploy! (vai quebrar)
   - Site settings
        - Build & Deploy: (colocar o nome da sua subpasta do projeto frontend)
        - Domain Management: (colocar o nome que você quiser)
   - Deploys -> *Trigger deploy*

   #### 3) Implementação do Backend
   Padrão de camadas utilizado (repositories, DTO's, service e controller), com busca paginada e agrupada:
   [<img src="https://github.com/devsuperior/bds-assets/raw/main/sds/camadas.png" width=50% >](https://spring.io/guides)

   - Criado três arquivos de properties com perfis de: test, dev, prod
   - Gerado script SQL no perfil dev para criação das tabelas do Banco de Dados ([create.sql](https://github.com/jpbraz/projeto-sds3/blob/main/backend/create.sql))

   #### 4) Implementação e Deploy no Heroku:
   - Criado novo app no [Heroku](heroku.com)
   - Provisionado banco Postgres, definindo variável APP_PROFILE=prod
   - Criado servidor de acesso local via DBeaver (poderia ser feito via PgAdmin) utiliando dados de credenciais do Database.
   - Deploy do backend no Heroku via terminal (no diretório do projeto):

    heroku login
    heroku git:remote -a <nome-do-app>
    git subtree push --prefix backend heroku maingit subtree push --prefix backend heroku main


&nbsp;&nbsp;&nbsp;
