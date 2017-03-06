##Sequelize ORM

> Sequelize is a promise-based ORM for Node.js and io.js. We can use Sequelize to greatly simplify the queries we can make to the database with SQL. 

Usage example

```javascript
let Sequelize = require('sequelize');
let sequelize = new Sequelize('database', 'username', 'password');

let User = sequelize.define('user', {
  username: Sequelize.STRING,
  birthday: Sequelize.DATE
});

sequelize.sync().then(function() {
  return User.create({
    username: 'janedoe',
    birthday: new Date(1980, 6, 20)
  });
}).then(function(jane) {
  console.log(jane.get({
    plain: true
  }));
});