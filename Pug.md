##Pug

> Pug is a high performance **template/view engine** we can use with nodejs. It is a rename from *'Jade'*and is is a clean, whitespace sensitive syntax for writing html. 

Simple example from npmjs doc:

```pug
doctype html
html(lang="en")
  head
    title= pageTitle
    script(type='text/javascript').
      if (foo) bar(1 + 5)
  body
    h1 Pug - node template engine
    #container.col
      if youAreUsingPug
        p You are amazing
      else
        p Get on it!
      p.
        Pug is a terse and simple templating language with a
        strong focus on performance and powerful features.
```

API example from npmjs doc:

```javascript
var pug = require('pug');
 
// compile 
var fn = pug.compile('string of pug', options);
var html = fn(locals);
 
// render 
var html = pug.render('string of pug', merge(options, locals));
 
// renderFile 
var html = pug.renderFile('filename.pug', merge(options, locals));
```