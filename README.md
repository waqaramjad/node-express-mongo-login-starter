Node-Express-Mongo-Login-Starter
------------------------

A starter log-in application for **Node.js** using **Express** web framework and **MongoDB**.

Getting Started
---------------

Install [MongoDB](https://www.mongodb.org/downloads)

Install [Node.js](http://nodejs.org)

`git clone https://github.com/simondiep/node-express-mongo-login-starter.git`

`cd node-express-mongo-login-starter`

`npm install`

`node app`

Additional Tips
---------------

When developing, I highly recommend [nodemon](https://github.com/remy/nodemon).  It monitors a running app and restarts the app if any files have changed.  This has saved me a lot of time from manually restarting Node to see a new change.
`npm install -g nodemon`

For static code analysis, I recommend [jshint](https://www.npmjs.com/package/jshint).  It catches a lot of issues that are easily glossed over.
`npm install -g jshint`

npm scripts have been set up to run the app as well as tests, inside package.json

`npm start`

`npm test`

`npm lint`

What happens behind the scenes with MongoDB
--------------------------------------------
When a user visits the site, a new **session** document is **created** in MongoDB, with the passport field empty.

When the user creates a new account, a new **user** document is **created** in MongoDB.

When the user logs into the site, the existing **session** is **updated** by adding the user's ID into the session document.  The passport field is used.

When the user logs out of the site, the user's ID is **removed** from the **session** document's passport field.


Why each NPM Package is included
--------------------------------

| Express Package      | Description |
| -------------------- | ----------- |
| body-parser          | Simplifies incoming request data |
| express              | Node.js web framework |
| express-flash        | Notification messages |
| express-session      | Session Management |
| express-validator    | Simple form validation |
| morgan               | HTTP Request logging |
  
| General Package      | Description |
| -------------------- | ----------- |
| bcrypt-nodejs        | Password hashing and salting |
| jade                 | HTML template engine |
| mongoose             | MongoDB object modeling |
| passport             | Simple authentication library |
| passport-local       | Username/Password sign-in plugin for passport |
  
| Testing Package      | Description |
| -------------------- | ----------- |
| chai                 | Assertion library used by Mocha |
| mocha                | Test framework |
| supertest            | HTTP assertion library |

