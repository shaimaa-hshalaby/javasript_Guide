# JavaScript Arrays

## 1. Introduction to Arrays

An array is a data structure that allows you to store a collection of items, such as numbers, strings, objects, or even other arrays.
Each item in an array is called an element, and each element is identified by an index, starting from 0.
Arrays are versatile and commonly used in JavaScript for tasks like storing lists of items, managing data, and iterating through collections.

## 2. Creating Arrays

### Array Literal

The simplest way to create an array is to use an array literal, which is defined by enclosing a comma-separated list of elements in square brackets `[]`.

```javascript
const fruits = ["apple", "banana", "cherry"];
```

### Array Constructor

You can also create an array using the `Array` constructor by calling it with or without arguments.

```javascript
const numbers = new Array(1, 2, 3); // With arguments
const emptyArray = new Array(); // Without arguments, creates an empty array
```

when you use the Array constructor with a single numeric argument, it's treated as the initial length of the array. The resulting array will have the specified length, but its elements will be initially empty (i.e., they will be set to undefined).

```javascript
const myArray = new Array(5);
console.log(myArray); // Outputs: [ , , , , ]
console.log(myArray.length); // Outputs: 5
```

### Array.from() Method

The `Array.from()` method allows you to create an array from an iterable object (e.g., a string, a set, a map, or an array-like object).

```javascript
const arrayFromStr = Array.from("Hello"); // Creates ["H", "e", "l", "l", "o"]
```

## 3. Array Elements

### Accessing Elements

You can access elements in an array using square brackets and the element's index.

```javascript
const fruits = ["apple", "banana", "cherry"];
const firstFruit = fruits[0]; // Access the first element (index 0)
const secondFruit = fruits[1]; // Access the second element (index 1)
```

### Modifying Elements

You can modify elements in an array by assigning a new value to a specific index.

```javascript
const fruits = ["apple", "banana", "cherry"];
fruits[1] = "orange"; // Change the second element
```

## 4. Array Properties

### Length

The `length` property of an array returns the number of elements in the array.

```javascript
const fruits = ["apple", "banana", "cherry"];
const numFruits = fruits.length; // numFruits is 3
```

## 5. Common Array Operations

### Adding Elements

- **Push**: Adds one or more elements to the end of an array.
  
  ```javascript
  const fruits = ["apple", "banana"];
  fruits.push("cherry"); // Adds "cherry" to the end
  ```

- **Unshift**: Adds one or more elements to the beginning of an array.

  ```javascript
  const fruits = ["banana", "cherry"];
  fruits.unshift("apple"); // Adds "apple" to the beginning
  ```

### Removing Elements

- **Pop**: Removes the last element from an array and returns it.

  ```javascript
  const fruits = ["apple", "banana", "cherry"];
  const removedFruit = fruits.pop(); // Removes "cherry" and returns it
  ```

- **Shift**: Removes the first element from an array and returns it.

  ```javascript
  const fruits = ["apple", "banana", "cherry"];
  const removedFruit = fruits.shift(); // Removes "apple" and returns it
  ```

### Searching and Filtering

- **Index of**: Returns the index of the first occurrence of an element in an array, or -1 if not found.

  ```javascript
  const fruits = ["apple", "banana", "cherry"];
  const index = fruits.indexOf("banana"); // index is 1
  ```

- **Filter**: Creates a new array with all elements that pass a test (provided as a function).

  ```javascript
  const numbers = [1, 2, 3, 4, 5];
  const evenNumbers = numbers.filter((num) => num % 2 === 0); // [2, 4]
  ```

### Sorting Arrays

- **Sort**: Sorts the elements of an array in place (mutates the original array).

  ```javascript
  const fruits = ["banana", "apple", "cherry"];
  fruits.sort(); // Sorts alphabetically: ["apple", "banana", "cherry"]
  ```

- **Reverse**: Reverses the order of elements in an array in place (mutates the original array).

  ```javascript
  const numbers = [1, 2, 3, 4, 5];
  numbers.reverse(); // Reverses the order: [5, 4, 3, 2, 1]
  ```

## 6. Iterating Through Arrays

### For Loop

You can iterate through an array using a `for` loop.

```javascript
const fruits = ["apple", "banana", "cherry"];
for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
```

### For...of Loop

The `for...of` loop is a more concise way  
 to iterate through arrays.

```javascript
const fruits = ["apple", "banana", "cherry"];
for (const fruit of fruits) {
    console.log(fruit);
}
```

### ForEach Method

The `forEach` method allows you to apply a function to each element of an array.

```javascript
const numbers = [1, 2, 3, 4, 5];
numbers.forEach((num) => {
    console.log(num);
});
```

### Map Method

The `map` method creates a new array by applying a function to each element of an existing array.

```javascript
const numbers = [1, 2, 3];
const doubledNumbers = numbers.map((num) => num * 2); // [2, 4, 6]
```

## 7. Multidimensional Arrays

A multidimensional array is an array of arrays. It allows you to create grids, tables, or matrices.

```javascript
const matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];
```

## 8. Array Methods

JavaScript provides various array methods for performing common operations on arrays. Here are a few essential ones:

### concat()

The `concat()` method combines two or more arrays and returns a new array.

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const combinedArray = arr1.concat(arr2); // [1, 2, 3, 4]
```

### join()

The `join()` method joins all elements of an array into a string, separated by a specified separator.

```javascript
const fruits = ["apple", "banana", "cherry"];
const fruitString = fruits.join(", "); // "apple, banana, cherry"
```

### slice()

-  The `slice()` method extracts a portion of an array into a new array without modifying the original array.
-  The slice(start,end) method selects from a given start, up to a (not inclusive) given end.
-  start is optional, the default is zero.
-  end is optional, the default is the last element.
-  a negative index can be used to indicate an offset from the end of the array. For example, -2 refers to the second to last element of the array.


```javascript
const numbers = [1, 2, 3, 4, 5];
const slicedArray = numbers.slice(1, 4); // [2, 3, 4]
```

### splice()

The `splice()` method can be used to add or remove elements from an array at a specified index.

```javascript
const numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 0, 6); // Inserts 6 at index 2
numbers.splice(3, 2); // Removes 2 elements starting from index 3
```

### push() and pop()

The `push()` method adds one or more elements to the end of an array, while the `pop()` method removes the last element from the end.

```javascript
const fruits = ["apple", "banana"];
fruits.push("cherry"); // Adds "cherry" to the end
const removedFruit = fruits.pop(); // Removes "cherry" and returns it
```

### shift() and unshift()

The `shift()` method removes the first element from the array, while the `unshift()` method adds one or more elements to the beginning.

```javascript
const fruits = ["banana", "cherry"];
fruits.unshift("apple"); // Adds "apple" to the beginning
const removedFruit = fruits.shift(); // Removes "apple" and returns it
```

### indexOf() and lastIndexOf()

The `indexOf()` method returns the first index at which a specified element is found in an array. The `lastIndexOf()` method returns the last index at which a specified element is found.

```javascript
const fruits = ["apple", "banana", "cherry", "banana"];
const firstBananaIndex = fruits.indexOf("banana"); // 1
const lastBananaIndex = fruits.lastIndexOf("banana"); // 3
```

## 9. Array Destructuring

Array destructuring allows you to extract values from arrays and assign them to variables in a concise way.

```javascript
const [first, second] = ["apple", "banana"];
console.log(first); // "apple"
console.log(second); // "banana"
```

## 10. Working with Arrays

### Copy an Array

To create a copy of an array that is independent of the original array, you can use the `slice()` method or the spread operator (`...`).

```javascript
const originalArray = [1, 2, 3];
const copyArray = originalArray.slice(); // Using slice
const spreadCopy = [...originalArray]; // Using spread operator
```

### Merge Arrays

To merge two or more arrays into a single array, you can use the `concat()` method or the spread operator (`...`).

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const mergedArray = arr1.concat(arr2); // Using concat
const spreadMerged = [...arr1, ...arr2]; // Using spread operator
```

### Reverse an Array

To reverse the order of elements in an array without modifying the original array, you can use the `reverse()` method or create a reversed copy.

```javascript
const originalArray = [1, 2, 3];
const reversedArray = originalArray.slice().reverse(); // Using slice and reverse
const spreadReversed = [...originalArray].reverse(); // Using spread and reverse
```

-----------------------------------------
## Exercises 

**Exercise 1: Accessing Elements**
- Given the array `[10, 20, 30, 40, 50]`, write a function that returns the first and last elements. For example, `getFirstAndLast([10, 20, 30, 40, 50])` should return `[10, 50]`.

**Exercise 2: Modifying Elements**
- Write a function that takes an array of strings like `["apple", "banana", "cherry"]` and capitalizes the first letter of each string. The result should be `["Apple", "Banana", "Cherry"]`.

**Exercise 3: Array Properties**
- Given the array `[12, 18, 24, 30, 36]`, write a function that calculates the average of all the numbers in the array. The result should be `24`.

**Exercise 4: Adding and Removing Elements**
- Create an array of your favorite colors, e.g., `["red", "blue", "green"]`. Write a function to add a new color "purple" to the beginning of the array. Then write another function to remove the last color from the array. The final array should be `["purple", "red", "blue"]`.

**Exercise 5: Searching and Filtering**
- Given the array `["Alice", "Bob", "Charlie", "David", "Eve"]`, write a function that checks if the name "Charlie" is in the array and returns `true`. For example, `isNameInArray(["Alice", "Bob", "Charlie", "David", "Eve"], "Charlie")` should return `true`.

**Exercise 6: Sorting Arrays**
- Write a function that sorts an array of numbers like `[5, 3, 8, 1, 4]` in ascending order. The result should be `[1, 3, 4, 5, 8]`.

**Exercise 7: Iterating Through Arrays**
- Given an array of student objects like `[{ name: "Alice", score: 90 }, { name: "Bob", score: 85 }, { name: "Charlie", score: 92 }]`, write a function that calculates the average score of all students. The result should be `89`.

**Exercise 8: Multidimensional Arrays**
- Create a 2D tic-tac-toe board as an array, where `X` represents X's move, `O` represents O's move, and `null` represents an empty cell. Write a function that checks if there's a winner (three X's or O's in a row, column, or diagonal). For example, given the board:
  ```
  [
    ["X", "O", null],
    ["X", "O", null],
    ["X", null, null]
  ]
  ```
  The function should return `"X"` as the winner.

**Exercise 9: Array Methods**
- Given an array of words like `["apple", "banana", "cherry"]`, write a function that returns a new array containing the lengths of the words. The result should be `[5, 6, 6]`.

**Exercise 10: Array Destructuring**
- Write a function that swaps the values of two elements in an array using destructuring. For example, given the array `[10, 20]`, the function should return `[20, 10]`.

**Exercise 11: Working with Arrays**
- Write a function that merges two sorted arrays like `[1, 3, 5]` and `[2, 4, 6]` into a single sorted array. The result should be `[1, 2, 3, 4, 5, 6]`.

**Exercise 12: Array of Objects**
- Create an array of objects representing books with properties like `title`, `author`, and `year`, e.g.,
  ```
  [
    { title: "Book1", author: "Author1", year: 2000 },
    { title: "Book2", author: "Author2", year: 1998 },
    { title: "Book3", author: "Author3", year: 2005 }
  ]
  ```
  Write a function that finds the oldest book in the array based on the `year` property. The result should be the book object with the oldest year.
