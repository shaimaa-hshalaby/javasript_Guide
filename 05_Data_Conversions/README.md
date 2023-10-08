

# JavaScript Data Conversion

In JavaScript, data conversion refers to the process of changing the data type of a value from one type to another. 
This process is essential for working with different data types, handling user inputs, and performing various operations. 
In this guide, we'll explore the various methods and techniques for data conversion in JavaScript.

## Type Coercion

Type Coercion refers to the process of automatic or implicit conversion of values from one data type to another.
This includes conversion from Number to String, String to Number, Boolean to Number etc. when different types of operators are applied to the values.

Type coercion in JavaScript:
```javascript
  const num = 5;
  const str = "10";
  
  const result = num + str; // Result is "510" (string concatenation)
```
> JS converts number to string with "+" operator as it is used as a concatenation operator, but it converts string to number with other operators

```javascript
  const num = 5;
  const str = "10";
  
  const result = num * str; // Result is "50" 
```

## Explicit Conversion (Type casting)

Explicit conversion, also known as type casting, is the intentional conversion of data types in JavaScript. 
Unlike type coercion, which is automatic, explicit conversion requires using functions or constructors to change data types.

### Using Functions

You can use various functions to explicitly convert data types in JavaScript. Here are some common conversion functions:

- `parseInt()`: Converts a string to an integer.
- `parseFloat()`: Converts a string to a floating-point number.
- `String()`: Converts a value to a string.
- `Number()`: Converts a value to a number.

Example using `parseInt()`:
```javascript
  const num = 5;
  const str = "10";
    
  const result = num +  parseInt(str);
  
  console.log(result); // Result is 15 (number)
```

### Using Constructors

JavaScript provides constructors for specific data types that allow you to create new instances with explicit type conversion:

- `new String()`: Creates a string object.
- `new Number()`: Creates a number object.
- `new Boolean()`: Creates a boolean object.

Example using constructors:
```javascript
const num = new Number(42);

console.log(num); // Result is 42 (number object)
```

## String to Number Conversion

Converting a string to a number is a common data conversion task in JavaScript. You can use functions like `parseInt()` and `parseFloat()` to achieve this.

Example using `parseFloat()`:
```javascript
  const str = "3.14";
  const num = parseFloat(str);
  
  console.log(num); // Result is 3.14 (number)
```

## Number to String Conversion

Converting a number to a string is also a common operation. You can use the `String()` function for this purpose.

Example using `String()`:
```javascript
const num = 42;
const str = String(num);

console.log(str); // Result is "42" (string)
```

## Boolean Conversion

JavaScript automatically converts values to boolean in certain contexts. Understanding how values are coerced to boolean is crucial.

Falsy values:
- `false`
- `0` and `-0`
- `NaN`
- `null`
- `undefined`
- An empty string (`""`)

Truthy values:
- All values not listed as falsy

Example:
```javascript
const value = "Hello";

if (value) {
    console.log("Truthy");
} else {
    console.log("Falsy");
}

// Result is "Truthy"
```

## Arrays and Objects

Arrays and objects can be converted to other data types as needed. To convert an array to a string, you can use the `join()` method. 
To convert an object to a string, you can use `JSON.stringify()`.

Array to String Example:
```javascript
const arr = [1, 2, 3];
const arrStr = arr.join(", "); // Converts the array to a string with commas

console.log(arrStr); // Result is "1, 2, 3"
```

Object to String Example:
```javascript
  // Create an object
  const person = {
      firstName: "John",
      lastName: "Doe",
      age: 30,
      isStudent: false
  };
  
  // Convert the object to a JSON string
  const jsonString = JSON.stringify(person);
  console.log(jsonString);
```


## Unary Plus Operator in JavaScript

-  In JavaScript, the unary plus operator (`+`) is a versatile and powerful tool for working with numbers.
-  The unary plus operator (`+`) is a simple yet powerful operator in JavaScript.
-  Its primary purpose is to convert values into numbers. Here's the basic syntax of the unary plus operator:

```javascript
+value
```

You place the `+` symbol before a value, and it tries to convert that value into a number. 
Depending on the input value, the unary plus operator can perform different tasks, as we'll explore in the following sections.

### Converting Strings to Numbers

One of the most common uses of the unary plus operator is to convert strings to numbers.
JavaScript allows you to concatenate strings with the `+` operator, but when you use it with a string that contains a valid numeric representation, it converts the string into a number.

```javascript
const numericString = "42";
const number = +numericString;

console.log(number); // Output: 42 (a numeric value)
```

In this example, the unary plus operator converts the string `"42"` into the numeric value `42`.


### Working with NaN

When you use the unary plus operator with a value that cannot be converted into a number, it results in `NaN` (Not-a-Number).

```javascript
const invalidValue = +"Hello";

console.log(invalidValue); // Output: NaN
```

In this example, the string `"Hello"` cannot be converted into a valid number, so the result is `NaN`.

### Converting Booleans to Numbers

You can also use the unary plus operator to convert booleans to numbers. `true` is converted to `1`, and `false` is converted to `0`.

```javascript
const trueBoolean = +true;
const falseBoolean = +false;

console.log(trueBoolean); // Output: 1
console.log(falseBoolean); // Output: 0
```

This can be useful when you need to perform numeric operations based on boolean conditions.

## Using `typeof` Operator

The `typeof` operator allows you to determine the data type of a value. It returns a string representing the data type.

Example:
```javascript
const value = 42;
const type = typeof value;

console.log(type); // Result is "number"
```

---------------------------------------------------

## Exercises

**Exercise 1:** Converting Strings to Numbers

Write a JavaScript function called `convertToNumber` that takes a string as input and uses the unary plus operator to convert it into a number. Test the function with various numeric string inputs.

**Exercise 2:** Handling Invalid Values

Write a function `handleInvalidValue` that takes a string as input and uses the unary plus operator to attempt conversion to a number. If the conversion results in `NaN`, return a custom error message; otherwise, return the converted number.

**Exercise 3:** Converting Booleans to Numbers

Design a function `convertBooleanToNumber` that takes a boolean value as input and uses the unary plus operator to convert it to a number (`1` for `true` and `0` for `false`). Test the function with various boolean inputs.

**Exercise 4:** Conversion in Real Scenarios

Imagine a scenario where you receive user input as strings, and you need to validate and convert them to numbers. Create a function `validateAndConvert` that takes a string as input, checks if it represents a valid number, and returns the number if valid or an error message if not. Use the unary plus operator for conversion.

**Exercise 6:** Advanced Conversion

Write a function `advancedConversion` that takes an input value and uses the unary plus operator to perform the following conversions:
- If the input is a numeric string, convert it to a number.
- If the input is a boolean, convert it to a number as described earlier.
- If the input is already a number, return it.
- For any other type of input, return `NaN`.

These exercises will help reinforce your understanding of data type conversion in JavaScript and how to use the unary plus operator effectively.
