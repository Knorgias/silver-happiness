## Promises

> Promises are a new improved way of writing callbacks and help our code run asynchronously

Example

```javascript
function readFile(filename, enc){
  return new Promise(function (fulfill, reject){
    fs.readFile(filename, enc, function (err, res){
      if (err) reject(err);
      else fulfill(res);
    });
  });
}
```