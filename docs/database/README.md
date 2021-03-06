# Database, ORM and sessions

We.js use Sequelize as Object-relational mapping (ORM) with extra steps for allowing model extensions in plugins

Current We.js database feature only suport SQL databases ('mysql'|'mariadb'|'postgres'|'mssql') 

For user session we.js projects use the express-session

## Important variables

In project execution default connection is avaible at `we.db.defaultConnection` and all models is avaible in `we.db.models`

## Database configuration

By default all projects have 3 database connection configurations that is selected by environment.
Example: if you are in dev enviroment it will start the default database connection with we.config.database.dev configuration

** For all database options see: http://sequelize.readthedocs.org/en/latest/api/sequelize/#class-sequelize **

### Mysql

Mysql suport requires mysql npm modules: `npm install --save mysql`
Example configuration:

file: `config/local.js`

```js
  // ...
  database: {
    prod: {
      //host: 'your-database-hostname',
      dialect: 'mysql',
      database: 'databaseName',
      username: 'databaseUser',
      port: '3306',
      password: 'password'
    },
    dev: {
      //host: 'your-database-hostname',     
      dialect: 'mysql',
      database: 'databaseName',
      username: 'databaseUser',
      port: '3306',      
      password: 'password'
    },
    test: {
      //host: 'your-database-hostname',      
      dialect: 'mysql',
      database: 'databaseName',
      username: 'databaseUser',
      port: '3306',      
      password: 'password'
    }
  }
  // ...
```

### PostgreSQL 

For suport with postgreSQL you need we-core v0.3.89+
To configure the postgreSQL database you need to:

1. Install **pg** and **pg-hstore** in your project:

```js
npm install --save pg pg-hstore
```

2. Configure the project **config/local.js**:

```js
  // ...
  database: {
    prod: {
      //host: 'your-database-hostname',     
      dialect: 'postgres',
      database: 'databaseName',
      username: 'databaseUser',
      password: 'password'
    },
    dev: {
      //host: 'your-database-hostname',  
      dialect: 'postgres',
      database: 'databaseName',
      username: 'databaseUser',
      password: 'password'
    }
  },
  // ...
```

3. Configure a session store

  We-core mysql session store is disabled without mysql database then you need to configure you session store.
  See the session store page
