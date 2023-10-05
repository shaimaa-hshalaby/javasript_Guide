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
