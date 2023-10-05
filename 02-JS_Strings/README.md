## JS Strings

### Creating Strings

You can create strings in JavaScript using single or double quotes. Here's how you can create strings:

```javascript
let singleQuotedString = 'This is a single-quoted string.';
let doubleQuotedString = "This is a double-quoted string.";
```

You can also create strings using the `String` constructor:

```javascript
let stringConstructed = new String("This is a constructed string.");
```

However, using quotes is the more common and convenient way to create strings.
---------------------
### String Length

You can find the length of a string using the `length` property:

```javascript
let text = "Hello, World!";
let length = text.length; // length is 13
```
------------------------
### String Concatenation

#### Using `+` Operator:
You can concatenate (combine) strings using the `+` operator:

```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = firstName + " " + lastName; // fullName is "John Doe"
```

#### Using Template Literals (Backticks):

Template literals, enclosed in backticks (\`), allow you to embed variables and expressions directly within the string using `${}`:

```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = `${firstName} ${lastName}`; // fullName is "John Doe"
```

Template literals also support multiline strings, making them a powerful choice for string concatenation and formatting. 

-------------------------------
### String Methods

JavaScript provides numerous built-in methods for working with strings. Here are some commonly used string methods:

#### 1. `toUpperCase()` and `toLowerCase()`

```javascript
let text = "Hello, World!";
let uppercaseText = text.toUpperCase(); // uppercaseText is "HELLO, WORLD!"
let lowercaseText = text.toLowerCase(); // lowercaseText is "hello, world!"
```

#### 2. `charAt()` and `charCodeAt()`

`charAt()` returns the character at a specified index, and `charCodeAt()` returns the Unicode value (ASCII code) of the character at that index:

```javascript
let text = "Hello, World!";
let charAtIndex2 = text.charAt(2); // charAtIndex2 is "l"
let charCodeAtIndex2 = text.charCodeAt(2); // charCodeAtIndex2 is 108
```

#### 3. `substring()`

`substring()` extracts a portion of the string between two specified indices:

```javascript
let text = "Hello, World!";
let substring = text.substring(0, 5); // substring is "Hello"
```

#### 4. `indexOf()` and `lastIndexOf()`

`indexOf()` finds the first occurrence of a substring, and `lastIndexOf()` finds the last occurrence:

```javascript
let text = "Hello, World!";
let firstIndex = text.indexOf("o"); // firstIndex is 4
let lastIndex = text.lastIndexOf("o"); // lastIndex is 7
```

#### 5. `split()`

`split()` splits a string into an array of substrings based on a specified separator:

```javascript
let text = "apple,banana,cherry";
let fruits = text.split(","); // fruits is ["apple", "banana", "cherry"]
```

#### 6. `replace()`

`replace()` replaces a specified substring with another string:

```javascript
let text = "Hello, World!";
let newText = text.replace("World", "Universe"); // newText is "Hello, Universe!"
```

#### 7. `trim()`

`trim()` removes whitespace (spaces, tabs, and line breaks) from the beginning and end of a string:

```javascript
let text = "   Hello, World!   ";
let trimmedText = text.trim(); // trimmedText is "Hello, World!"
```

-------------------------------------------------
## Exercises

### Exercise 1: String Creation

1. Create a JavaScript string variable named `myString` and assign it the value "Hello, World!".

### Exercise 2: String Length

1. Write a JavaScript function that takes a string as an argument and returns its length. Test it with the `myString` variable.

### Exercise 3: String Concatenation

1. Declare two JavaScript variables, `firstName` and `lastName`, and assign them your first name and last name as strings. Use string concatenation to create a full name and display it.

### Exercise 4: Template Literals

1. Rewrite the previous exercise using template literals to create the full name.

### Exercise 5: Uppercase and Lowercase

1. Create a JavaScript function that takes a string as input and returns the same string in all uppercase letters. Test it with a sample string "This is an Example String."
2. Create another JavaScript function that takes a string as input and returns the same string in all lowercase letters. Test it with a sample string "JavaScript Exercises Are Fun!".

### Exercise 6: Substring

1. Write a JavaScript function that extracts a substring from a given string. The function should take the original string, a starting index, and an ending index as parameters and return the extracted substring.
Test it with a sample string "JavaScript is a powerful scripting language."
find the substring between the indices 11 & 20

### Exercise 7: Index of and Last Index Of

1. Create a JavaScript function that finds and returns the index of the first occurrence of a specific character in a string. Test it with a sample string and character.
9. Write another JavaScript function that finds and returns the index of the last occurrence of a specific character in a string. Test it with a sample string and character.

### Exercise 8: String Split

10. Create a JavaScript function that splits a given string into an array of words. The function should take the original string and a separator (e.g., space) as parameters and return the array of words.

### Exercise 9: String Replace

11. Write a JavaScript function that replaces all occurrences of a specific word in a string with another word. Test it with a sample string and words.

### Exercise 10: String Trimming

12. Create a JavaScript function that removes all leading and trailing spaces from a given string. Test it with a sample string containing extra spaces.

These exercises cover various aspects of JavaScript strings, from basic string manipulation to more advanced operations. They should help reinforce the concepts you've learned in the tutorial.
