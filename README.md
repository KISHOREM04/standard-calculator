# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write  Javascript program for implementing five different operations.

### Step 5:
Vlidate the HTML and CSS code.

### Step 6:
Publish the website in the given url.


## PROGRAM :
```
calc.html

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/CSS/style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">
        <h1>Calculator</h1>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>

</body>
<script src="/static/JS/index.js"></script>

</html>

index.js

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

style.css

.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: #ff99f7;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}
```
## OUTPUT:
![output 1](https://user-images.githubusercontent.com/119404643/213697844-396c3f31-8311-46a8-8e4b-5c03db94897c.png)

![output 2](https://user-images.githubusercontent.com/119404643/213697924-96f5fdf9-4130-4628-b452-47ace846faed.png)

## HTML VALIDATOR:
![HTML valid](https://user-images.githubusercontent.com/119404643/213698196-b783cf09-b9d6-41e1-988d-1405ac6caed7.png)

## RESULT:
The program for designing a simple calculator using Jvascript is created successfully.


