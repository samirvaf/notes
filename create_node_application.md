# Steps to create node application

> Create application base structure

- Set up environment following notes inside /environment_setup
- Create src/ folder
- Inside src/ create app/ database/ config/ folders
- app.js server.js routes.js files

> Install express and run the project with a simple route

- yarn add express
- Create App class initializing express, middlewares and routes
- Set up a simple route to run and test the application

> Set up database (Sequelize/Postgres)

- Run a docker container with your postgres database
- Put all the info, username, password, host and database name inside .env file
- Inside /config folder create a database.js file with the .env references for the needed info to connect to our database
- Set up .sequelizerc file with the paths for models, migrations, seeds, config file
- Inside /database folder create a index.js file to set up the database connection, follow sequelize documentation
- Import ./database folder inside app.js file
- Create migrations/seeds by running yarn sequelize migration:create --name=migration_name
- Edit the generated file with the data that you need (create table, modify table)
- Run your migrations: yarn sequelize db:migrate
- To create seeds: yarn sequelize seed:generate --name=seeds_name
- Edit the same way as migrations file and than run: yarn sequelize db:seed:all

> Create models

- Create /models folder inside src/app/
- Create model file e.g User.js
- import { Sequelize, Model } from 'sequelize';
- Created class should extend sequelize Model
- Follow sequelize documentation to finish model file
- Import and initialize model inside database/index.js