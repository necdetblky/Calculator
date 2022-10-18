# Calculator
html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Calculator</title>
</head>
<body>
    <table class="tbl">
        <tr>
            <td colspan="3"><input type="text" id="result"></td>
            <td><input type="button" value="c" onclick="clr()" id="clear"></td>
        </tr>
        <tr>
            <td><input type="button" value="1" onclick="Num(1)"></td>
            <td><input type="button" value="2" onclick="Num(2)"></td>
            <td><input type="button" value="3" onclick="Num(3)"></td>
            <td><input type="button" value="/" onclick="Num('/')"></td>
        </tr>
        <tr>
            <td><input type="button" value="4" onclick="Num(4)"></td>
            <td><input type="button" value="5" onclick="Num(5)"></td>
            <td><input type="button" value="6" onclick="Num(6)"></td>
            <td><input type="button" value="-" onclick="Num('-')"></td>
        </tr>
        <tr>
            <td><input type="button" value="7" onclick="Num(7)"></td>
            <td><input type="button" value="8" onclick="Num(8)"></td>
            <td><input type="button" value="9" onclick="Num(9)"></td>
            <td><input type="button" value="+" onclick="Num('+')"></td>
        </tr>
        <tr>
            <td><input type="button" value="." onclick="Num('.')"></td>
            <td><input type="button" value="0" onclick="Num('0')"></td>
            <td><input type="button" value="=" onclick="equal()"></td>
            <td><input type="button" value="*" onclick="Num('*')"></td>
        </tr>
    </table>
</body>
</html>

style.css
body{
    background:linear-gradient(to right, #6F3F36, #804F46, #A5766D, #CBA9A3);
  }
  table.tb1{
    position:absolute;
    top:45%;
    left:35%;
    transform:transtale(-50%, -50%);
    border:1px solid black;
    background:grey;
    box-shadow:5px 10px;
    border-radius:25px;
  }
  input[type="button"]{
    cursor:pointer;
    color:black;
    background-color:white;
    width:2em;
    height:2em;
    font-family:cursive;
    font-size:large;
    font-weight:bold;
    border:1px solid white;
    margin:2px;
     border-radius:25px;
  }
  input[type="text"]{
    width:85%;
    padding:7px;
    font-family:sans-serif;
    font-weight:bold;
    border:1px solid black;
    background:white;
    color:black;
    font-size:large ;
     border-radius:25px;
  }
  #clear{
    color:black;
    background-color:pink;
    width:2em;
    border: 1px solid white;
  }

script.js
function Num(val){ 
    document.getElementById('result').value += val;

}

function equal(){
    let Input = document.getElementById('result').value;
    let Output = eval(Input);
    document.getElementById('result').value = Output;
}

function clr(){
    document.getElementById('result').value = '';
}
