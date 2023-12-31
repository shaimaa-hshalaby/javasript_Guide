## Browser API Term
The term "Browser API" refers to a set of interfaces and methods provided by web browsers to allow developers to interact with and manipulate web content, such as HTML, CSS, and JavaScript, within a web page. These APIs provide a way to access and control various aspects of web browsers and the Document Object Model (DOM) of web pages. They are essential for building web applications and enhancing user experiences.

The Most common categories of Browser APIs include:

**DOM API:** These APIs provide methods and objects for accessing and manipulating the DOM of a web page. Common DOM APIs include document, window, and the various methods for querying and manipulating elements in the DOM.

------------------------------------------

## Introduction to the Document Object Model (DOM)

The Document Object Model, commonly referred to as the DOM, is a fundamental concept in web development.
It is a powerful and interactive way to represent and manipulate web pages. Essentially, the DOM provides a structured, tree-like representation of an HTML or XML document,
allowing developers to access, modify, and interact with the content and structure of a web page using programming languages like JavaScript.

The DOM is a bridge between web content (e.g., HTML, XML) and programming languages, enabling developers to create dynamic, interactive web applications.
It provides a structured way to access and manipulate the elements and data on a web page, making it possible to respond to user interactions, update content dynamically,
and create rich, responsive user interfaces.

### Key concepts of the DOM include:

1. **Structured Tree:**
   The DOM represents a web page as a tree structure, where each element (e.g., HTML tags) is represented as a node, and these nodes are organized hierarchically.
2. **Access and Manipulation:**
    Developers can use the DOM to access and modify the properties, attributes, and content of elements on a web page, making it possible to create dynamic content and interactive features.
3. **Event Handling:**
   The DOM enables the registration of event listeners to respond to user actions, such as clicks, keypresses, and mouse movements, allowing for interactivity and user engagement.
4. **Cross-Browser Compatibility:**
   The DOM is supported by virtually all modern web browsers, making it a standard and widely used tool for web development. It provides a consistent way to interact with web content across different browsers.

--------------
## The difference between `document` & `window` 
In JavaScript, there are 2 main objects, `document` and `window` objects. they are part of the Document Object Model (DOM), but they serve different purposes and have distinct roles in a web page's structure and interaction.

**`document` Object:**

The `document` object represents the HTML document displayed in a web browser. It provides access to the content of the web page, allowing you to manipulate and interact with its elements.

- The `document` object is part of the DOM and primarily deals with the structure and content of the web page.
- It contains properties and methods for accessing and modifying HTML elements, such as forms, images, links, and text.
- You can use the `document` object to query and manipulate the DOM, including adding, modifying, or deleting elements on the web page.
- It does not represent the entire browser window but focuses on the content within that window.

**Example:**
```javascript
// Access an element by its ID
const element = document.getElementById("myElement");

// Change the text of an element
element.innerHTML = "New content";
```

**`window` Object:**

The `window` object represents the browser window or tab that contains the HTML document. It provides access to various properties and methods that control the browser's behavior and allow interaction with the environment outside the HTML document.

- The `window` object is the global object in the browser's JavaScript environment.
- It provides access to the browser's features, such as setting timeouts, intervals, navigating to URLs, and interacting with the browser history.
- You can also use the `window` object to access information about the user's screen, location, or browser settings.
- It's responsible for managing the browser's dimensions, frames, and interactions outside of the web page's content.

**Example:**
```javascript
// Open a new browser window
window.open("https://www.example.com");

// Set a timeout to execute a function after a delay
window.setTimeout(function() {
  console.log("Timeout executed");
}, 2000);
```

---------------------------------------------
## `document` common used properties

| Property                | Description                                          |
|-------------------------|------------------------------------------------------|
| `document.title`        | Gets or sets the title of the current document.     |
| `document.URL`          | Returns the full URL of the current document.       |
| `document.domain`       | Gets or sets the domain of the current document's URL. |
| `document.cookie`       | Gets or sets the cookies associated with the current document. |
| `document.documentElement` | Returns the root element of the document (usually `<html>`). |
| `document.body`         | Returns the `<body>` element of the document.       |
| `document.head`         | Returns the `<head>` element of the document.       |
| `document.location`     | Provides information about the URL and allows for navigation. |
| `document.referrer`     | Returns the URL of the document that referred to the current document. |
| `document.forms`        | Returns a collection of all `<form>` elements in the document. |
| `document.images`       | Returns a collection of all `<img>` elements in the document. |
| `document.links`        | Returns a collection of all `<a>` elements with `href` attributes. |
| `document.scripts`      | Returns a collection of all `<script>` elements in the document. |
| `document.styleSheets`  | Returns a collection of all the stylesheets in the document. |


## `document` common used methods


| Method                                  | Description                                          |
|-----------------------------------------|------------------------------------------------------|
| `document.getElementById(id)`            | Returns the element with the specified `id` attribute. |
| `document.getElementsByClassName(class)`  | Returns a live HTMLCollection of elements with the specified class name. |
| `document.getElementsByTagName(tag)`      | Returns a live HTMLCollection of elements with the specified tag name. |
| `document.querySelector(selector)`        | Returns the first element that matches the specified CSS selector. |
| `document.querySelectorAll(selector)`     | Returns a static NodeList of all elements that match the specified CSS selector. |
| `document.createElement(tagName)`        | Creates a new HTML element with the specified tag name. |
| `document.createTextNode(text)`          | Creates a new text node with the specified text content. |
| `document.appendChild(node)`             | Appends a child node to the current element.       |
| `document.removeChild(node)`              | Removes a child node from the current element.     |
| `document.replaceChild(newNode, oldNode)` | Replaces an old child node with a new one.         |
| `document.getElementById(id).setAttribute(attribute, value)` | Sets the value of an attribute on the specified element. |
| `document.getElementById(id).getAttribute(attribute)`        | Retrieves the value of the specified attribute from the element. |
| `document.getElementById(id).removeAttribute(attribute)`     | Removes the specified attribute from the element. |
| `document.getElementById(id).addEventListener(event, handler)` | Attaches an event listener to the specified element. |
| `document.getElementById(id).removeEventListener(event, handler)` | Removes an event listener from the specified element. |

---------------------------------------------

## Elements & Nodes

In the context of the Document Object Model (DOM) in web development, "node" and "element" are related concepts, but they represent different things. Understanding the distinction between these terms is crucial for working with the DOM effectively. Here's the difference:

**1. Node:**

A "node" in the DOM is a generic term for any individual object within the DOM tree structure. Nodes can represent various things, including elements, text, attributes, and other parts of the document. There are several types of nodes, with the most common ones being:

- **Element Nodes:** These represent HTML elements in the document, like `<div>`, `<p>`, or `<a>`.

- **Text Nodes:** These represent the text content of an element, spaces and new lines.

- **Attribute Nodes:** These represent the attributes of an element, like `id`, `class`, or `src`.

- **Comment Nodes:** These represent comments within the HTML source code.

- **Document Nodes:** These represent the entire HTML document and are typically the root of the DOM tree.

Nodes are organized hierarchically in a tree structure, with the document node at the top, and they are used to access, modify, and navigate the content and structure of the web page.

**2. Element:**

An "element" is a specific type of node in the DOM that represents an HTML element, such as a `<div>`, `<p>`, or `<a>`. Elements are a subset of nodes, and they represent the actual HTML tags in the document. Elements have properties and methods that you can use to manipulate and interact with the HTML structure. For example, you can access an element's attributes, content, and child elements using the properties of an element node.

In summary, all elements are nodes, but not all nodes are elements. Elements are a specific category of nodes that represent the HTML tags in the DOM, whereas nodes encompass a broader range of objects in the DOM tree, including elements, text, attributes, and more. Understanding this distinction is essential for working with the DOM effectively and accurately targeting the elements you want to manipulate or interact with in your web development projects.

------------------------------------------------------------------------------
## How does the browser render the pages

Here's how the process works:

1. **HTML Parsing:** When you load a web page, the browser retrieves the HTML and starts parsing it. As it parses the HTML, it constructs the DOM tree, which represents the structure and hierarchy of the web page.

2. **CSS Styling:** After constructing the DOM, the browser applies the styles defined in the linked or inline CSS to the elements in the DOM. This is what gives the page its visual appearance.

3. **Layout and Rendering:** Once the DOM is constructed and styled, the browser performs layout calculations to determine the position and size of each element on the page. It then renders the web page, displaying it on the screen.

4. **User Interaction:** The user can interact with the rendered page by clicking links, filling out forms, or performing other actions. These interactions can trigger navigation, form submissions, or other operations.


-----------------------------------------------------------------------------

## Querying DOM Elements in JavaScript

Manipulating and interacting with elements on a web page is a fundamental part of web development. To achieve this, you need to understand how to query and access these elements in the Document Object Model (DOM). In this tutorial, we will explore the different methods for querying DOM elements in JavaScript and discuss the various return types associated with each method.

### Common DOM Element Querying Methods

#### `getElementById()`

This method retrieves an element by its unique `id` attribute. It returns a single element, or `null` if no matching element is found.

**Example:**
```javascript
const element = document.getElementById("myElement");
```

#### `getElementsByClassName()`

This method returns a collection of elements that have a specified class name. It returns an HTMLCollection or NodeList.

**Example:**
```javascript
const elements = document.getElementsByClassName("myClass");
```

### `getElementsByTagName()`

This method returns a collection of elements with a specified HTML tag name. It also returns an HTMLCollection or NodeList.

**Example:**
```javascript
const paragraphs = document.getElementsByTagName("p");
```

### `querySelector()`

`querySelector()` allows you to select the first element that matches a CSS selector. It returns a single element or `null` if no match is found.

**Example:**
```javascript
const element = document.querySelector("#myElement .myClass");
```

### `querySelectorAll()`

This method returns all elements that match a CSS selector. It returns a NodeList.

**Example:**
```javascript
const elements = document.querySelectorAll(".myClass");
```

## Return Types

The return types of the querying methods are as follows:

- `getElementById()`: Returns a single HTML element or `null`.
- `getElementsByClassName()`: Returns an HTMLCollection or NodeList (array-like collection).
- `getElementsByTagName()`: Returns an HTMLCollection or NodeList.
- `querySelector()`: Returns a single HTML element or `null`.
- `querySelectorAll()`: Returns a NodeList.

## Elements Query Best Practices

- Use `getElementById()` when you need a single, unique element with an `id` attribute.
- When querying by class name or tag name, prefer `querySelector()` or `querySelectorAll()` for more flexible selection based on CSS selectors.
- Be aware that `getElementsByClassName()` and `getElementsByTagName()` return live collections (which means that it reflects the current state of the DOM. any changes in the DOM will reflect to the collection), while `querySelectorAll()` returns a static NodeList ( adding or removing elements to the DOM, the NodeList you obtained remains unchanged) 

-----------------------------------------------------------------------------

## Difference Between Attributes and Properties

In the context of DOM (Document Object Model) and web development, there is a distinction between "attributes" and "properties."

**`Attributes`**

- **Attributes** are the initial values that are specified in the HTML source code and are part of the element's markup.
- They are defined in the element's opening tag and provide configuration settings or metadata for that element.
- Examples of attributes include `id`, `class`, `src`, `href`, and other HTML attributes.
- Attributes are typically represented as strings.

```html
<a id="myLink" href="https://www.example.com">Example Link</a>
```

**`Properties`**

- **Properties** are values that are accessible and modifiable through the DOM using JavaScript.
- They represent the current state of the element and can be updated during runtime.
- Properties correspond to attributes but are often derived from attributes and can have different data types.
- For example, the `href` attribute becomes the `href` property in JavaScript, but it can be accessed as a string.

### Synchronization Between Attributes and Properties

In many cases, there is a one-way synchronization from attributes to properties when the page is loaded:

1. When the page loads, the values of attributes are used to initialize the corresponding properties. For example, the `src` attribute of an `<img>` element is used to set the `src` property in JavaScript.

```html
<img src="image.jpg" id="myImage">
```

```javascript
const image = document.getElementById("myImage");
console.log(image.src); // This will log the absolute URL of the image.
```

2. After the initial synchronization, properties can change independently of attributes. For example, you can change the `src` property in JavaScript, and it won't affect the `src` attribute in the HTML source code.

```javascript
image.src = "new-image.jpg"; // Changes the image source using the property.
```

3. Modifying attributes directly in JavaScript using `.setAttribute()` may not immediately affect the properties, and vice versa. In some cases, changes to one are reflected in the other, but it's not guaranteed.

------------------------------------------------------

## DOM Manipulation versus DOM Traversal

**DOM Manipulation** and **DOM Traversal** are two fundamental tasks in web development that involve interacting with the Document Object Model (DOM) to access and modify elements on a web page. While they are related, they serve different purposes:

**DOM Manipulation:**

- **Definition:** DOM manipulation involves directly changing the properties, attributes, or content of DOM elements to modify the appearance or behavior of a web page.
- **Use Cases:** You use DOM manipulation to update the content, style, or attributes of existing elements. For example, you might change the text of a paragraph, add or remove HTML elements, modify styles, or toggle the visibility of an element.
- **Methods:** Common DOM manipulation methods include `innerHTML`, `textContent`, `setAttribute`, `appendChild`, `removeChild`, and methods for modifying CSS properties.

**DOM Traversal:**

- **Definition:** DOM traversal refers to navigating through the DOM tree to find and access elements relative to other elements. It's about moving between parent, child, and sibling nodes to locate specific elements.
- **Use Cases:** DOM traversal is commonly used to find elements, often based on their relationships to other elements, their classes, or their position in the DOM tree. It's especially useful for selecting elements dynamically based on user actions.
- **Methods:** Common DOM traversal methods include `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, `querySelectorAll`, and various methods for traversing parent, child, and sibling nodes.

---------------------------------------------------------------

## Child, Parent, Descendant, Ancestor and Sibling Elements

1. **Child Element:**
   - A "child element" is an element that is nested within another element. It is a direct descendant of the parent element.
   - For example, in the HTML below the `<p>` element is a child element of the `<div>` element.
      
      ```html
      <div>
        <p>Some text</p>
      </div>
      ```

2. **Parent Element:**
   - A "parent element" is an element that contains one or more child elements. It is at a higher level in the DOM hierarchy.
   - In the example below, the `<div>` element is the parent of the `<p>` element.

      ```html
      <div>
        <p>Some text</p>
      </div>
      ```

3. **Descendant Elements:**
   - "Descendant elements" are elements that are nested at any level within another element. They can be direct children or nested deeper within child elements.
   - In the HTML below, both the `<p>` and `<strong>` elements are descendants of the `<div>` element.

      ```html
      <div>
        <p>
          <strong>Important</strong>
        </p>
      </div>
      ```

4. **Ancestor Elements:**
   - "Ancestor elements" are elements that are higher in the hierarchy and contain a given element. They can be parents, grandparent elements, or even higher ancestors.
   - In the HTML below, the `<div>` element is an ancestor of the `<p>` and `<strong>` elements.

      ```html
      <div>
        <p>
          <strong>Important</strong>
        </p>
      </div>
      ```

5. **Sibling Elements:**
   - "Sibling elements" are elements that share the same parent and are at the same level in the hierarchy.
   - In the HTML below, the `<li>` elements are siblings of each other.

      ```html
      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
      </ul>
      ```

----------------------------------------------------

## DOM Traversal in JavaScript
 
DOM traversal involves moving up, down, and across this tree to locate elements for various purposes, such as reading, updating, or deleting content.
getting elements by tag names, class names or IDs are types of DOM traversal.
- `document.getElementsByTagName("p");`
- `document.getElementById("myElement");`
- `document.getElementsByClassName("myClass");`

### Navigating Parent and Child Elements

You can traverse up and down the DOM tree to access parent and child elements:

- Access the parent node with `.parentNode` or `.parentElement`.
- Access child nodes with `.childNodes`, which returns a collection that may include text nodes.
- Access child elements using `.children`, which returns only element nodes.
- Access the first child even if it is a space or new line (text node) `.firstChild`.
- Access the first child HTML Element `.firstElementChild`.
- Access the last child even if it is a text node `.lastChild`.
- Access the last child HTML Element `.lastElementChild`.

```javascript
const parent = element.parentNode; // Access the parent node
const children = element.children; // Access child elements
const firstChild = parent.firstElementChild; // Access first child
const firstChild = parent.lastElementChild; // Access last child
```

### Traversing Siblings

Traversing siblings involves accessing elements that share the same parent node. Common sibling traversal methods include:

- `.nextSibling` and `.previousSibling`: Access adjacent nodes.
- `.nextElementSibling` and `.previousElementSibling`: Access adjacent elements.

```javascript
const nextElement = element.nextElementSibling;
const previousElement = element.previousElementSibling;
```

## Using Selectors: `querySelector` and `querySelectorAll`

Modern DOM traversal often involves using CSS selectors with `querySelector()` and `querySelectorAll()`. These methods return elements based on a CSS selector.

```javascript
// Select the first element with the class "myClass"
const element = document.querySelector(".myClass");

// Select all <a> elements with the class "link"
const links = document.querySelectorAll("a.link");
```

------------------------------------------------------------------------------------

## Styling the DOM Using JavaScript

Styling the Document Object Model (DOM) with JavaScript allows you to dynamically change the appearance of HTML elements on your web page. This can be useful for creating interactive web applications, responding to user actions, or modifying the layout and visual presentation of content.

### Modifying Styles with the `style` Property

The `style` property of a DOM element provides direct access to its inline CSS styles. You can use this property to modify specific style attributes like `color`, `font-size`, or `background-color`.

```javascript
const element = document.getElementById("myElement");

// Change text color and font size
element.style.color = "blue";
element.style.fontSize = "16px";
```

### Adding and Removing Classes with `className`

You can apply predefined CSS classes to elements by manipulating the `className` property. This method is especially useful when you want to apply consistent styles to multiple elements.

```javascript
const element = document.getElementById("myElement");

// Add a CSS class
element.className = "styled-element";
```

### Toggling Classes with `classList.toggle`

The `classList.toggle` method allows you to add or remove a class based on its presence. This is handy for creating toggle switches or interactive elements that change style on user interaction.

```javascript
const element = document.getElementById("myElement");

// Toggle a CSS class
element.classList.toggle("active");
```

### Checking for Classes with `classList.contains`

To check if an element has a specific class, you can use the `classList.contains` method. This is useful for conditional styling based on the existence of a class.

```javascript
const element = document.getElementById("myElement");

// Check if an element has a class
if (element.classList.contains("highlighted")) {
  // Perform an action
}
```

### Adding and Removing Classes with `classList.add` and `classList.remove`

You can explicitly add or remove classes using the `classList.add` and `classList.remove` methods. These are helpful for applying or removing styles based on user actions or events.

```javascript
const element = document.getElementById("myElement");

// Add a CSS class
element.classList.add("highlighted");

// Remove a CSS class
element.classList.remove("active");
```
--------------------------------------------------------------------------------------------------------------------------------

## Adding and Removing HTML Elements by Javascript

Dynamic manipulation of HTML elements is a fundamental part of building interactive web applications. JavaScript provides a variety of methods to add, remove, and modify elements within the Document Object Model (DOM).

##£ Modifying Inner HTML with `innerHTML`

The `innerHTML` property allows you to set the HTML content of an element, effectively replacing its content.

```javascript
const element = document.getElementById("myElement");

// Replace the content with new HTML
element.innerHTML = "<p>New content</p>";
```

### Inserting HTML with `insertAdjacentHTML`

The `insertAdjacentHTML` method allows you to insert HTML at a specified position relative to the element.

```javascript
   insertAdjacentHTML(position, text)
```
the position valid values are `beforebegin`, `afterbegin`, `beforeend` & `afterend`.

```javascript
const element = document.getElementById("myElement");

// Insert HTML after the element
element.insertAdjacentHTML("afterend", "<p>Inserted content</p>");
```


### Creating Elements with `createElement`

The `createElement` method lets you create new elements in memory, which can be subsequently added to the DOM.

```javascript
// Create a new element
const newElement = document.createElement("div");
newElement.textContent = "Newly created element";

// Append the new element to the document
document.body.appendChild(newElement);
```

### Appending Elements with `appendChild` and `append`

`appendChild` and `append` methods are used to add elements as child nodes within other elements in the DOM.

```javascript
const parentElement = document.getElementById("parent");

// Append a child element using appendChild
const childElement = document.createElement("p");
childElement.textContent = "Child element";
parentElement.appendChild(childElement);

// Append a child element using append
parentElement.append(childElement);
```
**Key Differences between  `appendChild` and `append`:**

- **Number of Arguments:** appendChild accepts a single argument (the child element), while append can accept multiple arguments.

- **Appending Existing Elements:** appendChild moves an existing element if it is already in the DOM, while append appends new copies of elements, leaving the original elements in their current positions.

- **Versatility:** append is more versatile, allowing you to append a mix of elements, text, and other data in a single call.

In summary, append is a more flexible method for adding elements to the DOM, especially when you need to add multiple child elements at once or combine elements with text. appendChild is suitable when you want to move an existing element to a new parent. The choice between them depends on your specific requirements in a given situation.

### Updating Text Content with `textContent`

The `textContent` property allows you to set or replace the text content of an element.

```javascript
const element = document.getElementById("myElement");

// Replace the text content
element.textContent = "New text content";
```

### Prepending Elements with `prepend`

The `prepend` method inserts one or more elements as the first child of the target element.

```javascript
const parentElement = document.getElementById("parent");
const newElement = document.createElement("p");
newElement.textContent = "New child element";

// Prepend the new element as the first child
parentElement.prepend(newElement);
```

### Inserting Elements with `insertBefore`, `before`, and `after`

- `insertBefore` is used to insert an element before a specified reference element.
- `before` inserts an element before another element without the need for a reference element.
- `after` inserts an element after another element without the need for a reference element.

```javascript
const parentElement = document.getElementById("parent");
const referenceElement = document.getElementById("reference");
const newElement = document.createElement("p");
newElement.textContent = "New child element";

// Insert before a reference element
parentElement.insertBefore(newElement, referenceElement);

// Insert before a specific element
referenceElement.before(newElement);

// Insert after a specific element
referenceElement.after(newElement);
```

### Replacing Elements with `replaceWith`

The `replaceWith` method replaces one element with another.

```javascript
const oldElement = document.getElementById("oldElement");
const newElement = document.createElement("p");
newElement.textContent = "Replacement element";

// Replace the old element with the new element
oldElement.replaceWith(newElement);
```

### Browser Compatibility

Browser compatibility varies for some of the mentioned methods. Be sure to check compatibility before using them in production. For example, `insertAdjacentHTML` may not be supported in older browsers.

