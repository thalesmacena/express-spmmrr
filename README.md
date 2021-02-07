<div align="center">

 # express-spmmrr-starter

  <div style="display: flex">
    <a href="https://nodejs.org/en/">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" alt="Node.JS"  width="50" height="50"/>
    </a>
     <a href="https://expressjs.com/pt-br/">
      <img src="https://expressjs.com/images/express-facebook-share.png" alt="Express.js"  width="100"/>
    </a>
    <a href="https://sequelize.org/master/">
      <img src="https://sequelize.org/master/manual/asset/logo-small.png" alt="Sequelize"  width="50" height="50"/>
    </a>
   <a href="https://www.postgresql.org/">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg"  width="50" height="50"/>
    </a>
    <a href="https://mongoosejs.com/">
      <img src="https://images.opencollective.com/frontendmasters/0b9cda4/logo/256.png" alt="Mongoose"  width="50" height="50"/>
    </a>
    <a href="https://www.mongodb.com/">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB"  width="50" height="50"/>
    </a>
    <a href="https://redis.io/">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original.svg" alt="Redis"  width="50" height="50"/>
    </a>
    <a href="https://github.com/Redocly/redoc">
      <img src="https://res.cloudinary.com/apideck/image/upload/v1594740999/icons/redoc.png" alt="ReDoc"  width="50" height="50"/>
    </a>

  </div>

</div>

A Node.js express back-end starter to save your time with Sequelize, Postgres, Mongo and Redis integration. With Redoc to serve the API Specification.

## What's included?
- dotenv
- eslint with prettier with airbnb styleguide
- nodemon and sucrase
- sentry
- youch
- bee-queue
- Sequelize CLI
- Redoc CLI
- yup
- Multer
- bcrypt
- jsonwebtoken

## Configuring the application
First clone this application in the repository you want. In the future this process will be easier. Then delete the .git folder and the others .gitignore.
### Set Databases
Then, create a Postgres and Mongodb database and a Redis image. I recommend using Docker, and use Postbird and mongodb compass to create a new database respectively.

now you need to rename the `.env.example` file to: `.env`.

### Setting the environment variables
```Shell
# Main is the default port of applicativon
MAIN=3333

# Change the APP_URL to match the port used
APP_URL=http://localhost:3333
NODE_ENV=devevlopment

# Auth

# APP_SECRET is the key used to set the hash of the jwt token
APP_SECRET=

# Database Postgres
DB_HOST=
DB_USER=
DB_PASS=
DB_NAME=

# mongodb
MONGO_URL=

# Redis because Redis
REDIS_HOST=127.0.0.1
REDIS_POST=6379

# Sentry
SENTRY_DSN=
```
### Set API Specification
You will find a api.yaml in the root of the application, this is a example of a OAS - Open API Specification (swagger specification). You can edit this file and change his name.

If you change his name, you need to configure the render script of ReDoc in package.json

```JSON
"api": "yarn redoc-cli serve 'path/to/file.yaml'"
```

## Run the project

the project has the following scripts configured:

```
yarn dev
```
run the application in development mode

```
yarn dev:debug
```
run the application in debug mode

```
yarn queue
```
run the queue service of the aplication with his background jobs

```
yarn api
```
Render the api specification with redoc, at `http://localhost:8080`
