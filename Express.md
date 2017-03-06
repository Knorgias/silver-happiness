## Express

> Definition of express as found in *https://www.tutorialspoint.com/nodejs/nodejs_express_framework.htm*
>Express is a minimal and flexible Node.js web application framework that provides a robust set of features to develop web and mobile applications. It facilitates the rapid development of Node based Web applications.

####Installing Express

Firstly, install the Express framework globally using NPM so that it can be used to create a web application using node terminal.

######Installation command

$ npm install express --save

Little example ('hello world')

```javascript
var express = require('express');
var app = express();

app.get('/', function (req, res) {
   res.send('Hello World');
})

var server = app.listen(8081, function () {
   var host = server.address().address
   var port = server.address().port
   
   console.log("Example app listening at http://%s:%s", host, port)
})
```