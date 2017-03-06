## HTML-markup

> HTML-markup is an Html template engine

####Installation

`npm install html-markup`

#### Little example

```HTML
#{set title,'MyPage' /}
#{set menu,'home' /}
#{extends '/model.html' /}
<div>...</div>
#{include '/menu-' + menu + '.html' /}
<p>Bienvenue sur #{get title/}</p>
```

```javascript
var markup = require('markup')
var express = require('express');
var app = express();
 
app.engine('html', markup.renderFile);
app.set('views', markup.directory); // specify the views directory 
app.set('view engine', 'html'); // register the template engine 
 
// What's on /dist folder is freely accessible 
app.get('/dist', express.static(__dirname + '/dist'));
// For the rest, we use the engine 
app.get('/', markup.lookFor)
 
app.listen(80);
```


