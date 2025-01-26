# Node.js Typescript Rest API with MySQL example
Building Node.js Typescript Express and MySQL: CRUD Rest API example.

| Methods	| Urls	| Actions
| -------- | ------- | ------- |
| GET | api/tutorials | get all Tutorials
| GET | api/tutorials/:id | get Tutorial by id
| POST | api/tutorials | add new Tutorial
| PUT | api/tutorials/:id | update Tutorial by id
| DELETE | api/tutorials/:id | remove Tutorial by id


## Project setup
```
npm install
```

### Run
```
npm run start
```

### MySQL Database

Connect to MySQL instance and create database and table as per below:

create database testdb;
use testdb;

CREATE TABLE IF NOT EXISTS `tutorials` (
  id int NOT NULL PRIMARY KEY AUTO_INCREMENT,
  title varchar(255) NOT NULL,
  description varchar(255),
  published boolean DEFAULT false
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

Once Table is created update application source code and then deploy again by editing below file:

src/config/db.config.ts
