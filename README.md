# Calculator
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
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
    background: linear-gradient(to right, blue, pink, red);
}
table.tbl{
    position: absolute;
    top: 45%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 15px;
    box-shadow: rgba(0, 0, 0, 0.56) 0px 22px 70px 4px;
}
input[type="button"]{
    color: black;
    cursor: pointer;
    background-color: white;
    font-size: 2em;
    border: 1px solid white;
    padding: 20px;
    width: 100%;
    margin: 10px 60px 10px 0px;   
}
input[type="text"]{
    color: black;
    background-color: white;
    padding: 20px;
    border: 1px solid white;
    font-size: 2em;
    width: 100%;

}
#clear{
    background: pink;
    border: 1px solid pink;
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
