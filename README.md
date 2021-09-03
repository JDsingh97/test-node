# TURF WAR BE

# File and folder Naming conventions

- Folder and file name will be singular and follow `kebab-case`
- Classes and interfaces Names will be singular and follow `PascalCasing`
- Any global constants or environment variables are in `all-caps` and follow `SNAKE_CASE`

For more details onto casing refer [here](https://medium.com/better-programming/string-case-styles-camel-pascal-snake-and-kebab-case-981407998841)

# API

## Add new API

In order to add a new API resource,

- create a new controller in folder `src/app/controllers`
- in `src/app/routes` folder, add the resource in `index.ts` file and create another file for the routes of a particular resource. This file be then used in `index.ts` for mapping the resource and the routes.
- For API validation create a validator file in `src/app/validators` folder. This file should contain only the Joi object. For use of that object refer to `src/app/routes/userRoutes.ts`

## API Docs

Swagger is to be used for API documentation.

# Project Setup

To setup the project, all you need to do is
`docker-compose up -d`

# DB

This project uses typeorm for orm to connect and execute queries on DB. It is configured to use postgres as its database.

This setup is using sync option of Typeorm. So DB is automatically updated with updates in our models

# Module Aliases

This project setup uses some module aliases for the ease in readbility and importing of other modules.
Refer to `_moduleAliases` section in `package.json` for currently created module aliases. These aliases are workable in src folder only as of now
