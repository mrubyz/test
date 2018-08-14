---
layout: default
title: Για το κοινό
---


<div class="w3-container">

<h2>Accordions</h2>
<p>An accordion is used to show (and hide) HTML content:</p>
  
<button onclick="myFunction('Demo1')" class="w3-btn w3-block w3-blue w3-round-large w3-left-align">Open Section 1</button>
<div id="Demo1" class="w3-container w3-hide">
  <h4>Section 1</h4>
  <p>Some text..</p>
</div>

<button onclick="myFunction('Demo2')" class="w3-btn w3-block w3-blue w3-round-large w3-left-align">Open Section 2</button>
<div id="Demo2" class="w3-container w3-hide">
  <h4>Section 2</h4>
  <p>Some text..</p><p>Some text..</p>
</div>


<button onclick="myFunction('Demo3')" class="w3-btn w3-block w3-blue w3-round-large w3-left-align">Open Section 3</button>
<div id="Demo3" class="w3-container w3-hide">
  <h4>Section 3</h4>
  <p>Some text..</p><p>Some text..</p><p>Some text..</p><p>Some text..</p>
</div>

<button onclick="myFunction('Demo4')" class="w3-btn w3-block w3-blue w3-round-large w3-left-align">Open Section 4</button>
<div id="Demo4" class="w3-container w3-hide">
  <h4>Section 4</h4>
  <p>Some text..</p><p>Some text..</p><p>Some text..</p><p>Some text..</p>
</div>


</div>
<script>
function myFunction(id) {
    var x = document.getElementById(id);
    if (x.className.indexOf("w3-show") == -1) {
        x.className += " w3-show";
        x.previousElementSibling.className = 
        x.previousElementSibling.className.replace("w3-black", "w3-red");
    } else { 
        x.className = x.className.replace(" w3-show", "");
        x.previousElementSibling.className = 
        x.previousElementSibling.className.replace("w3-red", "w3-black");
    }
}
</script>
