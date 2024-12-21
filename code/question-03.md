Here’s a list of 100 common JavaScript interview questions that may be asked by various companies. These questions cover a broad range of topics including basics, advanced concepts, and practical applications:

## Basic JavaScript Concepts




---

### 90. **What is the `debugger` keyword in JavaScript?**

The `debugger` keyword is used to pause the execution of JavaScript code at a specific point, allowing you to inspect variables and the call stack. It acts like a breakpoint in the code. When the `debugger` statement is encountered, the browser’s developer tools open, and execution is paused.

**Example**:

```javascript
function testDebugger() {
  let x = 10;
  debugger; // Code will pause here
  console.log(x);
}

testDebugger();
```

When the code hits the `debugger` statement, the execution stops, and you can inspect `x` and other parts of the code in the developer tools.

---

### 91. **How does JavaScript handle errors in a try/catch block?**

In JavaScript, errors can be caught and handled using the `try...catch` block. The `try` block contains the code that may throw an error, while the `catch` block handles the error.

**Example**:

```javascript
try {
  let result = riskyFunction();
  console.log(result);
} catch (error) {
  console.error('An error occurred:', error.message);
}
```

- If an error occurs inside the `try` block, JavaScript jumps to the `catch` block.
- The `catch` block receives the error object, which contains details about the error (e.g., message, stack trace).

You can also use `finally`, which will always run regardless of whether an error occurred:

```javascript
try {
  let result = riskyFunction();
} catch (error) {
  console.error('Error:', error);
} finally {
  console.log('This will run no matter what');
}
```

---

### 92. **What are JavaScript frameworks, and how do they differ from libraries?**

- **JavaScript frameworks**: A framework is a collection of prewritten code that provides a structure for building applications. It usually dictates the structure of your code and is opinionated about how things should be done. Frameworks provide a lot of functionality out of the box and are generally used to build large-scale applications (e.g., **Angular**, **Vue.js**, **React**).

  **Example**: Angular is a framework because it provides structure, conventions, and tools for building applications.

- **JavaScript libraries**: A library is a collection of functions and utilities that you can use to perform specific tasks (e.g., manipulating the DOM, making AJAX requests). Libraries are not opinionated, meaning they allow you to structure your application as you choose (e.g., **Lodash**, **jQuery**).

  **Example**: Lodash is a library because it provides utility functions, but it doesn't dictate how your app should be structured.

---

### 93. **What is the `bind()` method used for in JavaScript?**

The **`bind()`** method creates a new function that, when called, has its `this` value set to the specified context (object), and any provided arguments are pre-set (partial application).

**Example**:

```javascript
const person = {
  name: 'Alice',
  greet() {
    console.log('Hello, ' + this.name);
  }
};

const greetAlice = person.greet.bind(person);
greetAlice(); // Hello, Alice
```

Here, `greetAlice` is bound to the `person` object, so `this` inside the `greet()` method refers to `person`.

---

### 94. **What are service workers in JavaScript, and how do they work?**

**Service workers** are a type of web worker that runs in the background, separate from the web page, enabling features like caching, push notifications, and background synchronization. They allow for offline-first web experiences and can intercept network requests, enabling you to cache resources or serve content while offline.

**How they work**:
1. **Registration**: The service worker is registered in the browser via `navigator.serviceWorker.register()`.
2. **Installation**: After registration, the service worker goes through the installation phase, where it caches resources.
3. **Activation**: Once installed, it activates and begins intercepting network requests, allowing caching or returning responses from the cache.
4. **Fetching**: The service worker intercepts network requests and serves cached data, allowing for offline functionality.

**Example**:

```javascript
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('/service-worker.js').then(function(registration) {
    console.log('Service Worker registered with scope:', registration.scope);
  }).catch(function(error) {
    console.log('Service Worker registration failed:', error);
  });
}
```

Service workers enable powerful features like offline support, caching strategies, and background tasks for modern web applications.

---

### 95. **What are `Object.assign()` and its uses?**

**`Object.assign()`** is a method used to copy values from one or more source objects to a target object. It is typically used to clone objects or merge multiple objects.

**Syntax**:
```javascript
Object.assign(target, ...sources);
```

- **Target**: The object that will receive the properties.
- **Sources**: The objects whose properties will be copied to the target.

**Example**:

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };

const mergedObj = Object.assign({}, obj1, obj2);
console.log(mergedObj); // { a: 1, b: 2, c: 3, d: 4 }
```

- It **shallow copies** properties, meaning that if the properties are objects, the references are copied, not the values.
- It’s useful for merging objects, copying properties, or creating a shallow clone of an object.


### 96. **What is a `Map` and `Set` in JavaScript?**

- **Map**:
  A `Map` is a collection of key-value pairs where both keys and values can be any type of data (objects, functions, etc.). The keys in a `Map` are ordered, and you can iterate over them in insertion order. It maintains the order of the inserted keys.

  **Example**:

  ```javascript
  const map = new Map();
  map.set('name', 'John');
  map.set(1, 'one');
  map.set(true, 'yes');
  
  console.log(map.get('name'));  // 'John'
  console.log(map.size);         // 3
  ```

- **Set**:
  A `Set` is a collection of unique values. It stores values without duplicates, and the values in a `Set` are ordered. It can store any type of data and doesn’t allow duplicate entries.

  **Example**:

  ```javascript
  const set = new Set();
  set.add(1);
  set.add(2);
  set.add(2);  // Duplicate value, won't be added
  
  console.log(set);  // Set { 1, 2 }
  console.log(set.has(1));  // true
  console.log(set.size);    // 2
  ```

---

### 97. **What is the difference between shallow copy and deep copy in JavaScript?**

- **Shallow Copy**:
  A shallow copy means creating a new object, but nested objects or arrays within it are still referenced (not copied). It only copies the top-level properties.

  **Example**:

  ```javascript
  const obj1 = { a: 1, b: { c: 2 } };
  const shallowCopy = { ...obj1 };
  
  shallowCopy.b.c = 3;  // Modifying nested object
  console.log(obj1.b.c);  // 3, both obj1 and shallowCopy share the same reference to b
  ```

- **Deep Copy**:
  A deep copy means creating a completely independent copy of the original object, including all nested objects. It ensures that no references are shared between the copied object and the original.

  **Example**:

  ```javascript
  const obj1 = { a: 1, b: { c: 2 } };
  const deepCopy = JSON.parse(JSON.stringify(obj1));  // Simple deep copy method
  
  deepCopy.b.c = 3;
  console.log(obj1.b.c);  // 2, obj1 and deepCopy are independent
  ```

---

### 98. **What is functional programming in JavaScript? How is it different from object-oriented programming?**

- **Functional Programming**:
  Functional programming (FP) is a programming paradigm where you treat computation as the evaluation of mathematical functions and avoid changing state and mutable data. It focuses on immutability, higher-order functions, pure functions, and declarative code.

  **Features of FP**:
  - **Pure functions**: Functions that always return the same output for the same input and have no side effects.
  - **Immutability**: Data is not modified, but instead, new data is returned.
  - **First-class functions**: Functions can be passed as arguments and returned as values.
  - **Higher-order functions**: Functions that take other functions as arguments or return functions.

  **Example**:

  ```javascript
  const add = (a, b) => a + b;
  const multiply = (a, b) => a * b;

  const result = multiply(add(2, 3), 4);  // Using FP
  ```

- **Object-Oriented Programming (OOP)**:
  OOP is based on objects and classes. It focuses on data and methods that operate on that data, organizing code around objects that represent real-world entities.

  **Features of OOP**:
  - **Classes and objects**: Encapsulating data and behavior into objects.
  - **Inheritance**: Allowing classes to inherit properties and methods from other classes.
  - **Encapsulation**: Hiding the internal state and requiring all interaction to be done through methods.
  - **Polymorphism**: Allowing objects of different classes to be treated as objects of a common superclass.

  **Example**:

  ```javascript
  class Animal {
    constructor(name) {
      this.name = name;
    }
    speak() {
      console.log(this.name + ' makes a sound');
    }
  }

  const dog = new Animal('Rex');
  dog.speak();
  ```

**Key Differences**:
- **OOP** is about organizing code into objects and their interactions, while **FP** is about using pure functions and avoiding shared state.
- OOP typically uses mutable state, while FP emphasizes immutability.

---

### 99. **What is an abstract class in JavaScript?**

JavaScript does not have built-in support for **abstract classes** in the same way that languages like Java or C# do. However, you can simulate abstract classes by creating a class with methods that are not implemented, and then using subclasses to implement those methods.

**Example**:

```javascript
class Animal {
  constructor(name) {
    if (this.constructor === Animal) {
      throw new Error("Abstract class cannot be instantiated.");
    }
    this.name = name;
  }

  speak() {
    throw new Error("Method 'speak()' must be implemented.");
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks`);
  }
}

const dog = new Dog('Rex');
dog.speak();  // Rex barks

// const animal = new Animal('Generic');  // Error: Abstract class cannot be instantiated.
```

Here, `Animal` is treated as an abstract class by throwing an error if you try to instantiate it directly. Subclasses like `Dog` implement the abstract `speak()` method.

---

### 100. **How do you use JavaScript for manipulating the DOM?**

JavaScript allows you to interact with and manipulate the DOM (Document Object Model) to dynamically change the content and structure of a webpage. You can use various DOM methods to access elements and modify their properties, styles, or events.

- **Selecting elements**:
  You can select elements using methods like `getElementById()`, `querySelector()`, and `querySelectorAll()`.

  **Example**:

  ```javascript
  const element = document.getElementById('myElement');
  const allItems = document.querySelectorAll('.items');
  ```

- **Changing content**:
  You can modify the text or HTML content of an element using `textContent` or `innerHTML`.

  **Example**:

  ```javascript
  element.textContent = 'New Content';
  ```

- **Modifying attributes**:
  Use methods like `setAttribute()` to change element attributes.

  **Example**:

  ```javascript
  element.setAttribute('src', 'newImage.jpg');
  ```

- **Adding/removing classes**:
  Use `classList` to add, remove, or toggle CSS classes.

  **Example**:

  ```javascript
  element.classList.add('active');
  element.classList.remove('inactive');
  element.classList.toggle('highlight');
  ```

- **Creating and appending elements**:
  You can create new elements and append them to the DOM.

  **Example**:

  ```javascript
  const newElement = document.createElement('div');
  newElement.textContent = 'Hello, World!';
  document.body.appendChild(newElement);
  ```

- **Handling events**:
  You can attach event listeners to elements using `addEventListener()`.

  **Example**:

  ```javascript
  element.addEventListener('click', () => {
    alert('Element clicked!');
  });
  ```
