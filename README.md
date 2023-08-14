# temp.html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
 #convert {
  background-color:red;
}
#convert:hover {
  background-color:yellow;
}
h1 {
  font-family:'Times New Roman', Times, serif;
  margin-top: 100px;
  color:black;
}
.box{
  margin-top: 55px;
  display: block;
  width: 50%;
  height: 30ch;
  background-image:url("https://static.vecteezy.com/system/resources/thumbnails/002/295/452/small/background-of-scientific-and-technological-system-for-calculating-complex-data-vector.jpg");
}

input {
  display: block;
  padding: 10px;
  margin-top: 30px;
  color: #f4a55a;
  font-family: cursive, sans-serif;
}
::-webkit-input-placeholder {
   color:black;
}

:-ms-input-placeholder {  
   color:brown;  
}
button {
  padding: 25px;
  color:cadetblue;
  margin-top: 3px;
}
</style>
<title>Temperature Converter</title>
</head>
<body>
  <h1><center><font size="7">Temperature Converter</font></center></h1>
  <center>
  <div class="box">
  <input type="text" id="fahrenheit" placeholder="Fahrenheit" name="f" value="" />
  <input type="text" id="celsius" placeholder="Celsius" name="c" value="" />
  <button id="convert">CONVERT</button>
  <button id="clear">RESET</button>
  </div>
  </center>
  <script>
    document.getElementById('convert').onclick = tempConvert;
    document.getElementById('clear').onclick = clearForm;
    function tempConvert() {
       var fahrenheit = document.getElementById("fahrenheit").value;
       var celsius = document.getElementById("celsius").value;
       if (fahrenheit != '') {
            celsius = (parseFloat(fahrenheit) - 32) / 1.8;
       } 
      else {
        fahrenheit = (parseFloat(celsius) * 1.8) + 32;
       }
    document.getElementById('fahrenheit').value = parseFloat(fahrenheit).toFixed(1);
    document.getElementById('celsius').value = parseFloat(celsius).toFixed(1);
    }
   function clearForm() {
    document.getElementById('fahrenheit').value = '';
    document.getElementById('celsius').value = '';
   } 
</script>
</body>
</html>
