# JavaScript Control Structures Tutorial

Control structures in JavaScript allow you to dictate the flow of your code. They are essential for making decisions, looping through data, and creating more dynamic and interactive programs. In this tutorial, we'll explore the various control structures available in JavaScript, including conditional statements and loops.

## Table of Contents

1. **Conditional Statements**
   - `if` statement
   - `else` statement
   - `else if` statement
   - `switch` statement

2. **Loops**
   - `for` loop
   - `while` loop
   - `do...while` loop
   - `for...in` loop
   - `for...of` loop

### 1. Conditional Statements

#### `if` statement

The `if` statement is used to execute a block of code if a specified condition is true.

```javascript
if (condition) {
  // Code to execute if the condition is true
}
```

Example:

```javascript
const age = 18;
if (age >= 18) {
  console.log("You are an adult.");
}
```

#### `else` statement

The `else` statement is used in conjunction with the `if` statement to specify a block of code that should be executed when the condition is false.

```javascript
if (condition) {
  // Code to execute if the condition is true
} else {
  // Code to execute if the condition is false
}
```

Example:

```javascript
const age = 15;
if (age >= 18) {
  console.log("You are an adult.");
} else {
  console.log("You are a minor.");
}
```

#### `else if` statement

The `else if` statement is used to check multiple conditions in a sequence. It is often used after an initial `if` statement.

```javascript
if (condition1) {
  // Code to execute if condition1 is true
} else if (condition2) {
  // Code to execute if condition2 is true
} else {
  // Code to execute if none of the conditions are true
}
```

Example:

```javascript
const grade = 85;
if (grade >= 90) {
  console.log("A");
} else if (grade >= 80) {
  console.log("B");
} else {
  console.log("C or below");
}
```

#### `switch` statement

The `switch` statement is used to select one of many code blocks to be executed.

```javascript
switch (expression) {
  case value1:
    // Code to execute if expression is equal to value1
    break;
  case value2:
    // Code to execute if expression is equal to value2
    break;
  // Additional cases...
  default:
    // Code to execute if none of the cases match
}
```

Example:

```javascript
const day = "Monday";
switch (day) {
  case "Monday":
    console.log("It's the start of the week.");
    break;
  case "Friday":
    console.log("It's almost the weekend!");
    break;
  default:
    console.log("It's a regular day.");
}
```

### 2. Loops

#### `for` loop

The `for` loop is used to execute a block of code a specific number of times.

```javascript
for (initialization; condition; iteration) {
  // Code to execute in each iteration
}
```

Example:

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // Outputs 0, 1, 2, 3, 4
}
```

#### `while` loop

The `while` loop is used to execute a block of code as long as a specified condition is true.

```javascript
while (condition) {
  // Code to execute as long as the condition is true
}
```

Example:

```javascript
let count = 0;
while (count < 5) {
  console.log(count); // Outputs 0, 1, 2, 3, 4
  count++;
}
```

#### `do...while` loop

The `do...while` loop is similar to the `while` loop, but it always executes the code block at least once, even if the condition is initially false.

```javascript
do {
  // Code to execute at least once
} while (condition);
```

Example:

```javascript
let num = 0;
do {
  console.log(num); // Outputs 0
  num++;
} while (num < 0);
```

#### `for...in` loop

The `for...in` loop is used to iterate over the properties of an object.

```javascript
for (variable in object) {
  // Code to execute for each property
}
```

Example:

```javascript
const person = { name: "John", age: 30 };
for (let key in person) {
  console.log(key, person[key]); // Outputs "name John" and "age 30"
}
```

#### `for...of` loop

The `for...of` loop is used to iterate over the values of iterable objects like arrays and strings.

```javascript
for (variable of iterable) {
  // Code to execute for each value
}
```

Example:

```javascript
const colors = ["red", "green", "blue"];
for (let color of colors) {
  console.log(color); // Outputs "red", "green", "blue"
}
```

That concludes our tutorial on JavaScript control structures. These structures are fundamental for creating dynamic and interactive applications. Experiment with these concepts to gain a better understanding of how they work and how they can be applied to real-world programming scenarios.
