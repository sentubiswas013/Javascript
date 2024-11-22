**\# JavaScript Interview Questions & Answers**

## Basic JavaScript Concepts


## Arrays and Strings

Here are the JavaScript answers for the questions you asked:

### 1\. **Reverse a string without using built-in methods:**

To reverse a string without using the `reverse()` method or any other built-in methods, you can manually iterate through the string.

```javascript
 function reverseString(str) {
  let reversed = '';
  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }
  return reversed;
}
```

### 2\. **Remove duplicate values from an array:**

You can remove duplicates by iterating through the array and adding elements to a new array only if they haven't been added already.

```javascript
 function removeDuplicates(arr) {
  const uniqueArr = [];
  for (let i = 0; i < arr.length; i++) {
    if (!uniqueArr.includes(arr[i])) {
      uniqueArr.push(arr[i]);
    }
  }
  return uniqueArr;
}
```

Alternatively, you can use a `Set`, but this doesn't fit the "no built-in methods" requirement:

```javascript
 function removeDuplicates(arr) {
  const uniqueArr = [];
  arr.forEach(item => {
    if (!uniqueArr.includes(item)) {
      uniqueArr.push(item);
    }
  });
  return uniqueArr;
}
```

### 3\. **Find the longest word in a string:**

To find the longest word in a string, you can split the string into words, then iterate through the array of words to find the longest one.

```javascript
 function findLongestWord(str) {
  const words = str.split(' ');
  let longestWord = '';
  for (let i = 0; i < words.length; i++) {
    if (words[i].length > longestWord.length) {
      longestWord = words[i];
    }
  }
  return longestWord;
}
```

### 4\. **Check if a string is a palindrome:**

A palindrome reads the same backward as forward. To check if a string is a palindrome, compare the string with its reversed version.

```javascript
 function isPalindrome(str) {
  let reversed = '';
  for (let i = str.length - 1; i >= 0; i--) {
    reversed += str[i];
  }
  return str === reversed;
}
```

### 5\. **Flatten a nested array (array of arrays):**

To flatten a nested array, you can use a recursive function to go through each element. If an element is an array, recursively flatten it.

```javascript
 function flattenArray(arr) {
  let result = [];
  for (let i = 0; i < arr.length; i++) {
    if (Array.isArray(arr[i])) {
      result = result.concat(flattenArray(arr[i]));
    } else {
      result.push(arr[i]);
    }
  }
  return result;
}
```

### 6\. **Find the missing number in an array containing numbers from 1 to n:**

One efficient way to find the missing number is to use the formula for the sum of the first `n` natural numbers:

<math><semantics><mrow><mtext>Sum of first n numbers</mtext><mo>\=</mo><mfrac><mrow><mi>n</mi><mo>(</mo><mi>n</mi><mo>+</mo><mn>1</mn><mo>)</mo></mrow><mn>2</mn></mfrac></mrow><annotation>\\text{Sum of first n numbers} = \\frac{n(n + 1)}{2}</annotation></semantics></math>Sum of first n numbers\=2n(n+1)​

Then, subtract the sum of the array from the expected sum to find the missing number.

```javascript
 function findMissingNumber(arr, n) {
  const expectedSum = (n * (n + 1)) / 2;
  const actualSum = arr.reduce((sum, num) => sum + num, 0);
  return expectedSum - actualSum;
}
```

This solution assumes that the array contains numbers from 1 to `n` but with one number missing.

Let me know if you need any further clarification on these solutions!

## Objects and Data Structures

### 1\. **Merge two sorted arrays into a single sorted array**

To merge two sorted arrays into one sorted array, we can use a two-pointer approach to iterate through both arrays simultaneously and merge them in sorted order.

```javascript
 function mergeSortedArrays(arr1, arr2) {
    let result = [];
    let i = 0, j = 0;

    // Compare elements from both arrays and push the smaller one to the result
    while (i < arr1.length && j < arr2.length) {
        if (arr1[i] < arr2[j]) {
            result.push(arr1[i]);
            i++;
        } else {
            result.push(arr2[j]);
            j++;
        }
    }

    // If there are remaining elements in arr1
    while (i < arr1.length) {
        result.push(arr1[i]);
        i++;
    }

    // If there are remaining elements in arr2
    while (j < arr2.length) {
        result.push(arr2[j]);
        j++;
    }

    return result;
}

console.log(mergeSortedArrays([1, 3, 5], [2, 4, 6])); // [1, 2, 3, 4, 5, 6]
```

### 2\. **Deep clone an object**

A deep clone means creating a new object and copying over all properties, including nested objects. This can be done manually or using libraries like `lodash`. Below is a manual implementation:

```javascript
 function deepClone(obj) {
    if (obj === null || typeof obj !== 'object') return obj;

    let clone = Array.isArray(obj) ? [] : {};

    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            clone[key] = deepClone(obj[key]);  // Recursively clone the object or array
        }
    }

    return clone;
}

const original = { a: 1, b: { c: 2, d: 3 } };
const cloned = deepClone(original);
console.log(cloned);  // { a: 1, b: { c: 2, d: 3 } }
console.log(cloned.b !== original.b);  // true (deep clone)
```

### 3\. **Shallow copy vs Deep copy in JavaScript**

* **Shallow copy**: Copies the top-level properties of an object. If any property is an object or array, it references the original one (does not clone deeply). This means changes to nested objects will affect both the original and the copied object.

* **Deep copy**: Recursively copies all properties, including nested objects or arrays. This ensures that the new object is completely independent of the original object, including nested objects.

Example:

```javascript
 codelet obj1 = { a: 1, b: { c: 2 } };

// Shallow copy using Object.assign or spread
let shallowCopy = { ...obj1 };
shallowCopy.b.c = 10;
console.log(obj1.b.c);  // 10 (both objects are affected)

let deepCopy = JSON.parse(JSON.stringify(obj1));
deepCopy.b.c = 20;
console.log(obj1.b.c);  // 2 (deep copy does not affect the original)
```

### 4\. **Function to count the frequency of each character in a string**

You can create a frequency counter using a hash map (object in JavaScript):

```javascript
 function charFrequency(str) {
    const freqMap = {};
    for (let char of str) {
        freqMap[char] = (freqMap[char] || 0) + 1;
    }
    return freqMap;
}

console.log(charFrequency('aabbbcccc'));  // { a: 2, b: 3, c: 4 }
```

### 5\. **Implement a hash map in JavaScript**

A basic implementation of a hash map can use an array for storing key-value pairs and a simple hash function for converting keys to array indices.

```javascript
 codeclass HashMap {
    constructor(size = 100) {
        this.size = size;
        this.map = new Array(size);
    }

    _hash(key) {
        let hash = 0;
        for (let i = 0; i < key.length; i++) {
            hash = (hash + key.charCodeAt(i)) % this.size;
        }
        return hash;
    }

    set(key, value) {
        const index = this._hash(key);
        if (!this.map[index]) {
            this.map[index] = [];
        }
        // Handle collisions with a linked list (array in this case)
        this.map[index].push([key, value]);
    }

    get(key) {
        const index = this._hash(key);
        if (this.map[index]) {
            for (let [storedKey, storedValue] of this.map[index]) {
                if (storedKey === key) {
                    return storedValue;
                }
            }
        }
        return undefined;  // Return undefined if key doesn't exist
    }

    delete(key) {
        const index = this._hash(key);
        if (this.map[index]) {
            this.map[index] = this.map[index].filter(([storedKey]) => storedKey !== key);
        }
    }
}

const map = new HashMap();
map.set("name", "John");
map.set("age", 30);
console.log(map.get("name"));  // "John"
map.delete("age");
console.log(map.get("age"));  // undefined
```

### 6\. **Implement a set in JavaScript without using the `Set` object**

You can implement a set using an object (since object keys are unique in JavaScript):

```javascript
 codeclass MySet {
    constructor() {
        this.items = {};
    }

    add(value) {
        if (!this.items.hasOwnProperty(value)) {
            this.items[value] = true;
        }
    }

    delete(value) {
        if (this.items.hasOwnProperty(value)) {
            delete this.items[value];
        }
    }

    has(value) {
        return this.items.hasOwnProperty(value);
    }

    size() {
        return Object.keys(this.items).length;
    }

    values() {
        return Obje
```

## Higher-Order Functions and Functional Programming

### 1\. **What are Higher-Order Functions?**

A **higher-order function** is a function that either:

* Takes one or more functions as arguments, or
* Returns a function as its result.

Higher-order functions are a key concept in functional programming and allow for more abstract, flexible, and reusable code. In JavaScript, functions are first-class citizens, meaning they can be passed around just like any other value (such as numbers, strings, objects, etc.).

#### Example of Higher-Order Function:

```javascript
 code// Function that takes another function as an argument
function greet(name, callback) {
  return callback(name);
}

// Function passed as a callback
function sayHello(name) {
  return `Hello, ${name}!`;
}

console.log(greet('Alice', sayHello));  // Output: Hello, Alice!
```

### 2\. **Implement `map()`, `filter()`, and `reduce()` from Scratch**

Let's implement these functions without using the built-in versions.

#### `map()`

`map()` transforms each element of an array based on a given function.

```javascript
 function customMap(arr, callback) {
  const result = [];
  for (let i = 0; i < arr.length; i++) {
    result.push(callback(arr[i], i, arr));
  }
  return result;
}

const arr = [1, 2, 3, 4];
console.log(customMap(arr, x => x * 2));  // Output: [2, 4, 6, 8]
```

#### `filter()`

`filter()` creates a new array with all elements that pass the test implemented by the provided function.

```javascript
 function customFilter(arr, callback) {
  const result = [];
  for (let i = 0; i < arr.length; i++) {
    if (callback(arr[i], i, arr)) {
      result.push(arr[i]);
    }
  }
  return result;
}

const arr = [1, 2, 3, 4, 5];
console.log(customFilter(arr, x => x % 2 === 0));  // Output: [2, 4]
```

#### `reduce()`

`reduce()` reduces the array to a single value by applying a function on each element of the array.

```javascript
 function customReduce(arr, callback, initialValue) {
  let accumulator = initialValue !== undefined ? initialValue : arr[0];
  let startIndex = initialValue !== undefined ? 0 : 1;

  for (let i = startIndex; i < arr.length; i++) {
    accumulator = callback(accumulator, arr[i], i, arr);
  }

  return accumulator;
}

const arr = [1, 2, 3, 4];
console.log(customReduce(arr, (acc, curr) => acc + curr, 0));  // Output: 10
```

### 3\. **Debounce a Given Function**

Debouncing ensures that a function is only executed after a certain delay, useful for optimizing performance when dealing with high-frequency events (e.g., window resizing, key presses).

```javascript
 function debounce(func, delay) {
  let timeout;
  
  return function(...args) {
    clearTimeout(timeout);
    timeout = setTimeout(() => func(...args), delay);
  };
}

const onResize = debounce(() => {
  console.log('Window resized!');
}, 200);

window.addEventListener('resize', onResize);
```

### 4\. **Throttle a Given Function**

Throttling ensures that a function is only called once every specified interval, regardless of how many times it is triggered.

```javascript
 function throttle(func, limit) {
  let lastFunc;
  let lastRan;

  return function(...args) {
    if (!lastRan) {
      func(...args);
      lastRan = Date.now();
    } else {
      clearTimeout(lastFunc);
      lastFunc = setTimeout(() => {
        if (Date.now() - lastRan >= limit) {
          func(...args);
          lastRan = Date.now();
        }
      }, limit - (Date.now() - lastRan));
    }
  };
}

const logScroll = throttle(() => {
  console.log('Scrolled!');
}, 1000);

window.addEventListener('scroll', logScroll);
```

### 5\. **What is Currying?**

**Currying** is a functional programming technique where a function that takes multiple arguments is transformed into a sequence of functions, each taking a single argument. This allows partial application of functions.

#### Example of Currying in JavaScript:

```javascript
 function multiply(a) {
  return function(b) {
    return a * b;
  };
}

const multiplyBy2 = multiply(2);
console.log(multiplyBy2(3));  // Output: 6

const multiplyBy5 = multiply(5);
console.log(multiplyBy5(4));  // Output: 20
```

In the above example, `multiply` is a curried function. The first function `multiply(a)` takes one argument `a` and returns another function that takes a second argument `b`. We can call `multiplyBy2` with a single argument and apply it to different values later.

## Algorithms and Problem Solving

Here are the answers to the provided JavaScript-related tasks:

### 1\. **Find the Factorial of a Number**

Factorial of a number is the product of all positive integers less than or equal to that number.

```javascript
 code// Recursive approach
function factorial(n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}

// Iterative approach
function factorialIterative(n) {
    let result = 1;
    for (let i = 1; i <= n; i++) {
        result *= i;
    }
    return result;
}
```

### 2\. **Fibonacci Sequence (Recursively and Iteratively)**

* **Recursive approach:**

```javascript
 function fibonacciRecursive(n) {
    if (n <= 1) return n;
    return fibonacciRecursive(n - 1) + fibonacciRecursive(n - 2);
}
```

* **Iterative approach:**

```javascript
 function fibonacciIterative(n) {
    let a = 0, b = 1;
    for (let i = 2; i <= n; i++) {
        let temp = a + b;
        a = b;
        b = temp;
    }
    return n === 0 ? a : b;
}
```

### 3\. **Find the Intersection of Two Arrays**

To find common elements between two arrays:

```javascript
 function intersection(arr1, arr2) {
    return arr1.filter(value => arr2.includes(value));
}
```

### 4\. **Find the First Non-Repeating Character in a String**

The first non-repeating character in a string can be found by iterating through the string and counting occurrences of each character.

```javascript
 function firstNonRepeatingCharacter(str) {
    const charCount = {};
    
    for (let i = 0; i < str.length; i++) {
        charCount[str[i]] = (charCount[str[i]] || 0) + 1;
    }
    
    for (let i = 0; i < str.length; i++) {
        if (charCount[str[i]] === 1) {
            return str[i];
        }
    }
    
    return null;  // if no non-repeating character exists
}
```

### 5\. **Largest Sum of Consecutive Elements in an Array**

To find the largest sum of consecutive elements (Kadane's algorithm):

```javascript
 function largestSumConsecutive(arr) {
    let maxSum = arr[0];
    let currentSum = arr[0];
    
    for (let i = 1; i < arr.length; i++) {
        currentSum = Math.max(arr[i], currentSum + arr[i]);
        maxSum = Math.max(maxSum, currentSum);
    }
    
    return maxSum;
}
```

### 6\. **Binary Search on a Sorted Array**

Binary search is an efficient way to search in a sorted array.

```javascript
 function binarySearch(arr, target) {
    let left = 0;
    let right = arr.length - 1;
    
    while (left <= right) {
        const mid = Math.floor((left + right) / 2);
        
        if (arr[mid] === target) return mid;
        else if (arr[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    
    return -1;  // if target is not found
}
```

### 7\. **Check If Two Strings Are Anagrams**

Two strings are anagrams if they contain the same characters in the same frequency.

```javascript
 function areAnagrams(str1, str2) {
    if (str1.length !== str2.length) return false;
    
    const charCount = {};
    
    for (let i = 0; i < str1.length; i++) {
        charCount[str1[i]] = (charCount[str1[i]] || 0) + 1;
        charCount[str2[i]] = (charCount[str2[i]] || 0) - 1;
    }
    
    return Object.values(charCount).every(count => count === 0);
}
```

### 8\. **Check If a Number Is Prime**

A prime number is a number greater than 1 that has no divisors other than 1 and itself.

```javascript
 function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i <= Math.sqrt(num); i++) {
        if (num % i === 0) return false;
    }
    return true;
}
```

### 9\. **Reverse a Linked List**

To reverse a linked list, you can iterate through the list and reverse the pointers.

```javascript
 code// Assuming a simple linked list structure like this:
function ListNode(value) {
    this.value = value;
    this.next = null;
}

function reverseLinkedList(head) {
    let prev = null;
    let current = head;
    let next = null;
    
    while (current !== null) {
        next = current.next;
        current.next = prev;
        prev = current;
        current = next;
    }
    
    return prev;  // new head of the reversed list
}
```

### Summary of the Functions:

* **Factorial**: Both recursive and iterative implementations.
* **Fibonacci**: Recursive and iterative solutions.
* **Intersection of arrays**: Using `filter` and `includes`.
* **First non-repeating character**: Using a character count map.
* **Largest sum of consecutive elements**: Using Kadane's algorithm.
* **Binary Search**: Standard binary search algorithm on sorted arrays.
* **Anagram Check**: Counting the frequency of characters.
* **Prime Check**: Looping through numbers up to the square root of `n`.
* **Reverse Linked List**: Reversing the linked list using pointers.

Let me know if you need more details or modifications to these implementations!



## ES6+ Features





## Miscellaneous/Advanced Topics

Sure! Here are detailed answers to your JavaScript questions:





### 3\. **How would you implement inheritance in JavaScript (both classical and prototypal)?**

There are two main approaches to inheritance in JavaScript: **Classical Inheritance** (using constructor functions) and **Prototypal Inheritance**.

* **Classical Inheritance** (via constructor functions): JavaScript doesn't have classical inheritance like other OOP languages (e.g., Java, C++), but you can simulate it using constructor functions and setting the prototype chain manually.

  Example:

  ```javascript
   function Animal(name) {
    this.name = name;
  }

  Animal.prototype.speak = function() {
    console.log(this.name + ' makes a noise.');
  };

  function Dog(name) {
    Animal.call(this, name); // Call parent constructor
  }

  Dog.prototype = Object.create(Animal.prototype); // Inherit from Animal
  Dog.prototype.constructor = Dog;

  const dog = new Dog('Buddy');
  dog.speak(); // Buddy makes a noise.
  ```

* **Prototypal Inheritance** (using ES6 `class` syntax): ES6 introduced the `class` syntax to make inheritance clearer.

  Example:

  ```javascript
   codeclass Animal {
    constructor(name) {
      this.name = name;
    }
    
    speak() {
      console.log(this.name + ' makes a noise.');
    }
  }

  class Dog extends Animal {
    constructor(name) {
      super(name); // Call the parent constructor
    }
  }

  const dog = new Dog('Buddy');
  dog.speak(); // Buddy makes a noise.
  ```

### 4\. **What is a JavaScript module and how do you work with modules in modern JavaScript?**

A **JavaScript module** is a piece of code that is self-contained and can be imported and exported between different files. It allows for better organization, encapsulation, and reusability of code.

* **Using ES6 Modules**: In modern JavaScript (ES6 and later), the `import` and `export` statements are used to work with modules.

  **Exporting**:

  ```javascript
   code// math.js
  export function add(a, b) {
    return a + b;
  }

  export const pi = 3.14;
  ```

  **Importing**:

  ```javascript
   code// app.js
  import { add, pi } from './math.js';

  console.log(add(2, 3));  // 5
  console.log(pi);  // 3.14
  ```

  **Default Export**: You can also have a default export for a single value or function in a module.

  ```javascript
   code// myModule.js
  export default function() {
    console.log("This is a default export");
  }
  ```

  **Importing Default Export**:

  ```javascript
   code// app.js
  import myFunction from './myModule.js';
  myFunction();  // This is a default export
  ```

### 5\. **Explain the concept of "strict mode" in JavaScript.**

**Strict mode** is a way to opt into a stricter version of JavaScript that helps to catch common coding mistakes and improve performance. It restricts certain actions and throws more exceptions. It is enabled by adding `"use strict";` at the beginning of a script or function.

Key differences in strict mode:

* Disallows the use of undeclared variables.
* Prevents assignment to read-only properties.
* Disallows `eval` and `with`.
* Prevents the use of `this` in global context (it will be `undefined`).

Example:

```javascript
 code"use strict";
x = 10; // Throws an error because x is not declared
```

### 6\. **What is the difference between a forEach and a for loop in JavaScript?**

* **`forEach`**:

  * `forEach` is an array method that iterates over each item in an array.
  * It does not support breaking out of the loop (i.e., no `break` statement).
  * It can't be used with other iterable objects like objects or sets.

  Example:

  ```javascript
   const arr = [1, 2, 3];
  arr.forEach(item => console.log(item));
  ```

* **`for` Loop**:

  * The `for` loop is a general-purpose loop and can be used for any iterable, including arrays, objects, and more.
  * You can control the loop's flow using `break`, `continue`, and other loop control mechanisms.

  Example:

  ```javascript
   const arr = [1, 2, 3];
  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }
  ```

### 7\. **What are JavaScript generators and how are they used?**

A **generator** is a special type of function that can be paused and resumed. It uses the `function*` syntax and the `yield` keyword to yield multiple values over time, rather than returning a single value.

* **Generator Syntax**:

  ```javascript
   function* myGenerator() {
    yield 1;
    yield 2;
    yield 3;
  }

  const gen = myGenerator();
  console.log(gen.next().value); // 1
  console.log(gen.next().value); // 2
  console.log(gen.next().value); // 3
  console.log(gen.next().done);  // true
  ```

* **Usage**:

  * **Iterating over data**: Generators can be useful for handling large data streams or lazy evaluation (only generating values when needed).
  * **Asynchronous programming**: Generators were used in combination with `co` or `async/await` before `async/await` was introduced in ES6+.

  Example of generator-based asynchronous flow:

  ```javascript
   function* fetchData() {
    const response1 = yield fetch('url1');
    const response2 = yield fetch('url2');
    return [response1, response2];
  }
  ```

These are the core concepts you're asking about in JavaScript! Let me know if you'd like further explanations or examples.

## JavaScript and the DOM

Here are the answers to the JavaScript-related questions you posed:

### 1\. **How can you select an element in the DOM using JavaScript?**

In JavaScript, you can select an element in the DOM using several methods:

* **`getElementById()`**: Selects an element by its `id` attribute.

  ```javascript
   const element = document.getElementById('myElement');
  ```

* **`getElementsByClassName()`**: Selects all elements with a specific class.

  ```javascript
   const elements = document.getElementsByClassName('myClass');
  ```

* **`getElementsByTagName()`**: Selects all elements with a specific tag name.

  ```javascript
   const elements = document.getElementsByTagName('div');
  ```

* **`querySelector()`**: Selects the first matching element that matches a CSS selector.

  ```javascript
   const element = document.querySelector('.myClass');
  ```

* **`querySelectorAll()`**: Selects all matching elements (returns a NodeList).

  ```javascript
   const elements = document.querySelectorAll('div.myClass');
  ```

### 2\. **Write a function that updates the text content of an HTML element.**

Here's an example of a function that updates the text content of an element by its `id`:

```javascript
 function updateTextContent(elementId, newText) {
  const element = document.getElementById(elementId);
  if (element) {
    element.textContent = newText;
  }
}
```

Usage:

```javascript
 updateTextContent('myElement', 'New text content!');
```

### 3\. **Explain the difference between `addEventListener()` and `onclick`.**

* **`addEventListener()`**:

  * This method is more flexible and modern. It allows you to attach multiple event listeners to the same element, for different event types.
  * It does not overwrite existing event listeners, so it allows for better modularity and multiple handlers for the same event.
  * It also supports event capturing and bubbling.

  Example:

  ```javascript
   element.addEventListener('click', function() {
    console.log('Element clicked');
  });
  ```

* **`onclick`**:

  * This is an older, simpler way of attaching an event handler. It allows only one function to be assigned to the `onclick` property of an element, meaning if you set it again, it will overwrite the previous one.
  * It doesn’t support event capturing.

  Example:

  ```javascript
   element.onclick = function() {
    console.log('Element clicked');
  };
  ```

### 4\. **What is the purpose of event bubbling and capturing in JavaScript?**

Event bubbling and capturing are two phases of event propagation in the DOM:

* **Event Bubbling**:

  * This is the default behavior where an event starts from the innermost target element and bubbles up to the outer elements (parent elements) until it reaches the root (`document`).
  * It is useful when you want to handle events on a parent element and have the same event handler for multiple child elements.

  Example:

  ```javascript
   codedocument.getElementById('parent').addEventListener('click', function() {
    console.log('Parent clicked');
  });

  document.getElementById('child').addEventListener('click', function() {
    console.log('Child clicked');
  });
  ```

  In this case, clicking the `child` will log both "Child clicked" and "Parent clicked" (due to bubbling).

* **Event Capturing**:

  * In capturing, the event starts at the outermost parent element and propagates down to the target element.
  * This phase is not commonly used, but can be enabled by specifying `{ capture: true }` when adding an event listener.

  Example:

  ```javascript
   codedocument.getElementById('parent').addEventListener('click', function() {
    console.log('Parent clicked');
  }, true);  // This enables capturing
  ```

  In this case, clicking on the child element would log "Parent clicked" first, followed by "Child clicked" (because of capturing).

### 5\. **How would you dynamically add a new element to the DOM?**

You can dynamically create and add an element to the DOM using the following steps:

1. **Create a new element** with `document.createElement()`.
2. **Set its attributes** or content (e.g., using `textContent`, `classList`, etc.).
3. **Append it to a parent element** using `appendChild()` or `insertBefore()`.

Example:

```javascript
 function addNewElement() {
  // Step 1: Create a new <div> element
  const newDiv = document.createElement('div');
  
  // Step 2: Set the text content
  newDiv.textContent = 'This is a dynamically added element';
  
  // Step 3: Append the new element to the body or a specific container
  document.body.appendChild(newDiv);
}
```

Usage:

```javascript
 codeaddNewElement();
```

This will create a new `<div>` element with the specified text and append it to the `body` of the document.

---

### **Interview Preparation Tips**

1. **Understand the fundamentals**:

   * Be comfortable with **scoping** (global vs. local), **closures**, and **prototypal inheritance**. These are core to understanding how JavaScript works, especially when it comes to asynchronous behavior, performance, and debugging.

2. **Practice coding**:

   * Regular practice helps refine your problem-solving skills and speed. Platforms like **LeetCode**, **HackerRank**, **Codewars**, and **Exercism** provide a wide range of algorithmic challenges, which are common in interviews.

3. **Know the latest features**:

   * ES6+ brought many enhancements like **arrow functions**, **destructuring**, **async/await**, and **promises**. Knowing when and how to use these features makes your code cleaner and easier to maintain.

4. **Solve problems in different ways**:

   * Always explore multiple approaches to solving a problem. For example, you could solve a sorting problem using different algorithms like **QuickSort**, **MergeSort**, or **BubbleSort**. Make sure you can discuss the time complexity and space complexity of your solutions (e.g., O(n log n) vs O(n²)).

Good luck with your interview preparation!
