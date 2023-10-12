# JavaScript Objects

In JavaScript, objects are a fundamental data type that allows you to store and organize data in a structured way. 
Objects are used to represent real-world entities and their properties, making them a powerful tool for creating complex data structures.
In this comprehensive guide, we will explore everything you need to know about JavaScript objects, from the basics to advanced concepts.

## 1. Introduction to JavaScript Objects

At its core, an object in JavaScript is an unordered collection of key-value pairs.
These key-value pairs are called properties, where the keys are strings, and the values can be any data type, including other objects. 
Objects are used to model and represent real-world entities and concepts in your code.

Here's a basic example of an object representing a person:

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
    age: 30,
    hobbies: ["Reading","Coding"],
    isStudent: false,
};
```

In this example, `person` is an object with five properties: `firstName`, `lastName`, `age`, `hobbies` and `isStudent`.

## 2. Creating Objects

JavaScript offers several ways to create objects. Let's explore three common methods:

### Object Literal

The simplest way to create an object is by using the object literal notation:

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
};
```

### Constructor Function

You can create objects using constructor functions, which are like blueprints for objects. Here's an example:

```javascript
function Person(firstName, lastName) {
    this.firstName = firstName;
    this.lastName = lastName;
}

const john = new Person("John", "Doe");
```

### ES6 Class

With ES6, you can use classes to create objects in a more structured way. Here's an example:

```javascript
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
}

const john = new Person("John", "Doe");
```

## 3. Accessing Object Properties

You can access object properties using dot notation or square brackets:

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
};

console.log(person.firstName); // "John"
console.log(person["lastName"]); // "Doe"
```

## 4. Modifying Object Properties

You can modify object properties by assigning new values to them:

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
};

person.lastName = "Smith";
console.log(person.lastName); // "Smith"
```

## 5. Adding and Deleting Properties

You can add new properties to an object and delete existing ones:

```javascript
const person = {
    firstName: "John",
};

person.lastName = "Doe";
console.log(person.lastName); // "Doe"

delete person.firstName;
console.log(person.firstName); // undefined
```

## 6. Object Methods

Objects can also contain functions as properties, known as methods:

```javascript
const person = {
    firstName: "John",
    sayHello: function () {
        console.log(`Hello, my name is ${this.firstName}`);
    },
};

person.sayHello(); // "Hello, my name is John"
```

## 7. Looping Through Objects

You can iterate through an object's properties using `for...in` loops:

```javascript
const person = {
    firstName: "John",
    lastName: "Doe",
};

for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}
```
---------------------------------------------------------------------
## Exercises


### Exercise 1: Create an Object
Create an object called `book` that represents a book with the following properties:
- `title` (string)
- `author` (string)
- `publishedYear` (number)
- `isAvailable` (boolean)

### Exercise 2: Access and Modify Properties

Using the `book` object from Exercise 1, perform the following tasks:
- Access and log the `author` property to the console.
- Change the `publishedYear` to the current year.
- Log the updated `book` object to the console.

### Exercise 3: Add and Delete Properties

Starting with the `book` object, add a new property called `genre` (string) representing the book's genre. Then, delete the `isAvailable` property. Log the modified `book` object to the console.

### Exercise 4: Object Methods

Create an object named `car` with the following properties:
- `make` (string)
- `model` (string)
- `year` (number)
- `startEngine` (a function that logs "Engine started" to the console)

Call the `startEngine` method on the `car` object to start the engine.

### Exercise 5: Loop Through Properties

Create an object called `person` with various properties (e.g., name, age, address). Use a `for...in` loop to iterate through the properties of the `person` object and log each property and its value to the console.

### Exercise 6: Object Constructors

Define an object constructor function `Product` that represents a product with the following properties:
- `name` (string)
- `price` (number)
- `description` (string)

Create three instances of the `Product` object with different values and store them in an array. Loop through the array and log each product's details to the console.

-----------------------------------------------------------------------
## To do
8. Object Prototypes
9. Object Inheritance
10. 10. Object Serialization
