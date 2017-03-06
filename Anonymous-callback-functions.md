## Anonymous callback functions

#### Callback function
> A **callback function** is a function that you pass to someone and let them call it at some point of time, in simple words (?) Or, otherwise, a *reference* to executable code, or a piece of executable code, that is passed as an *argument* to other code.

#### Anonymous callback function

> The difference of an **anonymous** callback function is that it has no name. For example, in the following code, both  functions will produce the same result

```javascript
function acceptCallback(callback) {
  callback();
}

function callback() {
  console.log('callback invoked');
}
```

```javascript
function acceptCallback(callback) {
  callback();
}

acceptCallback(function() {
  console.log('callback invoked');
});
```
> In the first example we pass a function declaration, in the second example we pass an anonymous function