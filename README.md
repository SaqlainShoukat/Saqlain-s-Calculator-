<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simple Calculator</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
    }
    .calculator {
        width: 300px;
        margin: 0 auto;
        border: 1px solid whitesmoke;
        border-radius: 5px;
        padding: 20px;
        background-color: navajowhite;
    }
    .calculator input[type="button"] {
        width: 60px;
        height: 40px;
        margin: 5px;
        font-size: 18px;
        cursor: pointer;
    }
    .calculator input[type="text"] {
        width: 100%;
        height: 40px;
        margin-bottom: 10px;
        font-size: 18px;
        text-align: right;
        padding-right: 10px;
    }
</style>
</head>
<body>
    <div class="calculator">
        <input type="text" placeholder="Saqlain" id="display" readonly>
        <br>
        <input type="button" value="7" onclick="addToDisplay('7')">
        <input type="button" value="8" onclick="addToDisplay('8')">
        <input type="button" value="9" onclick="addToDisplay('9')">
        <input type="button" value="/" onclick="addToDisplay('/')">
        <br>
        <input type="button" value="4" onclick="addToDisplay('4')">
        <input type="button" value="5" onclick="addToDisplay('5')">
        <input type="button" value="6" onclick="addToDisplay('6')">
        <input type="button" value="×" onclick="addToDisplay('*')">
        <br>
        <input type="button" value="1" onclick="addToDisplay('1')">
        <input type="button" value="2" onclick="addToDisplay('2')">
        <input type="button" value="3" onclick="addToDisplay('3')">
        <input type="button" value="-" onclick="addToDisplay('-')">
        <br>
        <input type="button" value="0" onclick="addToDisplay('0')">
        <input type="button" value="." onclick="addToDisplay('.')">
        <input type="button" value="=" onclick="calculate()">
        <input type="button" value="+" onclick="addToDisplay('+')">
        <br>
        <input type="button" value="C" onclick="clearDisplay()">
    </div>

    <script>
        function addToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            let expression = document.getElementById('display').value;
            let result = eval(expression); // Using eval for simplicity (not recommended for production due to security risks)
            document.getElementById('display').value = result;
        }
    </script>
</body>
</html>
