WELCOME TO XML LEARNING SUMMARY  
###############################

=============================================
AJAX is a developer's dream, because you can:
=============================================

AJAX (Asynchronous JavaScript and XML) allows web applications to fetch data from a server asynchronously without reloading the entire page.

--HTML Page
<!DOCTYPE html>
<html>
<body>

<div id="demo">
  <h2>Let AJAX change this text</h2>
  <button type="button" onclick="loadDoc()">Change Content</button>
</div>

</body>
</html>

--Function loadDoc()

function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     document.getElementById("demo").innerHTML = this.responseText;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}

--What is AJAX?
AJAX = Asynchronous JavaScript And XML.
