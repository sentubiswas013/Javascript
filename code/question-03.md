Here’s a list of 100 common JavaScript interview questions that may be asked by various companies. These questions cover a broad range of topics including basics, advanced concepts, and practical applications:

## Basic JavaScript Concepts




---

### 57. **What is `setTimeout()` and `setInterval()`?**

- **`setTimeout()`**: Executes a function after a specified delay (in milliseconds).
  
  Example:
  ```javascript
  setTimeout(() => {
    console.log("Executed after 2 seconds");
  }, 2000);
  ```

- **`setInterval()`**: Executes a function repeatedly at a specified interval (in milliseconds) until stopped by `clearInterval()`.

  Example:
  ```javascript
  const intervalId = setInterval(() => {
    console.log("Executed every 2 seconds");
  }, 2000);

  // Stop the interval after 6 seconds
  setTimeout(() => clearInterval(intervalId), 6000);
  ```

---

### 58. **What are callbacks and promises used for in JavaScript?**

- **Callbacks**: Functions passed as arguments to other functions, used to handle asynchronous operations (e.g., after a data fetch or when an event occurs).
  - Callbacks are typically used for tasks like handling results after API calls, file reading, etc.
  
  Example:
  ```javascript
  function fetchData(callback) {
    setTimeout(() => {
      callback("Data fetched");
    }, 1000);
  }

  fetchData(result => {
    console.log(result); // "Data fetched"
  });
  ```

- **Promises**: Represent the result of an asynchronous operation, which may be completed in the future or fail.
  - Promises can be chained with `.then()` for success and `.catch()` for error handling.
  
  Example:
  ```javascript
  const myPromise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("Data fetched"), 1000);
  });

  myPromise.then(result => console.log(result)); // "Data fetched"
  ```

Both callbacks and promises allow for handling asynchronous tasks without blocking the execution of other code. Promises are a more modern approach and help avoid "callback hell" (deeply nested callbacks).

### 59. **What is a JavaScript memory leak and how can you avoid it?**

A **memory leak** occurs when the JavaScript engine does not release memory that is no longer in use. This can cause the browser to slow down or even crash as unused objects and resources remain in memory.

Common causes of memory leaks:
- **Global variables**: Variables that are accidentally declared in the global scope.
- **Unclosed event listeners**: Not removing event listeners can prevent objects from being garbage-collected.
- **Detached DOM elements**: When elements are removed from the DOM but still referenced in JavaScript, they won't be garbage collected.
  
To avoid memory leaks:
- Use `let` and `const` to avoid unintentional global variables.
- Remove event listeners using `removeEventListener()` when they're no longer needed.
- Set DOM references to `null` when you no longer need them to allow garbage collection.
- Use `WeakMap` or `WeakSet` to hold references that don't prevent garbage collection.

---

### 60. **How do you use regular expressions in JavaScript?**

Regular expressions (regex) are used for pattern matching and text manipulation in JavaScript. They can be created using the `RegExp` constructor or using a literal syntax.

- **Creating a regex**:
  ```javascript
  const regex = /hello/; // regex literal
  const regex2 = new RegExp("hello"); // using RegExp constructor
  ```

- **Using regex with methods**:
  - `test()`: Tests if a pattern exists in a string.
  ```javascript
  const regex = /hello/;
  console.log(regex.test("hello world")); // true
  ```

  - `exec()`: Executes a search for a match in a string and returns detailed information.
  ```javascript
  const regex = /hello/;
  console.log(regex.exec("hello world")); // ["hello"]
  ```

  - `match()`: Matches a string against a regex pattern and returns the result.
  ```javascript
  const str = "hello world";
  console.log(str.match(/world/)); // ["world"]
  ```

  - `replace()`: Replaces part of a string that matches a pattern.
  ```javascript
  const str = "hello world";
  console.log(str.replace(/world/, "JavaScript")); // "hello JavaScript"
  ```

---

### 61. **What are Web Workers in JavaScript?**

Web Workers are JavaScript scripts that run in the background, separate from the main thread, enabling you to perform tasks like calculations, data processing, or making network requests without blocking the UI or affecting performance.

- **Creating a Worker**:
  ```javascript
  const worker = new Worker('worker.js'); // worker.js is the script file

  worker.onmessage = function(event) {
    console.log('Message from worker:', event.data);
  };

  worker.postMessage('Hello, worker!');
  ```

In `worker.js`:
```javascript
self.onmessage = function(event) {
  console.log('Message from main thread:', event.data);
  self.postMessage('Hello from worker!');
};
```

Web Workers are useful for offloading CPU-intensive tasks and keeping the user interface responsive.

---

### 62. **How do you compare two objects in JavaScript?**

In JavaScript, objects are compared by reference, not by value. To compare objects by their values, you need to compare their properties individually.

- **Shallow comparison**: Compare the properties of two objects.
  ```javascript
  function shallowEqual(obj1, obj2) {
    return JSON.stringify(obj1) === JSON.stringify(obj2);
  }

  const obj1 = { name: "Alice", age: 25 };
  const obj2 = { name: "Alice", age: 25 };

  console.log(shallowEqual(obj1, obj2)); // true
  ```

- **Deep comparison**: You can implement or use libraries for deep comparison, which compares nested objects or arrays.
  ```javascript
  function deepEqual(a, b) {
    if (typeof a !== 'object' || typeof b !== 'object' || a === null || b === null) {
      return a === b;
    }

    const keysA = Object.keys(a);
    const keysB = Object.keys(b);

    if (keysA.length !== keysB.length) return false;

    for (let key of keysA) {
      if (!keysB.includes(key) || !deepEqual(a[key], b[key])) {
        return false;
      }
    }

    return true;
  }
  ```

---

### 63. **What is the DOM in JavaScript and how do you interact with it?**

The **DOM (Document Object Model)** is a programming interface for web documents, allowing JavaScript to interact with the HTML and XML structures of a page. The DOM represents the page as a tree of nodes, where each node is an object representing part of the page (such as an element, attribute, or text).

- **Accessing DOM elements**:
  ```javascript
  const element = document.getElementById('myElement');
  const elements = document.querySelectorAll('.myClass');
  ```

- **Modifying the DOM**:
  ```javascript
  const div = document.createElement('div');
  div.textContent = 'Hello World';
  document.body.appendChild(div); // Adds div to the body
  ```

- **Event handling**:
  ```javascript
  const button = document.getElementById('myButton');
  button.addEventListener('click', function() {
    alert('Button clicked!');
  });
  ```

The DOM allows dynamic interaction with the webpage, such as modifying content, handling user input, or controlling animation.

---

### 64. **What are the differences between a function expression and a function declaration?**

- **Function Declaration**:
  ```javascript
  function greet() {
    console.log("Hello");
  }
  ```

  - Can be called before it's defined (due to hoisting).
  - Has function scope.

- **Function Expression**:
  ```javascript
  const greet = function() {
    console.log("Hello");
  };
  ```

  - Cannot be called before it's defined.
  - Is treated as an expression and can be anonymous.

In summary, **function declarations** are hoisted and can be called before their declaration, while **function expressions** are not hoisted and must be defined before usage.

---

### 65. **What is the difference between `slice()` and `splice()` methods in JavaScript?**

- **`slice()`**: Creates a shallow copy of a portion of an array and returns a new array without modifying the original array.
  ```javascript
  const arr = [1, 2, 3, 4, 5];
  const newArr = arr.slice(1, 4); // [2, 3, 4]
  ```

- **`splice()`**: Changes the original array by adding/removing elements at a specified index.
  ```javascript
  const arr = [1, 2, 3, 4, 5];
  arr.splice(2, 2, 'a', 'b'); // Removes 3 and 4, and adds 'a', 'b'
  console.log(arr); // [1, 2, 'a', 'b', 5]
  ```

---

### 66. **What is the use of the `map()` method in JavaScript?**

The `map()` method creates a new array by applying a provided function to every element in the original array. It does not modify the original array.

Example:
```javascript
const arr = [1, 2, 3];
const newArr = arr.map(x => x * 2);
console.log(newArr); // [2, 4, 6]
```

---

### 67. **What are `map()`, `reduce()`, and `filter()` functions in JavaScript?**

- **`map()`**: Creates a new array with the results of calling a provided function on every element.
  ```javascript
  const arr = [1, 2, 3];
  const newArr = arr.map(x => x * 2); // [2, 4, 6]
  ```

- **`reduce()`**: Reduces an array to a single value by applying a function to each element (accumulator pattern).
  ```javascript
  const arr = [1, 2, 3];
  const sum = arr.reduce((acc, curr) => acc + curr, 0); // 6
  ```

- **`filter()`**: Creates a new array with elements that pass the provided test.
  ```javascript
  const arr = [1, 2, 3, 4, 5];
  const evenArr = arr.filter(x => x % 2 === 0); // [2, 4]
  ```

---

### 68. **What is the `Promise.all()` method used for?**

`Promise.all()` is used to execute multiple asynchronous operations concurrently and returns a promise that resolves when all the promises in the array have resolved or rejects if any promise is rejected.

Example:
```javascript
const promise1 = Promise.resolve(1);
const promise2 = Promise.resolve(2);

Promise.all([promise1, promise2]).then(values => {
  console.log(values); // [1, 2]
});
```

---

### 69. **What is the `finally()` method in JavaScript promises?**

The `finally()` method allows you to specify a block of code that will be executed after a promise settles (either resolved or rejected), regardless of the outcome.

Example:
```javascript
const promise = new

 Promise((resolve, reject) => {
  resolve('Success');
});

promise
  .then(result => {
    console.log(result); // Success
  })
  .finally(() => {
    console.log('Clean-up code runs');
  });
```

## Advanced JavaScript Concepts
### 70. **What is the concept of currying in JavaScript? Can you provide an example?**

**Currying** is a technique in functional programming where a function that takes multiple arguments is transformed into a sequence of functions, each taking one argument.

In simpler terms, currying allows you to break a function that takes multiple parameters into a series of functions that each take one parameter and return a new function until all parameters are provided.

**Example:**

```javascript
function multiply(a) {
  return function(b) {
    return a * b;
  };
}

const multiplyBy2 = multiply(2);
console.log(multiplyBy2(3)); // 6
```

Here, `multiply` is a curried function that first takes `a`, then returns a new function that takes `b` and performs the multiplication.

---

### 71. **What is the concept of memoization in JavaScript?**

**Memoization** is an optimization technique where the results of expensive function calls are cached, and when the same inputs occur again, the cached result is returned instead of recalculating it. This can greatly improve performance for functions that are called repeatedly with the same arguments.

**Example:**

```javascript
function memoize(fn) {
  const cache = {};
  return function(arg) {
    if (cache[arg]) {
      return cache[arg];
    }
    const result = fn(arg);
    cache[arg] = result;
    return result;
  };
}

const square = memoize(function(n) {
  console.log('Calculating...');
  return n * n;
});

console.log(square(4)); // Calculating... 16
console.log(square(4)); // 16 (cached)
```

Here, the `memoize` function caches results, so the second time `square(4)` is called, it returns the cached result without recalculating.

---

### 72. **What are decorators in JavaScript?**

**Decorators** are a special kind of declaration that can be used to modify the behavior of a class, method, accessor, property, or parameter in JavaScript. They are usually used in frameworks like TypeScript, Angular, or Babel, as part of the class syntax.

Decorators are functions that are applied to a class or method and can be used to add additional behavior or modify how things work.

**Example (in TypeScript):**

```typescript
function log(target: any, key: string) {
  console.log(`Method ${key} is called`);
}

class MyClass {
  @log
  sayHello() {
    console.log("Hello!");
  }
}

const obj = new MyClass();
obj.sayHello();
```

In the above example, the `@log` decorator is applied to the `sayHello` method, which will log every time the method is invoked.




### 88. **How can you implement inheritance in JavaScript without using classes?**

In JavaScript, inheritance can be implemented using **prototypes**. You can create an object and link it to another object’s prototype to inherit its properties and methods.

**Example**:

```javascript
function Animal(name) {
  this.name = name;
}

Animal.prototype.speak = function() {
  console.log(this.name + ' makes a sound');
};

function Dog(name) {
  Animal.call(this, name); // Inherit properties
}

Dog.prototype = Object.create(Animal.prototype); // Inherit methods
Dog.prototype.constructor = Dog; // Set correct constructor

const dog = new Dog('Rex');
dog.speak(); // Rex makes a sound
```

Here, `Dog` inherits from `Animal` by using `Object.create()` to set `Dog`'s prototype to `Animal.prototype`.

---

### 89. **What is the difference between synchronous and asynchronous code in JavaScript?**

- **Synchronous code**: Executes line by line. Each operation waits for the previous one to finish before continuing, blocking further code execution.

  **Example**:
  
  ```javascript
  console.log('Start');
  console.log('End');
  ```

  Both `console.log()` statements are executed one after the other.

- **Asynchronous code**: Allows operations to run in the background without blocking the main execution thread. It continues executing other code while waiting for the asynchronous operation (like fetching data, setTimeout) to complete.

  **Example**:

  ```javascript
  console.log('Start');
  setTimeout(() => {
    console.log('Middle');
  }, 1000);
  console.log('End');
  ```

  Output: 
  ```
  Start
  End
  Middle
  ```

  Here, `setTimeout` runs asynchronously, and the `console.log('End')` statement executes before the `setTimeout` callback.

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
