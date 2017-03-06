## File system module

> The file system module is a module in *nodejs* that we can use to **handle files**, like *read* and *write* files
> We can install and require it in our code

Example on requiring it

```javascript
var fs = require("fs");
```

Example on using it

```javascript
// Asynchronous read
fs.readFile('input.txt', function (err, data) {
   if (err) {
      return console.error(err);
   }
   console.log("Asynchronous read: " + data.toString());
});

// Synchronous read
var data = fs.readFileSync('input.txt');
console.log("Synchronous read: " + data.toString());

console.log("Program Ended");
```