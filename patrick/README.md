# LS-Mongo-I

## Topics - OKAY √

* Databases
* Relational Databases
* Non-Relational Databases
* MongoDB
* Mongoose
* ORM
* `mongod` vs `mongod --dbpath data` ???
* Mongoose.connect
* Mongoose.Schema
* Mongoose.model
* module.exports
* Model.find
* Model.findById
* Model.find().remove()
* .save
* Error first callback
* \_id

## Assignment

Download MongoDB.  https://www.mongodb.com/download-center - DONE √
  ```console
  $  mongo --version
      MongoDB shell version v3.4.7
      git version: cf38c1b8a0a8dca4a11737581beafef4fe120bcd
      OpenSSL version: OpenSSL 1.0.2l  25 May 2017
      allocator: system
      modules: none
      build environment:
          distarch: x86_64
          target_arch: x86_64
  ```

Create a new folder and run `npm init` to create your `package.json` file. - DONE √
  ```console
  $  npm init
      This utility will walk you through creating a package.json file.
      It only covers the most common items, and tries to guess sensible defaults.

      See `npm help json` for definitive documentation on these fields
      and exactly what they do.

      Use `npm install <pkg>` afterwards to install a package and
      save it as a dependency in the package.json file.

      Press ^C at any time to quit.
      package name: (patrick) user-db
      version: (1.0.0)
      description: LS-Mongo-I Assignment
      entry point: index.js
      test command:
      git repository: https://github.com/mixelpixel/LS-Mongo-I.git
      keywords:
      author: Patrick Kennedy
      license: (ISC)
      About to write to /Users/mixelpix/Lambda-University/LS-Mongo-I/patrick/package.json:

      {
        "name": "user-db",
        "version": "1.0.0",
        "description": "LS-Mongo-I Assignment",
        "main": "index.js",
        "scripts": {
          "test": "echo \"Error: no test specified\" && exit 1",
          "start": "node server.js"
        },
        "repository": {
          "type": "git",
          "url": "git+https://github.com/mixelpixel/LS-Mongo-I.git"
        },
        "author": "Patrick Kennedy",
        "license": "ISC",
        "bugs": {
          "url": "https://github.com/mixelpixel/LS-Mongo-I/issues"
          },
          "homepage": "https://github.com/mixelpixel/LS-Mongo-I#readme"
        }

        Is this ok? (yes)
        5 mixelpix Tue Aug 15 01:41:25$  npm i --save express body-parser cors mongoose
        npm notice created a lockfile as package-lock.json. You should commit this file.
        + cors@2.8.4
        + body-parser@1.17.2
        + mongoose@4.11.7
        + express@4.15.4
        added 81 packages in 10.865s
  ```

Install npm packages: `npm i --save express body-parser cors mongoose` - DONE √
  ```console
  $  npm i --save express body-parser cors mongoose
      + body-parser@1.17.2
      + express@4.15.4
      + cors@2.8.4
      + mongoose@4.11.7
      updated 4 packages in 5.624s
  ```

- Not using this:
  ```console
  $  npm i --save mongodb
      + mongodb@2.2.31
      updated 1 package in 5.294s
  ```

- Definitely used this:
  ```console
  $ mkdir data
  ```

  - some changes to package.json
  ```json
  "test": "echo \"Error: no test specified\" && exit 1"
  "test": "eslint *.js && nodemon server.js"

  "babel-preset-es2015": "^6.24.0",
  "eslint": "^3.17.1",
  "eslint-config-airbnb": "^14.1.0",
  "eslint-plugin-import": "^2.2.0"
  ```


Start your MongoDB server by running ~~`mongod`~~ from the command line. - OKAY √
  - USING: `mongod --dbpath data`
Implement the following routes but have them utilize a database to achieve data persistence. - DONE √
* [POST] `/users` This route should save a new user to the server. - DONE √
* [GET] `/users` This route will return an array of all users. - DONE √
* [GET] `/users/:id` This route will return the user with the matching `id` (`_id` on the db document) property. - DONE √
* [DELETE] `/users/:id` This route should delete the specified user. - DONE & DONER √

## Extra Credit

Implement a second collection called `BlogPosts`.  Implement the following routes: - DONE √
* [POST] `/posts` This route should save a new blog post to the server. - DONE √
* [GET] `/posts` This route will return an array of all blog posts. - DONE √
* [GET] `/posts/:id` This route will return the blog post with the matching `id` property. - DONE √
* [DELETE] `/posts/:id` This route should delete the specified blog post. - DONE √
Your user objects can take any form.
