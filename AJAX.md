##AJAX

> AJAX stands for **asynchronous Javascript and XML** and according to w3schools it is a developer's dream. Why? Because you can:

1. _Update a web page without reloading the page_
2. _Request data from a server - after the page has loaded_
3. _Receive data from a server - after the page has loaded_
4. _Send data to a server - in the background_

#### AJAX is not a programming language but a technique for accessing web servers from a web page. It allows web pages to be updated asynchronously by exchanging data with a web server behind the view of the user.
Short example

```javascipt
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
```
