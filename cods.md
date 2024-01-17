<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
.dropbtn {
  background-color: white;
  color: black;
  padding: 0;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.dropbtn:hover, .dropbtn:focus {
  background-color: #FFFFFF;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  
  background-color: #ffffff;
  min-width: 160px;
  overflow: auto;
  
  
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown a:hover {background-color: #ddd;}

.show {display: block;}
</style>
</head>
<body style="background-color:white;">

<h2>Clickable Dropdown</h2>
<p>Click on the button to open the dropdown menu.</p>

<div class="dropdown">
  <button onclick="myFunction()" class="dropbtn">How To Perform</button>
  <div id="myDropdown" class="dropdown-content">
	<p>How to text here</p>
  </div>
</div>
<h2>Clickable Dropdown</h2>
<p>Click on the button to open the dropdown menu.</p>

<script>
/* When the user clicks on the button, 
toggle between hiding and showing the dropdown content */
function myFunction() {
  document.getElementById("myDropdown").classList.toggle("show");
}

// Close the dropdown if the user clicks outside of it
window.onclick = function(event) {
  if (!event.target.matches('.dropbtn')) {
    var dropdowns = document.getElementsByClassName("dropdown-content");
    var i;
    for (i = 0; i < dropdowns.length; i++) {
      var openDropdown = dropdowns[i];
      if (openDropdown.classList.contains('show')) {
        openDropdown.classList.remove('show');
      }
    }
  }
}
</script>

</body>
</html>
