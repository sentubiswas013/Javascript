# JavaScript output based interview questions 
---

#### Click :star: if you like it!!
Every contribution counts, regardless of its size. I value and appreciate the efforts of all contributors, from beginners to seasoned developers. Join me on this exciting journey of open-source collaboration. **Together, let's build something amazing!** :handshake:

---

#### Contribution Guidelines

- :point_right: Please ensure that your contributions adhere to the coding style and guidelines of this project
- :point_right: Include clear and concise commit messages for all your commits
- :point_right: Provide a detailed description of your changes in the pull request.
- :point_right: Be respectful and considerate towards other contributors.

---

**1. What will be the output**
```js
let arr = [1, 2, 3, 4, 5, -6, 7];
arr.length = 0;
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ ]</li>
	<li><b>Reason</b> : The length of the array has been set to 0, so the array becomes empty.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**2. What will be the output**
```js
x = 10;
console.log(x);
var x;
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The declaration of the variable x is hoisted to the top of its scope.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**3. What will be the output**
```js
let a = { x: 1, y: 2 }
let b = a;
b.x = 3;
console.log(a);
console.log(b);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { x: 3, y: 2 } { x: 3, y: 2 }</li>
	<li><b>Reason</b> : 'a' and 'b' both are pointing to the same reference.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**4. What will be the output**
```js
for(var i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times, "value is 10"</li>
	<li><b>Reason</b> : "var" has a function scope, and there will be only one shared binding for the iterations. By the time the setTimeout function gets executed, the for loop has already completed and the value of the variable i is 10.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**5. What will be the output**
```js
for(let i = 0; i < 10; i++){
    setTimeout(function(){
      console.log("value is " + i);
  })
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10 times "value is" followed by the value of i in each iteration, from 0 to 9</li>
	<li><b>Reason</b> : "let" has a block scope, and a new binding will be created for each iteration. Here, a new variable i is created and has a different value for each iteration of the loop.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**6. What will be the output**
```js
function hello() {
  console.log("1");
    setTimeout(() => {
        console.log("2");
    })
  console.log("3");
}
hello();
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "1" followed by "3", and then after a small delay, "2"</li>
	<li><b>Reason</b> : console.log("1") statement logs "1" to the console. Then setTimeout() function is set to execute the callback function in the next event loop iteration and logs "3" to the console.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**7. What will be the output**
```js
let f = "8";
let a = 1;
console.log((+f)+a+1);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : The expression (+f) is a shorthand way to convert the string value of f to a number. Therefore, (+f) evaluates to 8.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**8. What will be the output**
```js
let a = 10;
if(true){
   let a = 20;
   console.log(a, "inside");
}
console.log(a, "outside");
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "inside" and 10, "outside"</li>
	<li><b>Reason</b> : The variable "a" declared inside "if" has block scope and does not affect the value of the outer "a" variable.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**9. What will be the output**
```js
var a = "xyz";
var a = "pqr";
console.log(a)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "pqr"</li>
	<li><b>Reason</b> : Both the variables are declared using "var" keyword with the same name "a". The second variable declaration will override the first variable declaration.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**10. What will be the output**
```js
const arr1 = [1, 2, 3, 4];
const arr2 = [6, 7, 5];
const result = [...arr1, ...arr2];
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [1, 2, 3, 4, 6, 7, 5]</li>
	<li><b>Reason</b> : Spread operator (...) concatenates the two arrays into "result" array.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**11. What will be the output**
```js
const person1 = { name: 'xyz', age: 21 };
const person2 = { city: 'abc', ...person1 };
console.log(person2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : { city: 'abc', name: 'xyz', age: 21 }</li>
	<li><b>Reason</b> : Spread operator (...) copies all the properties from person1 into person2.</li>
</ul>
</details> 

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**12. What will be the output**
```js
console.log(5 < 6 < 7);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : In JavaScript, the < operator evaluates expressions from left to right. First, the expression 5 < 6 is evaluated, resulting in true because 5 is less than 6. Then, the expression true < 7 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 < 7, which is true.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**13. What will be the output**
```js
console.log(7 > 6 > 5);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false</li>
	<li><b>Reason</b> : In JavaScript, the > operator evaluates expressions from left to right. First, the expression 7 > 6 is evaluated, resulting in true because 7 is greater than 6. Then, the expression true > 5 is evaluated. In this case, JavaScript performs type coercion and converts true to the number 1. Therefore, the expression becomes 1 > 5, which is false.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**14. What will be the output**
```js
console.log(0 == false);
console.log(1 == true);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true, true</li>
	<li><b>Reason</b> : The == operator converts operands to a common type before making the comparison. In both the cases, the boolean value will be converted to a number, i.e., false is converted to 0 and true is converted to 1. So, the expression 0 == false is equivalent to 0 == 0 and 1 == true is equivalent to 1 == 1.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**15. What will be the output**
```js
console.log([11, 2, 31] + [4, 5, 6]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : "11,2,314,5,6"</li>
	<li><b>Reason</b> : The + operator is used for both addition and string concatenation. When you try to concatenate two arrays using the + operator, the arrays are converted to strings and then concatenated together. In this case, the arrays [11, 2, 31] and [4, 5, 6] are converted to strings as "11,2,31" and "4,5,6" respectively. Then, the two strings are concatenated, resulting in "11,2,314,5,6".</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**16. What will be the output**
```js
console.log({} == {}); 
console.log({} === {});
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false, false</li>
	<li><b>Reason</b> : When you compare objects using == or ===, it checks if they refer to the exact same object. So even if they are looking same, they are pointing to different memory locations.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**17. What will be the output**
```js
let x = 5;
let y = x++;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, 6</li>
	<li><b>Reason</b> : The post-increment operator increments and returns the value before incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**18. What will be the output**
```js
let x = 5;
let y = ++x;
console.log(y);
console.log(x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 6, 6</li>
	<li><b>Reason</b> : The pre-increment operator increments and returns the value after incrementing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**19. What will be the output**
```js
console.log('apple'.split(''));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 'a', 'p', 'p', 'l', 'e' ]</li>
	<li><b>Reason</b> : split method is used to split a string into an array of substrings based on a specified separator. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**20. What will be the output**
```js
const arr = [2,3,5,2,8,10,5];
console.log(arr.indexOf(5))
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 2</li>
	<li><b>Reason</b> : indexOf method returns the index of the first occurrence of the specified element in the array. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**21. What will be the output**
```js
const array = [8, 18, 28, 38];
const result = array.map(element => element + 2)
               .filter((element) => element > 25);
console.log(result);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ 30, 40 ]</li>
	<li><b>Reason</b> : The code increments each element in the array by 2 using map and filters out elements greater than 25 using filter.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**22. What will be the output**
```js
function checkValue(value){
    var result = Array.isArray(value);
    console.log(result);
}
checkValue([1,2,3]);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true</li>
	<li><b>Reason</b> : Array.isArray() method is used to check if the provided value is an array.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**23. What will be the output**
```js
function sum(a=5, b=7){
    return a+b;
}
console.log(sum(undefined, 20));
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 25</li>
	<li><b>Reason</b> : Here, undefined is passed as the value for parameter a, and 20 is passed for parameter b. When any parameter is undefined, the default value is used. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**24. What will be the output**
```js
console.log(10 + "5");
console.log("5" + 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 105, 510</li>
	<li><b>Reason</b> : Since one operand is a string, the + operator performs string concatenation. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**25. What will be the output**
```js
console.log(10 - "5");
console.log("5" - 10);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 5, -5</li>
	<li><b>Reason</b> : In JavaScript, when the subtraction operator - is used, the operands are converted to numbers before performing the subtraction </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**26. What will be the output**
```js
console.log(printName());
function printName(){
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Hi my name is Bob</li>
	<li><b>Reason</b> : Regular functions are hoisted to the top. And you can access and call them even before they are declared. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**


**27. What will be the output**
```js
console.log(printName());
const printName = () => {
    return "Hi my name is Bob"
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : ReferenceError: Cannot access 'printName' before initialization</li>
	<li><b>Reason</b> : Arrow functions cannot be accessed before they are initialised. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**28. What will be the output (shallow copy of an object)**
```js
const userDetails = {
  firstName: "Surbhi",
  lastName: "Dighe",
  age: 20,
  address: {
    city: "Hyderabad",
    country: "India",
  },
};

let cloneUserDetails = { ...userDetails };
//Updating original object
userDetails.age = 22;
userDetails.address.city = "Banglore";

console.log(cloneUserDetails.age); 
console.log(cloneUserDetails.address.city);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 20, "Banglore"</li>
	<li><b>Reason </b> : cloneUserDetails is created by using the spread syntax ({ ...userDetails }). This syntax creates a shallow copy of the userDetails object, meaning that the top-level properties are copied, but nested objects are still referenced.</li>
	<li><b>case 1</b> : Although userDetails.age was changed to 22, cloneUserDetails still holds the original value of 20. This is because the spread syntax only creates a shallow copy, so the age property of cloneUserDetails remains unchanged.</li>
	<li><b>case 2</b> : The nested address object is still referenced by cloneUserDetails, so when the city property of userDetails.address is changed, it reflects in cloneUserDetails.address as well. Therefore, the output is "Banglore".</li>
	</ul>

</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**29. What will be the output**
```js
function hello(){
console.log(name);
console.log(age);
var name = "Alice";
let age = 21;
}
hello();
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : undefined, ReferenceError: can't access lexical declaration 'age' before initialization"</li>
	<li><b>Reason for console.log(name)</b> : The variable name (declared with var) is hoisted to the top, so JavaScript knows it exists, but it hasn't been assigned a value yet, so it prints undefined</li>
	<li><b>Reason for console.log(age)</b> : The variable age (declared with let) is also hoisted to the top of its scope, but unlike var, it is not initialized until the line where it is declared.</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**


**30. What will be the output**
```js
const arr1 = [1,2,3];
const arr2 = [1,2,3];
const str = "1,2,3";

console.log(arr1 == str);
console.log(arr1 == arr2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : true, false</li>
	<li><b>Reason for console.log(arr1 == str)</b> : Javascript compiler performs type conversion. In this case, it converts the array arr1 and the string str to their string representations and then compares them.</li>
	<li><b>Reason for console.log(arr1==arr2) </b> : In Javascript arrays are objects and objects are compared by reference. In this case, arr1 and arr2 are pointing to 2 different memory locations</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**31. What will be the output**
```js
const a = {x : 1};
const b = {x : 1};
console.log(a === b);
console.log(a.x === b.x)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : false, true</li>
	<li><b>Reason for console.log(a === b)</b> : This compares whether a and b refer to the exact same object in memory. They are two different objects in memory, so the comparison evaluates to false</li>
	<li><b>Reason for console.log(a.x === b.x)</b> : This compares the x property of objects a and b. Since both a.x and b.x have the same value i.e., 1, so the comparison evaluates to true.</b></li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**32. What will be the output**
```js
const arr = [10, -1, 2];
arr.sort((a, b) => a - b);
console.log(arr);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [-1, 2, 10]</li>
	<li><b>Reason</b> : The compare function (a, b) => a - b sorts the numbers numerically in ascending order.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**33. What will be the output**
```js
const arr = [11, 0, '', false, 2, 1];
const filtered = arr.filter(Boolean);
console.log(filtered);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [11, 2, 1]</li>
	<li><b>Reason</b> : filter(Boolean) removes all falsy values (0, "" (empty string), false, null, undefined, and NaN) from the array and keeps truthy ones.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**34. What will be the output**
```js
var x = 0;
var y = 10;
if(x){
  console.log(x);
}
if(y){
  console.log(y);
}
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 10</li>
	<li><b>Reason</b> : x = 0 is falsy and doesn't trigger the console.log(x), while y = 10 is truthy and triggers the console.log(y).</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**35. What will be the output**
```js
const obj = {
var1: 1,
var2: 2
};
const { var1, var2 } = obj;
console.log(var1, var2);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : 1, 2</li>
	<li><b>Reason</b> : Object destructuring extracts the values of var1 and var2 from obj object and prints them using console.log(var1, var2)</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**36. What will be the output**
```js
const user = { 
name: "Surbhi dighe", 
country: "India" 
};
const { name: fullname, country } = user;
console.log(fullname);
console.log(name);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Surbhi Dighe, ReferenceError: name is not defined</li>
	<li><b>Reason for console.log(fullname)</b> : The name property from user is assigned to a local variable fullname.</li>
	<li><b>Reason for console.log(name)</b> : It gives an error because name was assigned to a local variable fullname and therefore name is not directly accessible.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**37. What will be the output**
```js
const person = {
  firstName: 'Surbhi',
};
const { lastName="dighe" } = person;
console.log(lastName);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : dighe</li>
	<li><b>Reason</b> : The lastName property is not defined in the person object and the destructuring syntax provides a default value ("dighe") to be used when the property is missing.</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**38. What will be the output**
```js
const person = {
  firstName: 'Surbhi',
};
const { firstName="Henry"} = person;
console.log(firstName);
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : Surbhi</li>
	<li><b>Reason</b> : The `firstName` property in the `person` object has the value 'Surbhi'. The default value "Henry" is ignored because it only applies when the property does not exist or is `undefined`</li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**39. What will be the output**
```js
var a = 10;
let a = 20;
console.log(a)
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : SyntaxError: Identifier 'a' has already been declared</li>
	<li><b>Reason</b> : In Javascript, we cannot redeclare a variable with let if it has already been declared in the same scope. </li>
</ul>
</details>

**[:top: Scroll to Top](#javascript-output-based-interview-questions)**

**40. What will be the output**
```js
const arr = ["A","B","C","D","E"]
console.log(Object.keys(arr)); 
```
<details>
	<summary><b>View Answer</b></summary>
<ul>	
	<li><b>Output</b> : [ '0', '1', '2', '3', '4' ]</li>
	<li><b>Reason</b> : In JavaScript, arrays are a special type of object. Object.keys() on an array returns an array of strings representing the indices of the array elements. </li>
</ul>
</details>


======================

Here is a collection of 60 tricky JavaScript coding questions, along with their answers:

### 1. **What is the output of the following code?**
```javascript
console.log([] + []);
```
**Answer:** `""` (empty string). When you add two empty arrays, JavaScript coerces them to strings, resulting in an empty string.

---

### 2. **What is the output of the following code?**
```javascript
console.log([] == []);
```
**Answer:** `false`. Arrays are reference types, so two different arrays are not equal even if they contain the same elements.

---

### 3. **What is the output of the following code?**
```javascript
console.log({} + []);
```
**Answer:** `"[object Object]"`. An object is converted to its string representation, which is "[object Object]". Adding it to an empty array results in that string.

---

### 4. **What is the output of the following code?**
```javascript
console.log([] + {});
```
**Answer:** `"[object Object]"`. The array `[]` is coerced to an empty string `""`, and then the empty object `{}` is coerced to "[object Object]".

---

### 5. **What is the output of the following code?**
```javascript
console.log([] + [1]);
```
**Answer:** `"1"`. The empty array `[]` is coerced into an empty string `""`, and then the array `[1]` becomes `"1"`, resulting in the string `"1"`.

---

### 6. **What is the output of the following code?**
```javascript
console.log(1 + "1");
```
**Answer:** `"11"`. JavaScript converts the number `1` into a string and concatenates it with the string `"1"`.

---

### 7. **What is the output of the following code?**
```javascript
console.log(true + 1);
```
**Answer:** `2`. The boolean `true` is coerced to `1`, and then `1 + 1` equals `2`.

---

### 8. **What is the output of the following code?**
```javascript
console.log("1" - 1);
```
**Answer:** `0`. JavaScript converts the string `"1"` to a number and then subtracts `1`.

---

### 9. **What is the output of the following code?**
```javascript
console.log(0.1 + 0.2 === 0.3);
```
**Answer:** `false`. This is a result of floating-point precision errors in JavaScript.

---

### 10. **What is the output of the following code?**
```javascript
console.log("0" == false);
```
**Answer:** `true`. JavaScript coerces `"0"` to a number, and `false` is coerced to `0`, so they are equal.

---

### 11. **What is the output of the following code?**
```javascript
console.log(null == undefined);
```
**Answer:** `true`. In JavaScript, `null` and `undefined` are loosely equal to each other.

---

### 12. **What is the output of the following code?**
```javascript
console.log(null === undefined);
```
**Answer:** `false`. Strict equality (`===`) does not perform type coercion, so `null` and `undefined` are not strictly equal.

---

### 13. **What is the output of the following code?**
```javascript
console.log("1" == [1]);
```
**Answer:** `true`. JavaScript coerces the array `[1]` into the string `"1"`, which is equal to `"1"`.

---

### 14. **What is the output of the following code?**
```javascript
console.log([1] == true);
```
**Answer:** `false`. The array `[1]` is an object, and objects are not loosely equal to booleans.

---

### 15. **What is the output of the following code?**
```javascript
console.log([] == false);
```
**Answer:** `true`. The empty array `[]` is coerced to an empty string `""`, which is then coerced to `false`, making the equality `true`.

---

### 16. **What is the output of the following code?**
```javascript
console.log([1] == [1]);
```
**Answer:** `false`. Arrays are reference types, and two different arrays with the same content are not equal.

---

### 17. **What is the output of the following code?**
```javascript
console.log([1] === [1]);
```
**Answer:** `false`. Strict equality compares object references, and since both arrays are different objects, they are not strictly equal.

---

### 18. **What is the output of the following code?**
```javascript
console.log(typeof NaN);
```
**Answer:** `"number"`. Even though `NaN` stands for "Not a Number," its type is still `number`.

---

### 19. **What is the output of the following code?**
```javascript
console.log(typeof typeof 1);
```
**Answer:** `"string"`. The first `typeof 1` evaluates to `"number"`, and then `typeof "number"` evaluates to `"string"`.

---

### 20. **What is the output of the following code?**
```javascript
console.log(parseInt("100px"));
```
**Answer:** `100`. `parseInt` parses the string until it encounters a non-numeric character, so it stops at the number `100`.

---

### 21. **What is the output of the following code?**
```javascript
console.log(parseInt("abc"));
```
**Answer:** `NaN`. Since the string `"abc"` does not start with a number, `parseInt` returns `NaN`.

---

### 22. **What is the output of the following code?**
```javascript
console.log(parseInt("10.5"));
```
**Answer:** `10`. `parseInt` only reads the integer part of a number, truncating the decimal portion.

---

### 23. **What is the output of the following code?**
```javascript
console.log("10" - 1);
```
**Answer:** `9`. JavaScript coerces the string `"10"` to the number `10`, and then subtracts `1`.

---

### 24. **What is the output of the following code?**
```javascript
console.log("10" * 2);
```
**Answer:** `20`. The string `"10"` is coerced to the number `10`, and then multiplied by `2`.

---

### 25. **What is the output of the following code?**
```javascript
console.log(1 + "1" - 1);
```
**Answer:** `"10"`. The `1 + "1"` results in the string `"11"`, and then `"11" - 1` coerces `"11"` to `11`, resulting in `10`.

---

### 26. **What is the output of the following code?**
```javascript
console.log(1 + "1" - "1");
```
**Answer:** `0`. The `1 + "1"` results in the string `"11"`, and `"11" - "1"` coerces `"11"` to a number and subtracts `1`, resulting in `10`.

---

### 27. **What is the output of the following code?**
```javascript
console.log(1 + 2 + "3");
```
**Answer:** `"33"`. The first addition `1 + 2` gives `3`, and then `3 + "3"` results in the string `"33"`.

---

### 28. **What is the output of the following code?**
```javascript
console.log(1 + +"1");
```
**Answer:** `2`. The unary plus (`+`) converts the string `"1"` to a number, and `1 + 1` results in `2`.

---

### 29. **What is the output of the following code?**
```javascript
console.log("1" + + "1");
```
**Answer:** `"11"`. The second `"1"` is converted to a number with the unary `+`, and then the string `"1"` is concatenated with `1`, giving `"11"`.

---

### 30. **What is the output of the following code?**
```javascript
console.log(!!"0");
```
**Answer:** `true`. Any non-empty string, including `"0"`, is coerced to `true`.

---

### 31. **What is the output of the following code?**
```javascript
console.log(!!null);
```
**Answer:** `false`. `null` is falsy, so `!!null` coerces it to `false`.

---

### 32. **What is the output of the following code?**
```javascript
console.log(!!undefined);
```
**Answer:** `false`. `undefined` is falsy, so `!!undefined` coerces it to `false`.

---

### 33. **What is the output of the following code?**
```javascript
console.log(!!0);
```
**Answer:** `false`. `0` is falsy, so `!!0` coerces it to `false`.

---

### 34. **What is the output of the following code?**
```javascript
console.log(!!1);
```
**Answer:** `true`. `1` is truthy, so `!!1` coerces it to `true`.

---

### 35. **What is the output of the following code?**
```javascript
console.log([1] == true);
```
**Answer:** `false`. An array is not equal to a boolean, even though it contains a truthy value.

---

### 36. **What is the output of the following code?**
```javascript
console.log([1] == "1");
```
**Answer:** `true`. JavaScript coerces the array `[1]` into the string `"1"`, so the comparison is true.

---

### 37. **What is the output of the following code?**
```javascript
console.log([1] == 1);
```
**Answer:** `true`. The array `[1]` is coerced into the string `"1"`, which is then coerced into the number `1`, so the comparison is true.

---

### 38. **What is the output of the following code?**
```javascript
console.log([] == ![]);
```
**Answer:** `false`. The empty array `[]` is an object, and the negation of an empty array (`![]`) results in `false`, making the comparison false.

---

### 39. **What is the output of the following code?**
```javascript
console.log(+true);
```
**Answer:** `1`. The unary `+` converts the boolean `true` to `1`.

---

### 40. **What is the output of the following code?**
```javascript
console.log(+false);
```
**Answer:** `0`. The unary `+` converts the boolean `false` to `0`.

---

### 41. **What is the output of the following code?**
```javascript
console.log(2 + "2" - 1);
```
**Answer:** `"21"`. The `2 + "2"` results in `"22"`, and `"22" - 1` coerces `"22"` to `22`, resulting in `21`.

---

### 42. **What is the output of the following code?**
```javascript
console.log("1" + 1 + 1);
```
**Answer:** `"111"`. The first `1 + 1` results in the string `"1"`, and `"1" + 1` results in `"11"`, then `"11" + 1` results in `"111"`.

---

### 43. **What is the output of the following code?**
```javascript
console.log(1 + 1 + "1");
```
**Answer:** `"21"`. The first `1 + 1` results in `2`, and then `2 + "1"` results in the string `"21"`.

---

### 44. **What is the output of the following code?**
```javascript
console.log(true + true);
```
**Answer:** `2`. `true` is coerced to `1`, so `1 + 1` equals `2`.

---

### 45. **What is the output of the following code?**
```javascript
console.log(false + false);
```
**Answer:** `0`. `false` is coerced to `0`, so `0 + 0` equals `0`.

---

### 46. **What is the output of the following code?**
```javascript
console.log("3" * "2");
```
**Answer:** `6`. The strings `"3"` and `"2"` are coerced into numbers, and then multiplied.

---

### 47. **What is the output of the following code?**
```javascript
console.log("3" / "2");
```
**Answer:** `1.5`. The strings `"3"` and `"2"` are coerced into numbers, and then divided.

---

### 48. **What is the output of the following code?**
```javascript
console.log("3" % "2");
```
**Answer:** `1`. The strings `"3"` and `"2"` are coerced into numbers, and the modulus operation returns the remainder of `3 % 2`.

---

### 49. **What is the output of the following code?**
```javascript
console.log("Hello" - "World");
```
**Answer:** `NaN`. Since subtraction is not defined for strings, the result is `NaN`.

---

### 50. **What is the output of the following code?**
```javascript
console.log([].push(1));
```
**Answer:** `1`. The `push` method returns the new length of the array, which is `1` after pushing `1`.

---

### 51. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].pop());
```
**Answer:** `3`. The `pop` method removes and returns the last element of the array.

---

### 52. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].shift());
```
**Answer:** `1`. The `shift` method removes and returns the first element of the array.

---

### 53. **What is the output of the following code?**
```javascript
console.log([].unshift(1));
```
**Answer:** `1`. The `unshift` method adds one or more elements to the beginning of the array, and returns the new length.

---

### 54. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].reverse());
```
**Answer:** `[3, 2, 1]`. The `reverse` method reverses the order of the elements in the array.

---

### 55. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].join("-"));
```
**Answer:** `"1-2-3"`. The `join` method joins all elements of the array into a string, separated by the specified separator.

---

### 56. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].concat([4, 5]));
```
**Answer:** `[1, 2, 3, 4, 5]`. The `concat` method merges arrays into one array.

---

### 57. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].slice(1, 2));
```
**Answer:** `[2]`. The `slice` method returns a shallow copy of a portion of the array.

---

### 58. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].splice(1, 1));
```
**Answer:** `[2]`. The `splice` method removes elements from an array and returns them.

---

### 59. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].every(num => num > 0));
```
**Answer:** `true`. The `every` method checks if all elements satisfy the condition.

---

### 60. **What is the output of the following code?**
```javascript
console.log([1, 2, 3].some(num => num > 2));
```
**Answer:** `true`. The `some` method checks if at least one element satisfies the condition.

========