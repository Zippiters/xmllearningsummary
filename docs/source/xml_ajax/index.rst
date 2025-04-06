AJAX Introduction
=================

AJAX (Asynchronous JavaScript and XML) is a technique used to create fast and dynamic web pages by allowing data to be sent and received asynchronously between the web browser and a server.

**How AJAX Works**

1. A user triggers an event (e.g., clicking a button).
2. JavaScript creates an `XMLHttpRequest` object.
3. The request is sent to the server.
4. The server processes the request and sends a response.
5. JavaScript updates the webpage dynamically.

**Example: Simple AJAX Request (by vinch)**

.. code-block:: html

    <button type="button" onclick="loadData()" style="padding:10px 15px; background-color:#3498db; color:white; border:none; border-radius:5px;">Fetch Data</button>
    <p id="content" style="margin-top:15px; padding:10px; border:1px solid #ccc; background-color:#f9f9f9;"></p>

    <script>
    // AJAX function created by vinch
    function loadData() {
      var xhttp = new XMLHttpRequest();
      xhttp.onreadystatechange = function() {
        if (this.readyState == 4 && this.status == 200) {
          document.getElementById("content").innerHTML = this.responseText;
        }
      };
      xhttp.open("GET", "data.txt", true);
      xhttp.send();
    }
    </script>

