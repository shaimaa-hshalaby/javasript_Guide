## Understanding Variable Scopes in JavaScript

In JavaScript, variable scope determines where a variable can be accessed within your code. Variables in JavaScript can have one of several scopes, which include:

### Global Scope
  Variables declared at the top level of your JavaScript file or within an HTML `<script>` tag have global scope. 
  They are accessible from anywhere in your code, including inside functions or nested scopes.

  
  ```javascript
    var globalVar = "I am a global variable";
    
    function exampleFunction() {
        console.log(globalVar); // Accessible inside the function
    }
    
    console.log(globalVar); // Accessible outside the function
  ```
  
  Global variables can be accessed and modified from any part of your code, but they can also introduce potential issues related to naming conflicts and code maintainability.

#### Function Scope
  Variables declared inside a function, Each function creates a new scope. 
  They are accessible only within that specific function and are not visible outside of it.
  Variables declared with var, let and const are quite similar when declared inside a function.

  ```javascript
    function exampleFunction() {
        var localVar = "I am a function-scoped variable";
        console.log(localVar); // Accessible inside the function
    }
    
    console.log(localVar); // Throws an error: localVar is not defined
  ```
  
  Variables declared with `var` inside a function have local scope, which means they are isolated from the global scope and cannot be accessed outside of the function.

#### Block Scope (Introduced in ES6)
  Variables declared inside a block using `let` or `const` are block-scoped.
  A block is typically defined by a set of curly braces `{}` and can include if statements, loops, or any other code enclosed within braces.
  Block-scoped variables are accessible only within the block in which they are declared.

    
  ```javascript
    if (true) {
        let blockVar = "I am a block-scoped variable";
        console.log(blockVar); // Accessible inside the block
    }
    
    console.log(blockVar); // Throws an error: blockVar is not defined
  ```
  
  Block-scoped variables provide better control over variable visibility and help prevent issues related to variable hoisting.

----------------------------------------

## Exercises

### Exercise 1: Global Scope

1. Declare a global variable named `globalVar` and assign it a string value.
2. Write a function called `accessGlobalVar` that attempts to log the `globalVar` variable. Call this function both from within and outside another function. Observe the variable's accessibility.

### Exercise 2: Function Scope

1. Declare a function named `functionScopedExample`.
2. Inside `functionScopedExample`, declare a variable named `functionVar` and assign it a numeric value.
3. Try to access `functionVar` from outside the `functionScopedExample` function. What happens? Explain the result.

### Exercise 3: Block Scope (ES6)

1. Create an `if` statement with a block of code inside it.
2. Inside the block, declare a variable named `blockVar` using the `let` keyword and assign it a boolean value.
3. Try to access `blockVar` from outside the `if` statement. Explain the result.
4. Rewrite the same exercise using the `const` keyword instead of `let`. Observe any differences in variable accessibility.

### Exercise 4: Nested Scopes

1. Create a function called `outerFunction`.
2. Inside `outerFunction`, declare a variable named `outerVar` and assign it a string value.
3. Create another function called `innerFunction` inside `outerFunction`.
4. Inside `innerFunction`, try to log the `outerVar` variable. What happens? Explain the result.
