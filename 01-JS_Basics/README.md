## How to add Javascript to HTML?

There are several ways to add JavaScript to an HTML document

1. **Inline JavaScript:**
   Inline JavaScript involves placing JavaScript code directly within the HTML document using the `<script>` tag. This method is straightforward but not recommended for large scripts or maintaining clean code.

   ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>Inline JavaScript</title>
     </head>
     <body>
         <h1>Hello, World!</h1>
         <script>
             // Inline JavaScript code
             alert("This is an inline JavaScript alert!");
         </script>
     </body>
     </html>
   ```

2. **Internal JavaScript:**
   In this method, you include JavaScript code within the HTML file using the `<script>` tag, but the code is placed in the `<head>` or at the end of the `<body>` section, separate from the HTML content.

   ```html
     <!DOCTYPE html>
     <html>
     <head>
         <title>Internal JavaScript</title>
         <script>
             // Internal JavaScript code in the <head>
             function showMessage() {
                 alert("This is an internal JavaScript alert!");
             }
         </script>
     </head>
     <body>
         <h1>Hello, World!</h1>
         <button onclick="showMessage()">Click Me</button>
     </body>
     </html>
   ```

3. **External JavaScript:**
   In this approach, you place your JavaScript code in a separate external file (e.g., `script.js`) and then link it to your HTML document using the `<script>` tag. This is a clean and maintainable way to add JavaScript to your website.

   **index.html:**
   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>External JavaScript</title>
       <script src="script.js"></script>
   </head>
   <body>
       <h1>Hello, World!</h1>
       <button onclick="showMessage()">Click Me</button>
   </body>
   </html>
   ```

   **script.js:**
   ```javascript
   // External JavaScript code in script.js
   function showMessage() {
       alert("This is an external JavaScript alert!");
   }
   ```

4. **Event Listeners (Modern Approach):**
   Instead of using inline `onclick` attributes, you can attach event listeners in an external JavaScript file. This method separates HTML and JavaScript completely and is more maintainable for larger projects.

   **index.html:**
   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>Event Listeners</title>
   </head>
   <body>
       <h1>Hello, World!</h1>
       <button id="myButton">Click Me</button>
       <script src="script.js"></script>
   </body>
   </html>
   ```

   **script.js:**
   ```javascript
   // External JavaScript code in script.js
   document.getElementById('myButton').addEventListener('click', function () {
       alert("This is an event listener JavaScript alert!");
   });
   ```

Choose the method that best suits your project's needs and helps maintain code cleanliness and organization. External JavaScript files and event listeners are commonly used in modern web development for better maintainability and scalability.

---------------------------------------------

### What is a Variable?

In JavaScript, a variable is a container that holds data.
Variables allow you to store, access, and manipulate values or objects. You can think of them as named placeholders for data.

### Declaring Variables

There are three ways to declare variables in JavaScript:

1. **Using `var`:**
   `var` is the older way to declare variables in JavaScript. While it's still valid, it's less commonly used in modern JavaScript because it has some scope-related quirks.

   ```javascript
   var myVar = 42;
   ```

2. **Using `let`:**
   `let` is introduced in ES6 (ECMAScript 2015) and is the preferred way to declare variables for most use cases. It has block-level scope.

   ```javascript
   let myVar = 42;
   ```

3. **Using `const`:**
   `const` is also introduced in ES6 and is used to declare variables whose values should not change after assignment. It also has block-level scope.

   ```javascript
   const myVar = 42;
   ```

### Variable Naming Rules

When naming variables in JavaScript, follow these rules:

- Variable names are case-sensitive (`myVar` is different from `myvar`).
- Variable names must start with a letter, underscore (_), or dollar sign ($).
- After the initial character, variable names can contain letters, numbers, underscores, and dollar signs.
- Avoid using reserved words (e.g., `function`, `if`, `else`, `while`, etc.) as variable names.

### Assigning Values

You can assign values to variables when declaring them or later in your code:

```javascript
let myVar; // Declare myVar without assigning a value
myVar = 42; // Assign the value 42 to myVar
```

You can also declare and assign a value in one line:

```javascript
let myVar = 42; // Declare and assign myVar in one step
```

### Data Types

JavaScript is a loosely typed language, which means variables can hold values of different data types. Common data types include:

- **Number:** Used for numeric values (e.g., `let age = 25;`).
- **String:** Used for text (e.g., `let name = "John";`).
- **Boolean:** Used for true/false values (e.g., `let isStudent = true;`).
- **Array:** Used for ordered collections of values (e.g., `let colors = ["red", "green", "blue"];`).
- **Object:** Used for key-value pairs and more complex data structures (e.g., `let person = { name: "Alice", age: 30 };`).

### Scope

The scope of a variable defines where it's accessible in your code. Variables declared with `var` have function-level scope, while variables declared with `let` or `const` have block-level scope.

```javascript
if (true) {
   var x = 10; // x is accessible outside the if block
   let y = 20; // y is only accessible inside the if block
}

console.log(x); // 10
console.log(y); // ReferenceError: y is not defined
```

------------------------------------
## JS Operators

JavaScript operators are symbols or keywords used for performing operations on values or variables. 
In this tutorial, we'll cover the most common JavaScript operators and how to use them.

### 1. Arithmetic Operators

Arithmetic operators perform mathematical operations on numbers:

- **Addition (+):** Adds two or more values.
  ```javascript
  let result = 5 + 3; // result is 8
  ```

- **Subtraction (-):** Subtracts the second operand from the first.
  ```javascript
  let result = 10 - 3; // result is 7
  ```

- **Multiplication (*):** Multiplies two or more values.
  ```javascript
  let result = 4 * 6; // result is 24
  ```

- **Division (/):** Divides the first operand by the second.
  ```javascript
  let result = 12 / 4; // result is 3
  ```

- **Modulus (%):** Returns the remainder after division.
  ```javascript
  let result = 17 % 5; // result is 2
  ```

### 2. Comparison Operators

Comparison operators compare values and return a Boolean result (true or false):

- **Equal (==):** Checks if two values are equal.
  ```javascript
  let isEqual = 5 == 5; // isEqual is true
  ```

- **Not Equal (!=):** Checks if two values are not equal.
  ```javascript
  let isNotEqual = 5 != 3; // isNotEqual is true
  ```

- **Strict Equal (===):** Checks if two values are equal without type conversion (strict equality).
  ```javascript
  let isStrictEqual = 5 === "5"; // isStrictEqual is false
  ```

- **Strict Not Equal (!==):** Checks if two values are not equal without type conversion (strict inequality).
  ```javascript
  let isStrictNotEqual = 5 !== "5"; // isStrictNotEqual is true
  ```

- **Greater Than (>):** Checks if the first value is greater than the second.
  ```javascript
  let isGreaterThan = 10 > 5; // isGreaterThan is true
  ```

- **Less Than (<):** Checks if the first value is less than the second.
  ```javascript
  let isLessThan = 3 < 7; // isLessThan is true
  ```

### 3. Logical Operators

Logical operators are used to combine or manipulate Boolean values:

- **AND (&&):** Returns true if both operands are true.
  ```javascript
  let isTrue = true && true; // isTrue is true
  ```

- **OR (||):** Returns true if at least one operand is true.
  ```javascript
  let isTrue = true || false; // isTrue is true
  ```

- **NOT (!):** Negates a Boolean value.
  ```javascript
  let isFalse = !true; // isFalse is false
  ```

### 4. Assignment Operators

Assignment operators assign values to variables:

- **Assignment (=):** Assigns a value to a variable.
  ```javascript
  let x = 10;
  ```

- **Addition Assignment (+=):** Adds a value to a variable and assigns the result.
  ```javascript
  let x = 5;
  x += 3; // x is now 8
  ```

- **Subtraction Assignment (-=):** Subtracts a value from a variable and assigns the result.
  ```javascript
  let x = 10;
  x -= 4; // x is now 6
  ```

### 5. Other Operators

JavaScript also includes other operators, such as the ternary operator (`? :`), which is a shorthand for an `if...else` statement, and the typeof operator, which checks the data type of a value.

- **Ternary Operator (conditional operator):**
  ```javascript
  let age = 18;
  let message = age >= 18 ? "Adult" : "Minor";
  ```

- **typeof Operator:**
  ```javascript
  let x = 5;
  let type = typeof x; // type is "number"
  ```
