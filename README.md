<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <link rel="stylesheet" href="3.CSS">
</head>
  <style>
    body {
    background-color: #f4f4f4;
    background-image: linear-gradient(135deg, #7DE2FC 10%, #B9B6E5 100%);
    background-position: center;
}
.calculator {
   width: 300px;
   margin: 50px auto;
   background-color: rgb(0, 0, 0);
   border-radius: 10px;
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.4);
   padding: 20px;
}
.calculator input[type="button"] {
   width: 50px;
   height: 50px;
   font-size: 20px;
   margin: 8px;
   cursor: pointer;
   border: none;
   border-radius: 5px;
}
#display {
   width: auto;
   margin-bottom: 10px;
   padding: 10px;
   font-size: 20px;
   height: auto;
}
.calculator input[type="button"].equals {
   height: 5vh;
}
.calculator input[type="button"]:hover{
color: black;
}
h1 {
   color: black;
   text-align: center;
   font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
   font-weight: bolder;
}
  </style>
<body>
    <h1>CALCULATOR</h1>
    <div class="calculator">
        <input type="button" value="C" onclick="clearDisplay()" class="equals">
        <input type="text" id="display" disabled>
        <input type="button" value="7" onclick="appendToDisplay('7')">
        <input type="button" value="8" onclick="appendToDisplay('8')">
        <input type="button" value="9" onclick="appendToDisplay('9')">
        <input type="button" value="/" onclick="appendToDisplay('/')">
        <br>
        <input type="button" value="4" onclick="appendToDisplay('4')">
        <input type="button" value="5" onclick="appendToDisplay('5')">
        <input type="button" value="6" onclick="appendToDisplay('6')">
        <input type="button" value="*" onclick="appendToDisplay('*')">
        <br>
        <input type="button" value="1" onclick="appendToDisplay('1')">
        <input type="button" value="2" onclick="appendToDisplay('2')">
        <input type="button" value="3" onclick="appendToDisplay('3')">
        <input type="button" value="-" onclick="appendToDisplay('-')">
        <br>
        <input type="button" value="0" onclick="appendToDisplay('0')">
        <input type="button" value="." onclick="appendToDisplay('.')">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="+" onclick="appendToDisplay('+')">
        <br>
    </div>
    <script>
        function calculate() {
            try {
                document.getElementById('display').value = eval(document.getElementById('display').value);
            } catch (error) {
                document.getElementById('display').value = 'Error';
            }
        }
        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }
        function clearDisplay() {
            document.getElementById('display').value = '';
        }
    </script>
</body>
</html>
