# Installation

Install the npm package:

npm install typeorm --save

You need to install reflect-metadata shim:

npm install reflect-metadata --save

and import it somewhere in the global place of your app (for example in app.ts):

import "reflect-metadata";

You may need to install node typings:

npm install @types/node --save-dev

Install a database driver:

for MySQL or MariaDB

npm install mysql --save

for PostgreSQL or CockroachDB

npm install pg --save

for SQLite

npm install sqlite3 --save
