**\# JavaScript Interview Questions & Answers**

Certainly! Below is a list of JavaScript-related questions that span beginner to advanced topics:

## Beginner-Level Questions
---

### 1\. **What is JavaScript?**

JavaScript is a dynamic, interpreted programming language primarily used for creating interactive effects within web browsers. It allows developers to build interactive features on websites such as form validation, animations, and dynamic content updates.

### 2\. **What is the difference between `let`, `const`, and `var`?**

* `let`: Declares a block-scoped variable that can be reassigned.
* `const`: Declares a block-scoped variable whose value cannot be reassigned after initialization.
* `var`: Declares a function-scoped variable, which can be re-declared and reassigned (not recommended due to its behavior with hoisting).

```javascript
let x = 5; // Can be reassigned
const y = 10; // Cannot be reassigned
var z = 15; // Function-scoped
```

- **`var`**:

  - **Scope**: Function-scoped (if declared inside a function) or globally-scoped.
  - **Hoisting**: Variables declared with `var` are hoisted to the top of their scope but initialized with `undefined`.
  - **Re-declaration**: You can re-declare the same variable in the same scope.
  - **Use**: Considered outdated for modern JavaScript due to issues with scoping and hoisting.

- **`let`**:

  - **Scope**: Block-scoped (only accessible within the block it’s declared in, such as within a loop or if-statement).
  - **Hoisting**: Hoisted but not initialized. Accessing it before the declaration results in a ReferenceError (due to the Temporal Dead Zone).
  - **Re-declaration**: Cannot be re-declared within the same scope.
  - **Use**: Preferred for variables whose value will change.

- **`const`**:
  - **Scope**: Block-scoped.
  - **Hoisting**: Like `let`, `const` is hoisted but not initialized, leading to a Temporal Dead Zone.
  - **Re-declaration**: Cannot be re-declared in the same scope.
  - **Mutability**: The variable must be assigned a value at the time of declaration and cannot be reassigned. However, if the value is an object or array, its properties or elements can still be modified.


### 3\. **What are the data types in JavaScript?**

JavaScript has seven basic data types:
- **`Primitive`**:
* `String` (e.g., `"hello"`)
* `Number` (e.g., `42`)
* `BigInt` (e.g., `9007199254740991n`)
* `Boolean` (e.g., `true` or `false`)
* `undefined` (e.g., a variable that is declared but not assigned a value)
* `null` (e.g., an explicitly assigned empty value)
* `Symbol` (e.g., `Symbol('desc')`)
* `Object` (e.g., arrays, functions, and plain objects)

- **`Non-Primitive`**:
* `Object` (e.g., `"let person = { name: "John", age: 25 }"`)
* `Array` (e.g., `"let fruits = ["apple", "banana", "cherry"]"`)
* `Function` (e.g., `"function greet() { console.log("Hello, world!"); }"`)
* `Date` (e.g., `"let today = new Date();"`)
* `RegExp ` (e.g., `"let regex = /abc/;"`)

- **`Key Differences between Primitive and Non-Primitive Data Types`**:
<table><thead><tr><th><strong>Feature</strong></th><th><strong>Primitive Data Types</strong></th><th><strong>Non-Primitive Data Types</strong></th></tr></thead><tbody><tr><td><strong>Memory</strong></td><td>Stored in stack memory</td><td>Stored in heap memory</td></tr><tr><td><strong>Size</strong></td><td>Fixed size</td><td>Varies (depends on the data structure or object)</td></tr><tr><td><strong>Value or Reference</strong></td><td>Holds the actual value</td><td>Holds a reference to the value (pointer to an object)</td></tr><tr><td><strong>Complexity</strong></td><td>Simple and atomic</td><td>More complex and can store multiple values</td></tr><tr><td><strong>Example</strong></td><td><code>int</code>, <code>char</code>, <code>boolean</code>, <code>float</code></td><td><code>String</code>, <code>Array</code>, <code>Object</code>, <code>Class</code>, <code>Interface</code></td></tr><tr><td><strong>Mutability</strong></td><td>Immutable (except in some languages like Java)</td><td>Mutable or immutable depending on the type</td></tr></tbody></table>

### 4\. **What is the difference between `==` and `===`?**

* `==`: Compares values for equality with type coercion. It tries to convert the operands to the same type before comparing them. This can lead to unexpected results
* `===`: Compares values for equality without type coercion (strict equality). It is the **strict equality** operator, meaning it checks both value and type, and does **not perform type coercion**

```javascript
5 == '5'  // true because type coercion occurs
5 === '5' // false because types are different (number vs. string)
```

### 5\. **How do you create a function in JavaScript?**

There are multiple ways to define functions in JavaScript:

1. **Function Declaration**:

   ```javascript
    function greet() {
     console.log('Hello!');
   }
   ```

2. **Function Expression**:

   ```javascript
    const greet = function() {
     console.log('Hello!');
   };
   ```

3. **Arrow Function**:

   ```javascript
    const greet = () => console.log('Hello!');
   ```

### 6\. **What are the different ways to declare variables in JavaScript?**

* **`var`**: Function-scoped, can be redeclared.
* **`let`**: Block-scoped, can be reassigned but not redeclared in the same scope.
* **`const`**: Block-scoped, cannot be reassigned or redeclared.

```javascript
 var a = 1;   // function-scoped
let b = 2;   // block-scoped
const c = 3; // block-scoped, cannot be reassigned
```

### 7\. **What is the purpose of the `typeof` operator?**

The `typeof` operator returns a string indicating the type of a variable or expression.

```javascript
typeof 'hello';   // 'string'
typeof 42;        // 'number'
typeof true;      // 'boolean'
typeof undefined; // 'undefined'
typeof null;      // 'object' (a known JavaScript quirk)
```

### 8\. **What is hoisting in JavaScript? How does it work with variables and functions?**

* **Hoisting** is JavaScript's behavior of moving variable and function declarations to the top of their containing scope during the compile phase, before code execution begins.

  * **For functions**: Function declarations (not expressions) are hoisted with both their definition and value, meaning you can call them before they appear in the code.

  * **For variables**: With `var`, only the declaration (not the initialization) is hoisted, so the variable is initialized as `undefined`. With `let` and `const`, only the declaration is hoisted, but not the initialization, leading to a "temporal dead zone" if you try to access them before the declaration.

```javascript
 codeconsole.log(x); // undefined
var x = 5; 

console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;
```

### 9\. **What are JavaScript arrays, and how do you create one?**

Arrays in JavaScript are ordered collections of items. You can create an array using square brackets `[]`.

```javascript
 const fruits = ['apple', 'banana', 'cherry'];
```

### 10\. **How do you add, remove, or access elements in an array?**

* **Add**: `push()` to add to the end, `unshift()` to add to the beginning.
* **Remove**: `pop()` to remove from the end, `shift()` to remove from the beginning.
* **Access**: Use the index (starting from 0).

```javascript
fruits.push('orange');      // Adds 'orange' to the end
fruits.unshift('grape');    // Adds 'grape' to the beginning
fruits.pop();               // Removes 'orange'
fruits.shift();             // Removes 'grape'
console.log(fruits[1]);     // Access the second element 'banana'
```

### 11\. **What is a loop? What are the different types of loops in JavaScript?**

A loop allows you to repeat a block of code multiple times.

Types of loops:

* **`for` loop**: Iterates a specific number of times.
* **`while` loop**: Loops as long as the condition is true.
* **`do...while` loop**: Loops at least once and then checks the condition.
* **`for...of` loop**: Iterates over iterable objects (e.g., arrays).
* **`for...in` loop**: Iterates over object properties.

```javascript
 for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}

let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}

let fruits = ['apple', 'banana', 'cherry'];
for (const fruit of fruits) {
  console.log(fruit); // apple, banana, cherry
}
```

### 12\. **What are JavaScript objects? How do you create one?**

Objects in JavaScript are collections of key-value pairs. You create an object using curly braces `{}`.

```javascript
 const person = {
  name: 'John',
  age: 30,
  greet() {
    console.log('Hello!');
  }
};
```

### 13\. **What is the difference between `null` and `undefined`?**

* `undefined` means a variable has been declared but not assigned a value.
* `null` is an intentional absence of any value (i.e., "empty").

```javascript
let x;
console.log(x);  // undefined

let y = null;
console.log(y);  // null
```

### 14\. **How do you handle events in JavaScript?**

You can handle events by attaching event listeners to DOM elements using methods like `addEventListener`.

```javascript
 const button = document.querySelector('button');
button.addEventListener('click', function() {
  alert('Button clicked!');
});
```

### 15\. **What is the `this` keyword in JavaScript?**

The `this` keyword refers to the context in which a function is called. Its value is determined by how the function is invoked.

```javascript
 const person = {
  name: 'Alice',
  greet: function() {
    console.log(`Hello, ${this.name}`);
  }
};
person.greet(); // Hello, Alice
```
In global scope, `this` refers to the global object (`window` in browsers).

- **Context-dependent**:
  - **Global context**: In the global execution context (outside any function), `this` refers to the global object (`window` in browsers, `global` in Node.js).
  - **Inside a method**: When used inside an object method, `this` refers to the object itself.
  - **Inside a constructor**: In a constructor function, `this` refers to the newly created object.
  - **Arrow functions**: Arrow functions do not have their own `this`; instead, they inherit `this` from their surrounding (lexical) context.
  - **Explicit binding**: Methods like `call()`, `apply()`, and `bind()` can explicitly set the value of `this`.


### 16\. **How does the `forEach()` method work?**

`forEach()` is an array method that executes a provided function once for each array element.

```javascript
 const numbers = [1, 2, 3];
numbers.forEach((num) => {
  console.log(num);
});
// Output: 1, 2, 3
```

### 17\. **What is the purpose of `break` and `continue` statements?**

* `break`: Exits a loop or switch statement immediately.
* `continue`: Skips the current iteration of a loop and continues with the next iteration.

```javascript
 for (let i = 0; i < 5; i++) {
  if (i === 2) {
    continue;  // Skips the iteration where i === 2
  }
  if (i === 4) {
    break;     // Exits the loop when i === 4
  }
  console.log(i);  // 0, 1, 3
}
```

### 18\. **What is a callback function in JavaScript?**

A callback function is a function passed as an argument to another function, and it is executed after the completion of the main function.

```javascript
 function greet(name, callback) {
  console.log(`Hello, ${name}`);
  callback();
}

function afterGreet() {
  console.log('Goodbye!');
}

greet('Alice', afterGreet); // Output: Hello, Alice
                            //         Goodbye!
```

---

## Intermediate-Level Questions

Sure! Here are the answers to the list of JavaScript questions:

### 1\. **What is closure in JavaScript?**

A **closure** is a function that "remembers" its lexical scope even when the function is executed outside that scope. This happens because JavaScript functions are first-class objects and they maintain references to the environment in which they were created.

Example:

```javascript
 function outer() {
  let counter = 0;
  return function inner() {
    counter++;
    console.log(counter);
  };
}

const increment = outer();  // closure is created here
increment(); // 1
increment(); // 2
```

### 2\. **What is the difference between function declarations and function expressions?**

* **Function Declaration**: A named function defined with the `function` keyword.

  ```javascript
   function greet() {
    console.log("Hello");
  }
  ```

  Function declarations are hoisted, meaning they are available throughout the code.

* **Function Expression**: A function assigned to a variable, which may or may not be named.

  ```javascript
   const greet = function() {
    console.log("Hello");
  };
  ```

  Function expressions are not hoisted. The function is only available after the assignment.

### 6\. **What Are `setTimeout` and `setInterval`? How Do They Differ?**

Both `setTimeout` and `setInterval` are used to schedule asynchronous functions to be executed after a delay.

* **`setTimeout`**: Executes a function once after a specified delay (in milliseconds).

  ```javascript
   codesetTimeout(() => {
    console.log("This runs after 2 seconds.");
  }, 2000);
  ```

* **`setInterval`**: Executes a function repeatedly, with a specified delay between each execution.

  ```javascript
   codesetInterval(() => {
    console.log("This runs every 2 seconds.");
  }, 2000);
  ```

#### Key Differences:

* `setTimeout` runs the function **once** after the specified delay.
* `setInterval` runs the function **repeatedly** at intervals.
* Both functions return an identifier that can be used to **clear** them (using `clearTimeout()` or `clearInterval()`).

Example of clearing a timer:

```javascript
 codelet timerId = setInterval(() => {
  console.log("This will repeat every second.");
}, 1000);

// Stop the interval after 5 seconds
setTimeout(() => {
  clearInterval(timerId);
  console.log("Interval cleared.");
}, 5000);
```

### Conclusion

These are core concepts in JavaScript for handling asynchronous behavior and managing operations like promises, async/await, event loops, and timers. By understanding these, you can write more efficient and readable asynchronous code.

### 4\. **Explain the concept of promises and how then() and catch() work.**

A **promise** represents the eventual completion (or failure) of an asynchronous operation. It can be in one of three states: **pending**, **fulfilled**, or **rejected**.


#### How Promises Work:

* A promise can be in one of three states:
  * **Pending**: The operation is still in progress.
  * **Resolved** (Fulfilled): The operation completed successfully.
  * **Rejected**: The operation failed (with an error).
* You create a promise using the `Promise` constructor, which takes a callback with two parameters: `resolve` and `reject`.

Example:

```javascript
 const promise = new Promise((resolve, reject) => {
  let success = true;
  if (success) {
    resolve("Operation successful");
  } else {
    reject("Operation failed");
  }
});

promise.then(result => {
  console.log(result);  // "Operation successful"
}).catch(error => {
  console.log(error);   // "Operation failed"
});
```

In this example:

* The `then()` method is used to handle the success of the promise.
* The `catch()` method is used to handle any errors (rejections).

#### How to Use Promises:

* Use `then()` to handle success.
* Use `catch()` to handle errors.
* You can chain multiple `then()` calls to handle sequential asynchronous operations.

### 5\. **What is async/await in JavaScript? and Difference Between Async/Await and Promises**

`async`/`await` is syntax sugar built on top of Promises to make asynchronous code easier to write and read. They are not different technologies, but rather a more readable way to work with Promises.

#### Promises:

* Promises require chaining `.then()` and `.catch()` methods to handle results and errors.

Using promises:

```javascript
function resolveAfter2Seconds() {
   return new Promise((resolve) => {
     setTimeout(() => {
       resolve('resolved');
     }, 2000);
   });
 }

 async function asyncCall() {
   console.log('calling');
   const result = await resolveAfter2Seconds();
   console.log(result);
   // Expected output: "resolved"
 }
 asyncCall();

 // Output:
 // "calling"
 // "resolved"
```

#### async/await:

* `async` marks a function as asynchronous, meaning it will return a promise.
* `await` pauses the execution of the function until the promise is resolved or rejected.

Using async/await:

```javascript
async function fetchData() {
  let result = await fetch('https://api.example.com/data');
  let data = await result.json();
  console.log(data);
}

fetchData();
```

#### Key Differences:

* `async`/`await` makes code appear synchronous and easier to understand, while Promises are asynchronous and often require `.then()` and `.catch()` for handling success and errors.
* Error handling with `async/await` is done using `try`/`catch`, which can be more intuitive compared to `.catch()` with promises.

### 6\. **What are arrow functions, and how do they differ from regular functions?**

Arrow functions are a shorthand syntax for writing functions. They are more concise and do not have their own `this`, `arguments`, `super`, or `new.target`. Arrow functions inherit `this` from their lexical scope.

Example:

```javascript
// Regular function
function sum(a, b) {
  return a + b;
}

// Arrow function
const sum = (a, b) => a + b;
```

**Difference**: Arrow functions are not hoisted and do not have their own `this`.

### 7\. **What is event delegation in JavaScript?**

**Event delegation** is a technique where instead of adding event listeners to individual child elements, you add a single event listener to a parent element. The event listener is triggered when an event bubbles up from a child element.

Example:

```javascript
document.querySelector('#parent').addEventListener('click', function(event) {
  if (event.target && event.target.matches('button')) {
    console.log('Button clicked!');
  }
});
```

### 8\. **What is the Event Loop in JavaScript? How It Works**

The **event loop** is a mechanism that handles asynchronous operations in JavaScript. It continuously checks the call stack and the message queue. When the call stack is empty, it pushes tasks from the message queue to the call stack for execution.

#### How it Works:

* JavaScript is single-threaded, meaning it can only execute one operation at a time.
* The event loop continuously checks the **call stack** for functions that need to be executed.
* When asynchronous code (like a `setTimeout`, promise, or event listener) is invoked, it is added to the **message queue** (also called the **task queue**).
* The event loop moves tasks from the message queue to the call stack for execution when the call stack is empty.

Here's a simplified flow:

1. **Call Stack**: Synchronous code gets pushed onto the stack and executed.
2. **Web APIs** (like `setTimeout`): Asynchronous operations are handled by the browser or Node.js environment (outside the main thread).
3. **Message Queue**: Once an asynchronous task completes, it moves to the message queue.
4. The **Event Loop** checks if the call stack is empty. If it is, it pushes the next task from the queue onto the call stack.

This allows JavaScript to handle asynchronous events efficiently without blocking the execution of other tasks.

### 9\. **What is the difference between synchronous and asynchronous code?**

* **Synchronous code**: Executes sequentially, blocking the next operation until the current one is completed.
* **Asynchronous code**: Executes independently, allowing other operations to run without waiting for it to complete.

Example:

* Synchronous: Code is executed in sequence, blocking the next operation until the current one is finished.

  ```javascript
  console.log("First");
  console.log("Second");
  ```

* Asynchronous (with `setTimeout`): Code that runs in the background without blocking the main thread. Operations like HTTP requests, timers, and file I/O are asynchronous.

  ```javascript
  console.log("First");
  setTimeout(() => console.log("Second"), 1000);
  console.log("Third");
  ```

### 10\. **How does JavaScript handle asynchronous code (callbacks, promises, async/await)?**

* **Callbacks**: Functions passed as arguments to other functions to be executed later, usually once an asynchronous operation is completed.
* **Promises**: Represent a value that may be available now or in the future, allowing chaining of `.then()` and `.catch()`.
* **Async/Await**: Allows asynchronous code to be written in a synchronous style, simplifying handling of asynchronous operations.

### 11\. **What is the difference between call(), apply(), and bind() in JavaScript?**

These methods are used to change the context (`this`) of a function.

* **`call()`**: Invokes the function immediately with a specified `this` value and arguments.

  ```javascript
   function greet(name) {
    console.log(`Hello, ${name}`);
  }
  greet.call(this, 'Alice');
  ```

* **`apply()`**: Similar to `call()`, but arguments are passed as an array.

  ```javascript
  greet.apply(this, ['Alice']);
  ```

* **`bind()`**: Returns a new function with a specified `this` value, but it does not invoke the function immediately.

  ```javascript
   const greetAlice = greet.bind(this, 'Alice');
  greetAlice();
  ```

### 12\. **What are the map(), filter(), and reduce() methods?**

* **`map()`**: Creates a new array by applying a function to each element in an existing array.

  ```javascript
   const numbers = [1, 2, 3];
  const squares = numbers.map(x => x * x);  // [1, 4, 9]
  ```

* **`filter()`**: Creates a new array with elements that pass a given condition.

  ```javascript
   const numbers = [1, 2, 3, 4];
  const evenNumbers = numbers.filter(x => x % 2 === 0);  // [2, 4]
  ```

* **`reduce()`**: Reduces the array to a single value based on a function.

  ```javascript
   const numbers = [1, 2, 3];
  const sum = numbers.reduce((acc, curr) => acc + curr, 0);  // 6
  ```

### 13\. **What is the spread operator (...), and how is it used?**

The **spread operator** (`...`) is used to unpack elements from an array or object, or to spread values in function calls or array literals.

Example:

* **Arrays**:

  ```javascript
   const arr1 = [1, 2];
  const arr2 = [...arr1, 3, 4];  // [1, 2, 3, 4]
  ```

* **Objects**:

  ```javascript
   const obj1 = { name: "Alice" };
  const obj2 = { ...obj1, age: 25 };  // { name: "Alice", age: 25 }
  ```

### 14\. **What is destructuring in JavaScript?**

**Destructuring** allows you to extract values from arrays or objects into variables in a concise way.

* **Array Destructuring**:

  ```javascript
   const arr = [1, 2, 3];
  const [a, b] = arr;  // a = 1, b = 2
  ```

* **Object Destructuring**:

  ```javascript
   const person = { name: "Alice", age: 25 };
  const { name, age } = person;  // name = "Alice", age = 25
  ```

### 1\. **What are template literals and how are they used?**

Template literals are a feature in JavaScript that allows you to work with strings in a more flexible way. They are enclosed by backticks (`` ` ``) instead of single or double quotes, and allow for embedding expressions inside the string using `${}`.

**Example:**

```javascript
 codelet name = "Alice";
let age = 30;
let greeting = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(greeting); 
// Output: Hello, my name is Alice and I am 30 years old.
```

You can also create multi-line strings without needing escape characters:

```javascript
 codelet message = `This is a string
that spans multiple lines.`;
console.log(message);
```

### 15\. **How does JavaScript handle errors with try, catch, and finally?**

In JavaScript, errors in asynchronous code can be handled in two main ways:

1. **Using `.catch()` with Promises**: If the promise is rejected, the error can be caught using `.catch()`.

   ```javascript
    myPromise.then(result => {
     console.log(result);
   }).catch(error => {
     console.log('Error:', error);
   });
   ```

2. **Using `try/catch` with async/await**: If you are using `async`/`await`, you can handle errors more synchronously inside a `try/catch` block.

   ```javascript
    async function fetchData() {
     try {
       let data = await someAsyncOperation();
       console.log(data);
     } catch (error) {
       console.log('Error:', error);
     }
   }
   ```
  
* **`try`**: Executes code that might throw an error.
* **`catch`**: Handles errors if any occur in the `try` block.
* **`finally`**: Executes code after `try`/`catch`, regardless of whether an error occurred.

In both cases, you handle the error where the promise or asynchronous function is invoked.

### 16\. **What are modules in JavaScript, and how do you export and import them?**

**Modules** allow you to split your code into smaller, reusable pieces.

* **Exporting**:

  ```javascript
  // export.js
  export const greeting = "Hello";
  export function sayHello() {
    console.log("Hello");
  }
  ```

* **Importing**:

  ```javascript
  // import.js
  import { greeting, sayHello } from './export.js';
  console.log(greeting);  // "Hello"
  sayHello();             // "Hello"
  ```

## Advanced-Level Questions

Sure! Let's dive into these JavaScript concepts in detail.

---

### 1\. **What is the prototype chain in JavaScript?**

The **prototype chain** is a fundamental feature in JavaScript that allows objects to inherit properties and methods from other objects. Every JavaScript object has a `[[Prototype]]` property (also accessible via `__proto__`), which refers to another object. If a property or method is called on an object and it doesn’t exist on that object, JavaScript looks up the chain to the object's prototype, then the prototype's prototype, and so on, until it either finds the property or reaches the end of the chain (i.e., `Object.prototype`, which is `null`).

### 2\. **What is the `bind()` method used for in JavaScript?**

The `bind()` method in JavaScript is used to create a **new function** that, when invoked, has its `this` value set to a specific object and allows pre-setting parameters (partial function application). It doesn’t immediately call the function but returns a new function with the specified context.

Example:

```javascript
 const obj = { value: 42 };
const getValue = function() {
  return this.value;
};

const boundGetValue = getValue.bind(obj);
console.log(boundGetValue());  // 42
```

### 3\. **What is the difference between a shallow copy and a deep copy?**

* **Shallow copy**: Creates a new object but only copies the top-level properties. If the property is an object, it still refers to the same object in memory (i.e., nested objects are not copied, but referenced).
* **Deep copy**: Creates a new object and recursively copies all the properties, including nested objects, ensuring that no references to the original objects remain.

Example:

```javascript
let shallowCopy = [...originalArray]; // shallow copy
let deepCopy = JSON.parse(JSON.stringify(originalArray)); // deep copy (works with JSON-serializable data)
```

### 4\. **What are IIFE (Immediately Invoked Function Expressions), and when are they used?**

An **IIFE** is a function expression that is defined and executed immediately. It is often used to create a new scope to avoid polluting the global namespace or to encapsulate logic within a function.

Example:

```javascript
(function() {
  // This function runs immediately
  console.log('Hello from IIFE');
})();
```

IIFE is commonly used in JavaScript modules, closures, and when you want to avoid polluting the global scope.

### 5\. **What is the difference between `Object.create()` and the `new` keyword in JavaScript?**

* **`Object.create(proto)`**: Creates a new object with the specified prototype object (`proto`). It doesn't run a constructor function. Example:

  ```javascript
   const obj = Object.create(protoObject);
  ```

* **`new` keyword**: Creates a new object, sets the prototype to the constructor's prototype, and executes the constructor function. Example:

  ```javascript
   function Person(name) {
    this.name = name;
  }
  const person = new Person('Alice');
  ```

### 6\. **Explain the concept of JavaScript design patterns, such as Singleton or Module.**

* **Design Patterns** are reusable solutions to common software design problems. In JavaScript, some common patterns are:

  * **Singleton Pattern**: Ensures that a class has only one instance and provides a global point of access to that instance.

    ```javascript
     const Singleton = (function() {
      let instance;
      function createInstance() {
        return new Object('I am a singleton');
      }
      return {
        getInstance: function() {
          if (!instance) {
            instance = createInstance();
          }
          return instance;
        }
      };
    })();
    ```

  * **Module Pattern**: Used to encapsulate private data and expose only certain methods, maintaining a clean namespace.

    ```javascript
     const Module = (function() {
      let privateVar = 'I am private';
      return {
        publicMethod: function() {
          console.log(privateVar);
        }
      };
    })();
    ```

### 7\. **What is the purpose of the `Symbol` type in JavaScript?**

`Symbol` is a primitive data type introduced in ES6, used to create **unique identifiers** for object properties. Symbols are often used to avoid property name collisions, particularly for non-enumerable properties.

Example:

```javascript
 const sym = Symbol('description');
const obj = {
  [sym]: 'value'
};
console.log(obj[sym]); // 'value'
```

### 8\. **How does JavaScript event delegation work, and why is it useful?**

Event delegation is a technique where instead of attaching event listeners to each individual element, you attach a single listener to a parent element. This works by leveraging the event bubbling mechanism, where events propagate from the target element up through the DOM tree.

It’s useful because it reduces memory usage and allows handling events for dynamically added elements.

Example:

```javascript
document.querySelector('#parent').addEventListener('click', function(event) {
  if (event.target && event.target.matches('button.className')) {
    // Handle the button click event
  }
});
```

**How it works**: 
- Instead of adding an event listener to each child element, you add one listener to a common ancestor (like a container element) and use the event's `target` property to determine which child element triggered the event.

**Use case**:  
- Dynamically added items: Suppose you have a list where new items are added via JavaScript. Instead of adding event listeners to each new list item, you can add a listener to the parent `<ul>` element and use event delegation to handle clicks on `<li>` elements.

**Why it's useful:**

* Reduces memory usage by minimizing the number of event listeners.
* Works with dynamically added elements (elements that may not exist at the time the listener is attached).

### 9\. **What are Web Workers, and how do they work in JavaScript?**

**Web Workers** allow JavaScript to run in the background on a separate thread, without blocking the main thread. They are useful for tasks that are CPU-intensive or require heavy computations (e.g., large data processing) without freezing the UI.

Example:

```javascript
 const worker = new Worker('worker.js');
worker.postMessage('Hello Worker!');
worker.onmessage = function(event) {
  console.log('Received from worker:', event.data);
};
```

### 10\. **What are generators in JavaScript, and how do they differ from regular functions?**

Generators are functions that can pause execution and later resume from where they left off using the `yield` keyword. They return an iterator, which allows you to iterate over the function’s yielded values.

Difference:

* Regular functions execute from start to finish.
* Generators can pause with `yield` and resume when `next()` is called.

Example:

```javascript
 function* myGenerator() {
  yield 1;
  yield 2;
  yield 3;
}
const gen = myGenerator();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
```

### 11\. **What are the Proxy and Reflect objects in JavaScript?**

* **Proxy**: A special object that allows you to define custom behavior for fundamental operations (e.g., property lookup, assignment, function invocation). Example:

  ```javascript
   const proxy = new Proxy(target, handler);
  ```

* **Reflect**: A built-in object that provides methods for intercepting and manipulating JavaScript operations (e.g., getting and setting properties). It is often used in conjunction with `Proxy`. Example:

  ```javascript
  Reflect.set(target, 'prop', value);
  ```

### 2\. **Explain the concept of memoization and provide an example.**

#### **Memoization**:

Memoization is an optimization technique used to speed up repeated function calls by storing (or "memoizing") the results of expensive function calls. When the function is called again with the same arguments, it returns the cached result instead of recomputing it.

This is particularly useful for functions with high computational cost and overlapping subproblems (e.g., recursive algorithms).

#### **Example**:

Here's a simple example of memoization for the Fibonacci sequence calculation:

```javascript
 function memoize(fn) {
  const cache = {};
  return function(...args) {
    const key = JSON.stringify(args); // Create a unique key for each set of arguments
    if (key in cache) {
      return cache[key];
    } else {
      const result = fn(...args);
      cache[key] = result;
      return result;
    }
  };
}

// Regular Fibonacci function (recursive)
function fibonacci(n) {
  if (n <= 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

// Memoized Fibonacci function
const memoizedFibonacci = memoize(fibonacci);

console.log(memoizedFibonacci(40)); // Much faster after the first computation
```

**Why it works**:

* The first time `fibonacci(40)` is called, the function will compute the result.
* For subsequent calls, it will use the cached result, drastically reducing the time complexity.

---

### 13\. **How does JavaScript handle concurrency with async/await, Promises, and Event Loop?**

JavaScript uses an **event loop** to manage asynchronous operations, allowing non-blocking execution.

* **Promises**: Represent a value that may be available now, in the future, or never.
* **async/await**: Allows asynchronous code to be written in a synchronous-like style.
* The **Event Loop** ensures that asynchronous callbacks are processed after the current stack of synchronous operations is completed.

### 4\. **What is throttling and debouncing? How do they help with performance?**

#### **Throttling**:

Throttling ensures that a function is called at most once in a specified interval, no matter how frequently the event is triggered. This is useful for limiting the rate of execution during events that fire frequently (e.g., scrolling, resizing).

* **Use case**: If you have a scroll event handler that updates the UI on every scroll, throttling can make sure the handler runs only once every 100ms, for example.

```javascript
 code// Throttling example
function throttle(fn, wait) {
  let lastTime = 0;
  return function(...args) {
    const now = Date.now();
    if (now - lastTime >= wait) {
      lastTime = now;
      fn(...args);
    }
  };
}

window.addEventListener('scroll', throttle(() => {
  console.log('Scrolled!');
}, 200));
```

#### **Debouncing**:

Debouncing ensures that a function is called only after a certain delay, and the call is made only after the event stops firing for a specified period. It's useful for input fields or search bars where you only want to make the request after the user stops typing.

* **Use case**: In a search box, you only want to make a search request after the user has stopped typing for a certain duration.

```javascript
 code// Debouncing example
function debounce(fn, delay) {
  let timeoutId;
  return function(...args) {
    clearTimeout(timeoutId);
    timeoutId = setTimeout(() => fn(...args), delay);
  };
}

const input = document.querySelector('input');
input.addEventListener('input', debounce(() => {
  console.log('Searching...');
}, 500));
```

---

### **How do throttling and debouncing help with performance?**

* **Throttling**:

  * Throttling ensures that functions, especially those triggered by frequent events (like scrolling, resizing, or mouse movements), do not execute too many times in a short period. It improves performance by reducing the number of expensive operations that happen in quick succession.

* **Debouncing**:

  * Debouncing is helpful for scenarios where you only want to respond after the event has settled down. This is especially useful in situations like form validation or search queries, where making requests or calculations on every keystroke could lead to unnecessary server calls or processing.

Both techniques help in preventing excessive function executions, which can lead to performance bottlenecks, especially in complex or resource-heavy operations.

---

### Summary:

* **Memoization** is an optimization technique that caches function results to avoid redundant computations.
* **Memory leaks** in JavaScript can be prevented by clearing event listeners, intervals, and using weak references.
* **Throttling** and **debouncing** limit the frequency of function executions during frequent events, improving performance by reducing unnecessary computations.

### 15\. **How do you optimize performance in large-scale JavaScript applications?**

Optimization techniques summary:

* Minifying and compressing JavaScript.
* Using lazy loading and dynamic imports.
* Code splitting.
* Avoiding excessive DOM manipulation.
* Reducing reflows and repaints.
* Using Web Workers for heavy computations.

Optimizing JavaScript code for better performance involves several strategies:

#### a. **Minimize DOM Manipulations**

* Direct manipulation of the DOM is one of the slowest operations in JavaScript. Try to minimize it by:
  * Batch DOM updates (e.g., using `documentFragment` or `innerHTML` to make bulk changes).
  * Use virtual DOM frameworks (e.g., React, Vue) for efficient updates.

#### b. **Avoid Repeated Computations**

* Avoid recalculating the same values multiple times, especially in loops. Cache values if necessary.

#### c. **Asynchronous Programming**

* Use asynchronous operations (Promises, `async/await`) instead of blocking operations. This can help with UI responsiveness and prevent the thread from being blocked for long tasks (e.g., API calls).

#### d. **Use Efficient Data Structures**

* Choose the right data structure for the task at hand:
  * Arrays are good for ordered collections.
  * Objects or Maps are better for key-value lookups.
  * Sets can be useful for unique values.

#### e. **Debounce and Throttle Events**

* Use debouncing and throttling to manage performance of high-frequency events (scrolling, resizing, keypress).

#### f. **Minimize Memory Leaks**

* Ensure to clear intervals, timeouts, and event listeners that are no longer needed.
* Avoid unnecessary global variables and always clean up references to DOM elements and data when they are no longer in use.

#### g. **Lazy Loading**

* Only load assets (images, scripts) when they are needed, instead of all upfront.

#### h. **Use Web Workers for Heavy Computation**

* Move heavy computation to Web Workers to keep the UI thread responsive.

#### i. **Reduce HTTP Requests**

* Minimize the number of HTTP requests and use bundling or HTTP/2 to reduce latency.

### 16\. **Explain how JavaScript works in the browser: What happens when a webpage loads?**

When a webpage loads, the browser performs the following steps:

1. **Parsing HTML**: Builds the DOM (Document Object Model).
2. **Parsing CSS**: Builds the CSSOM (CSS Object Model).
3. **Rendering**: Combines DOM and CSSOM to render the page.
4. **JavaScript Execution**: Executes any embedded JavaScript, modifying the DOM/CSSOM and handling events.

The **event loop** coordinates asynchronous tasks while executing the synchronous code.

### 17\. **What is the difference between localStorage, sessionStorage, and cookies in JavaScript?**

* **localStorage**: Stores data persistently, even after the browser is closed.
* **sessionStorage**: Stores data for the duration of the page session (data is cleared when the page is closed).
* **Cookies**: Can store data with an expiration date and are sent with every HTTP request.

---

### 3\. **How do you handle memory leaks in JavaScript?**

Memory leaks occur when objects are no longer in use but are still being referenced, preventing the garbage collector from freeing up the memory. Here's how you can handle and prevent memory leaks in JavaScript:

#### a. **Use `WeakMap` or `WeakSet` for Caching**

* If you need to store references to objects, use `WeakMap` or `WeakSet`. These types allow garbage collection to remove objects when they are no longer referenced.

#### b. **Remove Event Listeners**

* Always remove event listeners when they're no longer needed. For example:
  ```javascript
   const button = document.querySelector('button');
  function handleClick() { console.log('clicked'); }
  button.addEventListener('click', handleClick);

  // When done
  button.removeEventListener('click', handleClick);
  ```

#### c. **Clear Timeouts and Intervals**

* When using `setTimeout` or `setInterval`, make sure to clear them when they are no longer needed.
  ```javascript
   const intervalId = setInterval(() => { console.log('Running'); }, 1000);

  // Clear when done
  clearInterval(intervalId);
  ```

#### d. **Avoid Global Variables**

* Limit the use of global variables, as they stay in memory for the duration of the page's lifecycle.

#### e. **Check Detached DOM Elements**

* Ensure that DOM nodes that are removed from the page are properly cleaned up, as references to them can prevent garbage collection.

#### f. **Profiling and Monitoring**

* Use browser developer tools to profile memory usage and track potential leaks, especially in long-running applications.

---



## Miscellaneous/Conceptual Questions

Sure! Let's go through each of the JavaScript questions one by one:

---

### 1\. **What are closures and lexical scoping?**

* **Lexical Scoping**: This means that the scope of variables is determined by where they are declared in the code. In JavaScript, functions are lexically scoped, meaning they "remember" the environment in which they were created, even if they are executed outside of that environment.

* **Closures**: A closure is a function that retains access to its lexical scope (variables) even after the function that created those variables has finished executing. This is powerful because it allows for private data encapsulation and function factory patterns.

  Example:

  ```javascript
   function outer() {
    let x = 10;
    return function inner() {
      console.log(x);  // `inner` has access to `x` because of the closure
    };
  }

  const myClosure = outer();
  myClosure();  // 10
  ```

  **Usefulness in frontend development:**

* Closures are useful for data encapsulation and creating private variables.
* They help in implementing function factories, event listeners, and callbacks that need access to the outer scope (e.g., preserving state in asynchronous callbacks or keeping track of event listeners).

---

### 3\. **What is the JavaScript event loop, and how does it affect performance?**

The **event loop** is a mechanism that handles the execution of multiple pieces of code in JavaScript. JavaScript is single-threaded, meaning it executes code line-by-line in one thread. The event loop ensures that tasks are executed asynchronously by managing the call stack and the event queue.

* **Call Stack**: The call stack contains functions that are currently being executed.
* **Event Queue**: When asynchronous operations (like timers or HTTP requests) complete, their callbacks are placed in the event queue.
* **Event Loop**: The event loop checks if the call stack is empty, and if it is, it moves tasks from the event queue to the call stack.

**Impact on performance**:

* Asynchronous code (e.g., setTimeout, AJAX, Promises) does not block the main thread. However, if there are too many tasks in the event queue or long-running operations on the call stack, it can delay the execution of further tasks and cause performance issues like UI freezes.

---

### 4\. **How does JavaScript handle inheritance?**

JavaScript uses **prototype-based inheritance**.

* **Prototype Chain**: Every object in JavaScript has a prototype object. When you try to access a property or method on an object, JavaScript first checks if the object has it. If not, it looks at the object's prototype, then the prototype's prototype, and so on until it reaches `null`.

* **ES6 Class Syntax**: While JavaScript is prototype-based, ES6 introduced `class` syntax to simplify object-oriented patterns. However, it is still based on prototype inheritance under the hood.

Example:

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  
  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks`);
  }
}

const dog = new Dog('Buddy');
dog.speak(); // Buddy barks
```

Here, `Dog` inherits from `Animal` using `extends`, and both classes use prototype chains to establish inheritance.

---

### 5\. **What is the role of the fetch API in JavaScript?**

The **Fetch API** provides a modern, promise-based approach to making asynchronous HTTP requests (replacing older methods like `XMLHttpRequest`).

* **Usage**: It is used to request resources (like data from a server) and handle the response asynchronously.

Example:

```javascript
 fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

* **Benefits**: Fetch is cleaner, returns Promises, and is more flexible (supports `GET`, `POST`, etc.). It's built on top of the Promise API and is easier to work with for modern asynchronous operations.

---

### 6\. **What is the difference between synchronous and asynchronous programming in JavaScript?**

* **Synchronous**: In synchronous programming, tasks are executed one after another in sequence. Each task must finish before the next one begins. This can block execution, especially for time-consuming tasks (e.g., file I/O, HTTP requests).

* **Asynchronous**: Asynchronous programming allows tasks to run independently, and the program doesn't wait for one task to finish before moving on to the next one. This helps avoid blocking the main thread and improves performance, especially for I/O-bound operations.

Example of synchronous:

```javascript
console.log('Start');
console.log('Middle');
console.log('End');
```

Example of asynchronous (using `setTimeout`):

```javascript
console.log('Start');
setTimeout(() => console.log('Middle'), 1000);
console.log('End');
```

Here, "Middle" is logged after 1 second without blocking "End".

---

### 7\. **Explain the concept of "callback hell" and how to avoid it.**

A **callback** is a function passed as an argument to another function that is executed once the asynchronous operation completes.

* **Callback Hell** (or Pyramid of Doom) refers to nested callbacks that make code hard to read, understand, and maintain. This usually happens when you have multiple asynchronous operations that depend on each other.

#### Problem of "Callback Hell":

* When you have multiple asynchronous operations that depend on each other, you may end up with deeply nested callbacks, often referred to as **callback hell** or **pyramid of doom**.
* This can make the code hard to read, maintain, and debug.

Example:

```javascript
doSomething(function(err, result) {
  if (err) {
    console.error(err);
  } else {
    doAnotherThing(result, function(err, result2) {
      if (err) {
        console.error(err);
      } else {
        doYetAnotherThing(result2, function(err, result3) {
          // and so on...
        });
      }
    });
  }
});
```

**Avoiding Callback Hell**:

1. **Promises**: Use Promises to flatten nested callbacks and chain them in a more readable way.
2. **Async/Await**: This syntax makes asynchronous code look more like synchronous code and avoids deeply nested callbacks.

Example using async/await:

```javascript
async function fetchData() {
  try {
    const result1 = await asyncFunction1();
    const result2 = await asyncFunction2();
    const result3 = await asyncFunction3();
  } catch (err) {
    console.error(err);
  }
}
```

---

### 8\. **What are the different ways to handle errors in JavaScript?**

There are several ways to handle errors in JavaScript:

* **`try...catch`**: The most common way to catch and handle errors in synchronous code.

  ```javascript
  try {
    throw new Error('Something went wrong');
  } catch (err) {
    console.error(err.message);
  }
  ```

* **Promises**: For asynchronous operations, you can use `.catch()` to handle errors.

  ```javascript
  someAsyncFunction().catch(err => console.error(err));
  ```

* **Async/Await**: Use `try...catch` around `await` to handle errors in asynchronous code.

  ```javascript
  try {
    const data = await fetchData();
  } catch (err) {
    console.error(err);
  }
  ```

---

### 9\. **What is the purpose of JavaScript's eval() function?**

The `eval()` function evaluates JavaScript code represented as a string. While it can be powerful, it is also dangerous because it allows execution of arbitrary code, which can lead to security vulnerabilities (e.g., code injection).

Example:

```javascript
eval('console.log("Hello from eval!")'); // Outputs: Hello from eval!
```

**Caution**: Avoid using `eval()` unless absolutely necessary due to potential security risks and performance concerns. It can also hinder optimizations by JavaScript engines.

---
  

## Bonus: JavaScript Frameworks and Libraries

Here’s an in-depth look at the questions you’ve asked, covering various concepts related to JavaScript frameworks and bundlers:

### 1\. **What is the Virtual DOM, and how does it work in React?**

The **Virtual DOM** (VDOM) is a lightweight, in-memory representation of the actual DOM elements on the web page. In React, the Virtual DOM acts as a staging area where React can perform operations before applying changes to the real DOM. This helps to optimize performance.

#### How it works:

* React maintains a **Virtual DOM** to improve efficiency. When a component’s state changes, React updates the Virtual DOM first.
* It then compares the updated Virtual DOM with the previous version using an algorithm called **reconciliation**.
* After the comparison, React calculates the most efficient way to update the real DOM and applies the minimal set of changes (also known as **diffing**).
* This process reduces unnecessary re-rendering and speeds up the application’s performance.

### 2\. **What is the difference between React, Vue, and Angular?**

Here’s a breakdown of the differences between these three popular frameworks:

* **React**:

  * **Type**: Library (focused on UI components).
  * **Development Style**: Component-based; uses JSX (JavaScript + HTML syntax).
  * **State Management**: React itself doesn’t have built-in state management, but libraries like Redux or React’s Context API can be used.
  * **Ecosystem**: React focuses on the view layer, so additional libraries (like React Router and state management tools) are needed.
  * **Learning Curve**: Moderate, especially if you are new to concepts like JSX, hooks, or functional programming.

* **Vue.js**:

  * **Type**: Framework (focuses on everything from the view to state management).
  * **Development Style**: Component-based with a focus on simplicity. It uses templates similar to HTML and also supports JSX.
  * **State Management**: Vue provides **Vuex** for state management out-of-the-box.
  * **Ecosystem**: Vue is more opinionated than React, providing a complete solution for routing (Vue Router) and state management (Vuex).
  * **Learning Curve**: Easy to moderate, with a clear and intuitive API. Vue has a simpler learning curve compared to React and Angular.

* **Angular**:

  * **Type**: Full-fledged framework (complete solution for building web applications).
  * **Development Style**: Component-based with TypeScript by default, which is a statically typed superset of JavaScript.
  * **State Management**: Angular uses services for state management and provides RxJS for handling asynchronous events.
  * **Ecosystem**: Angular comes with everything built-in (routing, state management, form handling, HTTP requests, etc.), which can be both a strength and a limitation.
  * **Learning Curve**: Steep due to its reliance on TypeScript and complex tooling.

### 3\. **Explain the concept of one-way data binding in React.**

**One-way data binding** means that data flows in a single direction: from the parent component to child components. In React:

* The **state** (data) is managed within the component (usually in the parent).
* A parent component passes down its state as **props** to child components.
* Child components cannot directly modify the parent’s state. Instead, they can trigger events (such as button clicks) that inform the parent component to update the state, and React will re-render components based on the new state.

This makes data flow predictable and easier to manage.

### 4\. **What is the role of Redux in React applications?**

**Redux** is a state management library often used with React applications. It helps manage the application state in a centralized store rather than having multiple local component states. Redux follows the principle of **unidirectional data flow**.

* **Store**: Holds the application’s state.
* **Actions**: Represent events that describe state changes.
* **Reducers**: Functions that specify how the state changes in response to actions.

By using Redux, you can manage complex application state in a more predictable and scalable way, especially for large applications with many components that need to share state.

### 5\. **What is Vue.js, and what are its main features?**

**Vue.js** is a progressive JavaScript framework for building user interfaces. It focuses on being easy to integrate into projects while also being capable of powering complex single-page applications (SPAs).

#### Main features:

* **Declarative Rendering**: Vue uses an HTML-based template syntax that allows you to declaratively bind the DOM to the underlying Vue instance’s data.
* **Component System**: Vue is built around a component-based architecture, which promotes reusability and separation of concerns.
* **Reactivity**: Vue’s reactive data binding automatically updates the view when data changes.
* **Vue Router**: Vue's official library for client-side routing.
* **Vuex**: Vue's official state management library.
* **Directives**: Vue uses special tokens like `v-if`, `v-for`, `v-bind` to bind attributes, control logic, and handle events.

### 6\. **What is Angular, and how does it differ from React and Vue?**

**Angular** is a platform and framework for building client-side applications using HTML, CSS, and TypeScript. Unlike React and Vue, Angular is a full-fledged framework, providing everything you need to build a web application.

#### Key Differences:

* **TypeScript by Default**: Angular uses TypeScript, while React and Vue are written in JavaScript (with TypeScript support).
* **Opinionated Framework**: Angular provides built-in tools for routing, forms, HTTP requests, and more, while React and Vue are more flexible and allow you to choose your tools.
* **Two-way Data Binding**: Angular supports two-way data binding, meaning that changes to the model automatically update the view and vice versa. React and Vue use one-way data binding by default.
* **Complexity**: Angular can be more difficult to learn due to its extensive tooling, dependency injection system, and more rigid structure.

### 7\. **How does JavaScript work with Webpack, Babel, and other bundlers?**

* **Webpack** is a module bundler that takes your JavaScript files, along with CSS, images, and other assets, and bundles them into a set of optimized files that can be loaded by the browser. It allows you to use modern JavaScript features (like ES6 modules) and compile them down to code that works in all browsers.
* **Babel** is a JavaScript compiler that converts modern JavaScript (like ES6 or JSX) into backward-compatible versions of JavaScript. It works as a transpiler, allowing you to use the latest JavaScript syntax today without worrying about browser support.
* **Other Bundlers**: Other bundlers like **Parcel** or **Rollup** work similarly to Webpack but with different setups and trade-offs. Rollup, for example, is known for optimizing libraries, while Parcel requires zero configuration to get started.

Together, **Webpack** and **Babel** (often integrated with other tools) allow developers to write modern JavaScript and have it work in older browsers without needing to manually handle the complexities of compatibility and performance optimizations.

### 8\. **What are JavaScript framework lifecycle methods (React, Vue, Angular)?**

**React**:

* **Mounting**: `constructor()`, `componentDidMount()`
* **Updating**: `shouldComponentUpdate()`, `componentDidUpdate()`
* **Unmounting**: `componentWillUnmount()`

React lifecycle methods allow you to hook into different stages of a component’s life: when it's created, updated, or destroyed.

**Vue**:

* **Lifecycle Hooks**: `beforeCreate()`, `created()`, `beforeMount()`, `mounted()`, `beforeUpdate()`, `updated()`, `beforeDestroy()`, `destroyed()`

Vue's lifecycle hooks allow you to execute code at various stages, similar to React, but they are more intuitive and offer a more granular set of lifecycle events.

**Angular**:

* **Lifecycle Hooks**: `ngOnInit()`, `ngOnChanges()`, `ngDoCheck()`, `ngAfterViewInit()`, `ngAfterViewChecked()`, `ngOnDestroy()`

Angular provides a robust set of lifecycle hooks tied to the component lifecycle and change detection system, allowing for finer control over how components interact with the application’s state and UI.

---
