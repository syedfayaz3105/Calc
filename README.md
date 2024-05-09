# Ex.08 Design of a Standard Calculator
## Date:04-05-2024

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
calc.html
```
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="calculator.css">
    <title> Calculator </title>
</head>
<body>
    <center>
    <div class="container">
        <h1>Calculator</h1>
        <h1>Farhana H (23012987)</h1>
        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color"> C </button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button> 7 </button></td>
                    <td><button> 8 </button></td>
                    <td><button> 9 </button></td>
                    <td><button class="color"> * </button></td>
                </tr>
                <tr>
                    <td><button> 4 </button></td>
                    <td><button> 5 </button></td>
                    <td><button> 6 </button></td>
                    <td><button class="color"> - </button></td>
                </tr>
                <tr>
                    <td><button> 1 </button></td>
                    <td><button> 2 </button></td>
                    <td><button> 3 </button></td>
                    <td><button class="color"> + </button></td>
                </tr>
                <tr>
                    <td><button> 0 </button></td>
                    <td><button class="color"> . </button></td>
                    <td><button class="color"> / </button></td>
                    <td><button class="color"> = </button></td>
                </tr>
            </table>
        </div>
    </div>
    </center>
</body>
<script src="calculator.js"></script>
</html>
```
calculator.css
```
.container {
    text-align: center;
    margin-top:23px
}

table {
    margin: auto;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(12, 11, 11);
    padding: 20px;
    background: transparent;
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: black;
}

button {
    border-radius: 20px;
    border: 0;
    outline: 0;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: transparent;
    color: black;
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}

.calculator { 
    border: none;
    background-color: lightblue;
    padding: 30px;
    border-radius: 30px;
    display: inline-block;
    
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

.color {
    color: black;
}
```
calculator.js
```
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```
## OUTPUT:
![Screenshot (19)](https://github.com/syedfayaz3105/Calc/assets/147144126/0ec8b32b-14b9-4c4e-acb2-d473c265229b)
![Screenshot (20)](https://github.com/syedfayaz3105/Calc/assets/147144126/3b0ded41-07e7-48d7-b4bd-04793473522a)



## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
