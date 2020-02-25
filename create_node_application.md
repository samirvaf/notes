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

> Auth feature

- Create .env parameter APP_SECRET used to hash the passwords
- Create inside /config folder a file auth.js
- exports secret and expiresIn
- Inside User model create a addHook('beforeSave') to hash the password using bcryptjs also create a method to checkPassword
- Create a session controller, import jsonwebtoken and Yup to validate request data
- Start by creating a Yup object to check if request has email and password
- Search in the database for the User with a corresponding email
- Finally call checkPassword method to validate the user
- If everything goes well, return a user object with desired data and a second object called token, use jsonwebtoken.sign() method

> Auth middleware

- Inside /app folder create middlewares folder
- import jsonwebtoken, promisify from util and authConfig from your config file
- export a async arrow function (req, res, next)
- Need to check if req.headers.authorization exists
- Get token from it by split(' '), remember it is a bearer token
- Inside a try/catch block, validate token by calling await promisify(jwt.verify)(token, authConfig.secret)
- Optionally you can add the logged in ID inside the request object to further use
- return next(); if everything goes well, so the application can continue to the subsequent route
- Inside your routes.js file, import authMiddleware and use it before all routes that requires an authenticated user
