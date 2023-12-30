# ODD23-24-WT-JavaScript

## Name: Mathesh S
## Reg no: 23013902

## (A)
# AIM:
To create a form with java script code to calculate electricity bill.

#  Designing Procedure:

## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as calc().

## STEP 4:
Give the necessary input that is required for calculating the electricity bill like var prev,curr,units,amt. Get the number for input using document.getElementById.

## STEP 5:
Give the necessary condition using if-else condition. Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 7 :
End the HTML structure.

## Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electricity Bill Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input {
            margin-bottom: 10px;
        }
        button {
            padding: 8px 12px;
            font-size: 16px;
            cursor: pointer;
        }
        #result {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>

    <h2>Electricity Bill Calculator</h2>

    <label for="consumption">Enter Monthly Consumption (in kWh):</label>
    <input type="number" id="consumption" placeholder="Enter consumption" required>

    <label for="rate">Enter Electricity Rate (per kWh):</label>
    <input type="number" id="rate" placeholder="Enter rate" required>

    <button onclick="calculateBill()">Calculate Bill</button>

    <div id="result"></div>

    <script>
        function calculateBill() {
            var consumption = document.getElementById('consumption').value;
            var rate = document.getElementById('rate').value;

            if (consumption === "" || rate === "") {
                alert("Please enter both consumption and rate values.");
                return;
            }

            consumption = parseFloat(consumption);
            rate = parseFloat(rate);

            var totalBill = consumption * rate;

            var resultElement = document.getElementById('result');
            resultElement.innerHTML = "Your electricity bill is $" + totalBill.toFixed(2);
        }
    </script>

</body>
</html>

```

## OUTPUT:

![Screenshot 2023-12-28 035321](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/9c46390b-5226-40b4-a834-6d97df56bb6c)


## RESULT:
Thus the java code executed to calculate the electricity bill.

<br>
<br>

## (B)

## AIM:
To create a form with java script code to compute the factorial of a given number without recursion.

## DESIGNING PROCEDURE:
## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as show().

## STEP 4:
Give the necessary input that is require to compute the factorial like var i, n, fact. Get the number for input using document.getElementById.

## STEP 5:
Using for-loop condition calculate the factorial. Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 6 :
End the HTML structure.

## Code:
```
function calculateFactorial(number) {
    // Check if the input is a non-negative integer
    if (typeof number !== 'number' || number < 0 || !Number.isInteger(number)) {
        return "Invalid input. Please enter a non-negative integer.";
    }

    // Handle the special case of 0! (factorial of 0)
    if (number === 0) {
        return 1;
    }

    // Initialize the result to 1
    let result = 1;

    // Multiply numbers from 1 to the given number
    for (let i = 1; i <= number; i++) {
        result *= i;
    }

    return result;
}

// Example: Compute factorial of 5
const inputNumber = 5;
const result = calculateFactorial(inputNumber);

console.log(`The factorial of ${inputNumber} is: ${result}`);

```

## OUTPUT:

![Screenshot 2023-12-28 040019](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/43b2ed81-b041-4678-935b-fca7d8c98982)


## Result:
Thus the java code executed to compute the factorial of a given number without recursion.

<br>
<br>

## (C)
## AIM:
To construct a JavaScript code to generate ‘N’ prime numbers.

## DESIGNING PROCEDURE:
## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as show().

## STEP 4:
Give the necessary input that is required to construct a java code to generate ‘N’ prime numbers . Get the number for input using document.getElementById.

## STEP 5:
Using for-loop condition generate ‘N’ prime numbers. Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 7 :
End the HTML structure.

## Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prime Number Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
    </style>
</head>
<body>

    <h2>Prime Number Generator</h2>

    <label for="inputN">Enter the value of N:</label>
    <input type="number" id="inputN" placeholder="Enter a positive integer" min="1" required>
    <button onclick="generateAndDisplayPrimes()">Generate Primes</button>

    <div id="result"></div>

    <script>
        function generateAndDisplayPrimes() {
            const N = document.getElementById('inputN').value;

            if (N <= 0 || !Number.isInteger(Number(N))) {
                alert("Please enter a positive integer for N.");
                return;
            }

            const primes = generatePrimes(Number(N));

            const resultElement = document.getElementById('result');
            resultElement.innerHTML = `The first ${N} prime numbers are: ${primes.join(', ')}`;
        }

        function generatePrimes(N) {
            let primes = [];
            let number = 2;

            while (primes.length < N) {
                if (isPrime(number)) {
                    primes.push(number);
                }
                number++;
            }

            return primes;
        }

        function isPrime(num) {
            if (num <= 1) {
                return false;
            }

            for (let i = 2; i <= Math.sqrt(num); i++) {
                if (num % i === 0) {
                    return false;
                }
            }

            return true;
        }
    </script>

</body>
</html>

```

## OUTPUT:

![Screenshot 2023-12-28 040403](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/cec5ed2b-d2e5-4d25-bab6-cf11bc603f07)


## Result:

Thus the java code executed to construct a JavaScript code to generate ‘N’ prime numbers.

<br>
<br>

## (D)

## AIM:
To construct a JavaScript program to implement a simple calculator.

## DESIGNING PROCEDURE:
## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as function f1() for addition, function f2() for subtraction, function f3() for multiplication, function f4() for division, function f5() for sin(a), function f6() for cos(a) ,function f7() for tan(a), function f8() for a*a , function f9() for clear.

## STEP 4:
Give the necessary input that is required to implement a simple calculator. Get the number for input using document.getElementById.

## STEP 5:
Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 7 :
End the HTML structure.

## Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        input, button {
            margin: 5px;
            padding: 8px;
            font-size: 16px;
        }
    </style>
</head>
<body>

    <h2>Simple Calculator</h2>

    <label for="num1">Enter Number 1:</label>
    <input type="number" id="num1" placeholder="Enter a number" required>

    <label for="operator">Select Operator:</label>
    <select id="operator">
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">/</option>
    </select>

    <label for="num2">Enter Number 2:</label>
    <input type="number" id="num2" placeholder="Enter a number" required>

    <button onclick="calculate()">Calculate</button>

    <div id="result"></div>

    <script>
        function calculate() {
            const num1 = parseFloat(document.getElementById('num1').value);
            const num2 = parseFloat(document.getElementById('num2').value);
            const operator = document.getElementById('operator').value;

            if (isNaN(num1) || isNaN(num2)) {
                alert("Please enter valid numbers for calculation.");
                return;
            }

            let result;
            switch (operator) {
                case '+':
                    result = num1 + num2;
                    break;
                case '-':
                    result = num1 - num2;
                    break;
                case '*':
                    result = num1 * num2;
                    break;
                case '/':
                    if (num2 === 0) {
                        alert("Cannot divide by zero.");
                        return;
                    }
                    result = num1 / num2;
                    break;
                default:
                    alert("Invalid operator.");
                    return;
            }

            document.getElementById('result').innerHTML = `Result: ${result.toFixed(2)}`;
        }
    </script>

</body>
</html>

```
## OUTPUT:

![Screenshot 2023-12-28 040922](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/365d342c-391e-4b2f-ae13-17ad0afd1563)


## Result:

Thus the java code executed to implement a simple calculator.

<br>
<br>

## (E):

## AIM:
To design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

## DESIGNING PROCEDURE:
## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as function f1() for bold, function f2() for italics, function f3() for uppercase, function f4() for lowercase, function f5() for capitalize, function f6() for right ,function f7() for left, function f8() for center, function f9() for clear formatting.

## STEP 4:
Give the necessary input that is required to design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations. Get the number for input using document.getElementById.

## STEP 5:
Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 7 :
End the HTML structure.

## Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Text Editor</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        textarea {
            width: 100%;
            height: 100px;
            margin-bottom: 10px;
            font-size: 16px;
            padding: 5px;
        }
        button {
            font-size: 16px;
            padding: 8px;
            margin-right: 10px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <h2>Simple Text Editor</h2>

    <textarea id="textInput" placeholder="Enter text..."></textarea>

    <button onclick="capitalizeText()">Capitalize</button>
    <button onclick="reverseText()">Reverse</button>
    <button onclick="clearText()">Clear</button>

    <div id="result"></div>

    <script>
        function capitalizeText() {
            const inputText = document.getElementById('textInput').value;
            const capitalizedText = inputText.toUpperCase();
            displayResult(capitalizedText);
        }

        function reverseText() {
            const inputText = document.getElementById('textInput').value;
            const reversedText = inputText.split('').reverse().join('');
            displayResult(reversedText);
        }

        function clearText() {
            document.getElementById('textInput').value = '';
            document.getElementById('result').innerHTML = '';
        }

        function displayResult(resultText) {
            document.getElementById('result').innerHTML = `<strong>Result:</strong><br>${resultText}`;
        }

```

## OUTPUT:

![Screenshot 2023-12-28 041427](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/f7337d3c-96cb-405c-b0da-4911b00d161e)


## Result:

Thus the java code executed to design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.+


## (F)

## AIM:
To design a JavaScript program which displays error messages when a field in form is entered incorrectly.

## DESIGNING PROCEDURE:
## STEP 1:
Start define the document as HTML.

## STEP 2:
Open the HTML structure with necessary head and body .Give the script type as text/javascript.

## STEP 3:
Define the function for the program as validate().

## STEP 4:
Give the necessary input that is required to design a JavaScript program which displays error messages when a field in form is entered incorrectly.Get the number for input using document.getElementById.

## STEP 5:
Using for-loop condition and if-else condition displays error messages when a field in form is entered incorrectly. Close the script and head tags.

## STEP 6:
Give the input type in the body of the HTML.

## STEP 7:
End the HTML structure.


## Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Form Validation</title>
  <style>
    .error-message {
      color: red;
    }
  </style>
</head>
<body>

  <form id="myForm">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username">
    <div id="usernameError" class="error-message"></div>

    <br>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    <div id="emailError" class="error-message"></div>

    <br>

    <input type="submit" value="Submit">
  </form>

  <script>
    document.getElementById('myForm').addEventListener('submit', function(event) {
      // Reset error messages
      document.getElementById('usernameError').textContent = '';
      document.getElementById('emailError').textContent = '';

      // Validate username
      const username = document.getElementById('username').value.trim();
      if (username === '') {
        document.getElementById('usernameError').textContent = 'Username is required.';
        event.preventDefault();
      }

      // Validate email
      const email = document.getElementById('email').value.trim();
      const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRegex.test(email)) {
        document.getElementById('emailError').textContent = 'Enter a valid email address.';
        event.preventDefault();
      }
    });
  </script>

</body>
</html>

```

## OUTPUT:

![Screenshot 2023-12-30 050937](https://github.com/Yt8md/ODD23-24-WT-JavaScript/assets/144443644/d6f92af4-4c78-4713-9cae-8264e9d52ec6)


## Result:
Thus the java code executed to design a JavaScript program which displays error messages when a field in form is entered incorrectly.
