# JavaScript Error Handling Tutorial

Error handling is a crucial aspect of JavaScript programming, as it allows you to gracefully deal with unexpected situations and exceptions that can occur during the execution of your code.
This tutorial will guide you through the fundamentals of error handling in JavaScript, including how to handle different types of errors and best practices for effective error management.

## Table of Contents

1. **Introduction to Error Handling**
2. **Types of JavaScript Errors**
   - Syntax Errors
   - Runtime Errors
   - Logical Errors
3. **Using the `try...catch` Statement**
4. **Throwing Custom Errors**
5. **Best Practices for Error Handling**
6. **Common Error Handling Patterns**

## 1. Introduction to Error Handling

Error handling is the process of detecting, managing, and recovering from errors or exceptions that may occur in your JavaScript code. Errors can be triggered by a variety of factors,
such as invalid data, unexpected conditions, or issues with external resources (e.g., network requests).
Proper error handling is essential for creating robust and user-friendly applications. When an error occurs, it should be handled in a way that provides feedback to the developer
for debugging and presents a user-friendly message to end-users.

## 2. Types of JavaScript Errors

### Syntax Errors

Syntax errors are the most straightforward type of error. They occur when you violate the rules of the JavaScript language. These errors prevent your code from running at all. 
Common causes include missing parentheses, unmatched braces, or typos.

```javascript
function sayHello() {
  console.log("Hello, world!)
}
```

### Runtime Errors

Runtime errors, also known as exceptions, occur during the execution of your code. They can be caused by various issues, such as trying to access an undefined variable,
dividing by zero, or calling a method on an object that doesn't exist.

```javascript
let x;
console.log(x.toUpperCase()); // TypeError: Cannot read property 'toUpperCase' of undefined
```

### Logical Errors

Logical errors are more challenging to detect because they don't result in error messages. Instead, your code may produce incorrect or unexpected results due to flawed logic 
in your program.

```javascript
function add(a, b) {
  return a - b; // Logical error: subtracts instead of adding
}
```

## 3. Using the `try...catch` Statement

JavaScript provides the `try...catch` statement for handling runtime errors. This statement allows you to wrap potentially error-prone code in a `try` block and specify 
how to handle errors in a corresponding `catch` block.

```javascript
try {
  // Code that may cause an error
} catch (error) {
  // Handle the error
  console.error("An error occurred:", error);
}
```

In this example, if an error occurs within the `try` block, it will be caught by the `catch` block, and you can handle it appropriately.
You can access error information via the `error` parameter in the `catch` block.

## 4. Throwing Custom Errors

While JavaScript provides built-in error types like `SyntaxError` and `TypeError`, you can also create custom errors using the `Error` constructor.
Custom errors allow you to provide more descriptive information about the error.

```javascript
function divide(a, b) {
  if (b === 0) {
    throw new Error("Division by zero is not allowed.");
  }
  return a / b;
}
```

In this example, we've created a custom error message to clarify why the division operation failed.

### Here's a full example that demonstrates the concepts of custom error and error handling:

```javascript
// Example: Error Handling in JavaScript

// Function to divide two numbers
function divide(a, b) {
  try {
    if (b === 0) {
      throw new Error("Division by zero is not allowed.");
    }
    return a / b;
  } catch (error) {
    // Handle the error gracefully
    console.error("An error occurred:", error.message);
    return NaN; // Return a safe default value
  }
}

// Example usage
console.log("Result:", divide(10, 2)); // Result: 5
console.log("Result:", divide(8, 0));  // An error occurred: Division by zero is not allowed. Result: NaN
console.log("Result:", divide(6, 3));  // Result: 2

```


## 5. Best Practices for Error Handling

Effective error handling is essential for robust code. Here are some best practices to follow:

- **Use Descriptive Error Messages**: Make error messages as informative as possible to aid debugging.

- **Avoid Silent Failures**: Never ignore errors or allow your code to continue executing when an error occurs. Silent failures can lead to unpredictable behavior.

- **Log Errors**: Use `console.error()` to log error details, making it easier to diagnose issues during development.

- **Handle Errors Gracefully**: When possible, recover from errors gracefully so that your application can continue to function. This might involve providing default values,
- retrying operations, or notifying the user.

- **Use Custom Errors**: Create custom error types when needed to provide more context and make error handling more specific.

- **Test Error Scenarios**: Write test cases that cover error scenarios to ensure your error handling works as expected.

--------------------------------------------
## Exercises

**Exercise 1:** Syntax Errors

Identify and correct the syntax errors in the following code snippets:

```javascript
a = 5;
console.log("Hello, world!)
if (x > 10 {
  console.log("x is greater than 10.");
}
```

**Exercise 2:** Runtime Errors

1. Write code that triggers a runtime error (e.g., a `TypeError`, `ReferenceError`, or any other runtime error) and explain what caused the error.

2. Write code that attempts to divide a number by zero and handle this error gracefully using a `try...catch` statement.

**Exercise 3:** Logical Errors

Identify the logical errors in the following code and correct them:

```javascript
function calculateTotal(price, taxRate) {
  return price + taxRate; // Logical error: Incorrect tax calculation
}
```

**Exercise 4:** Error Handling

1. Write a function that takes two parameters and attempts to divide them. Handle any division by zero errors using a `try...catch` statement and return a custom error message if the denominator is zero.

2. Create a custom error type named `NetworkError` and write a function that simulates a network request. If the request fails, throw a `NetworkError` with a descriptive message.

3. Write a function that calculates the factorial of a number. Handle invalid inputs (negative numbers) by throwing a custom error.

**Exercise 5:** Best Practices

For each of the following scenarios, explain which best practices for error handling are violated and how they can be improved:

Scenario 1: An application silently fails when a database connection fails, and no error message is logged.

Scenario 2: An application displays technical error messages to end-users, exposing internal details.

Scenario 3: A developer uses generic error messages like "An error occurred" without providing specific information.

Feel free to work through these exercises and check your solutions against the concepts covered in the tutorial. Error handling is an essential skill in JavaScript programming, and these exercises will help reinforce your knowledge.

## To do
-   Promises and Async/Await
-   Error Codes
