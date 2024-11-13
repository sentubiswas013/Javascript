## JavaScript Interview Questions & Answers

#### Beginner Level
Reverse a String
Write a function that reverses a given string.

```javascript
Copy code
function reverseString(str) {
  return str.split('').reverse().join('');
}
```

#### Palindrome Check
Check if a given string is a palindrome (reads the same forwards and backwards).

```javascript
Copy code
function isPalindrome(str) {
  return str === str.split('').reverse().join('');
}
```
#### Factorial of a Number
Write a function to calculate the factorial of a number.

```javascript
Copy code
function factorial(n) {
  return n <= 1 ? 1 : n * factorial(n - 1);
}
```
#### Fibonacci Sequence
Write a function to return the nth Fibonacci number.

```javascript
Copy code
function fibonacci(n) {
  if (n <= 1) return n;
  let a = 0, b = 1;
  for (let i = 2; i <= n; i++) {
    let temp = a + b;
    a = b;
    b = temp;
  }
  return b;
}

```
#### Find Largest Number in Array
Write a function that finds the largest number in an array.

```javascript
Copy code
function findLargest(arr) {
  return Math.max(...arr);
}

```
#### Count Vowels in a String
Write a function to count the number of vowels in a string.

```javascript
Copy code
function countVowels(str) {
  return (str.match(/[aeiouAEIOU]/g) || []).length;
}

```
#### Sum of Digits
Write a function to return the sum of digits of a given number.

```javascript
Copy code
function sumOfDigits(num) {
  return num.toString().split('').reduce((sum, digit) => sum + Number(digit), 0);
}

```
### Intermediate Level
#### Find the Second Largest Number
Write a function to find the second largest number in an array.

```javascript
Copy code
function secondLargest(arr) {
  let largest = -Infinity, second = -Infinity;
  arr.forEach(num => {
    if (num > largest) {
      second = largest;
      largest = num;
    } else if (num > second && num !== largest) {
      second = num;
    }
  });
  return second;
}

```
#### Anagram Check
Write a function that checks if two strings are anagrams of each other.

```javascript
Copy code
function areAnagrams(str1, str2) {
  return str1.split('').sort().join('') === str2.split('').sort().join('');
}

```
#### Merge Two Sorted Arrays
Write a function that merges two sorted arrays into one sorted array.

```javascript
Copy code
function mergeSortedArrays(arr1, arr2) {
  let result = [];
  let i = 0, j = 0;
  while (i < arr1.length && j < arr2.length) {
    if (arr1[i] < arr2[j]) {
      result.push(arr1[i]);
      i++;
    } else {
      result.push(arr2[j]);
      j++;
    }
  }
  return result.concat(arr1.slice(i), arr2.slice(j));
}

```
#### Find Missing Number in Array
Given an array of n - 1 numbers in the range from 1 to n, find the missing number.

```javascript
Copy code
function findMissingNumber(arr, n) {
  const totalSum = (n * (n + 1)) / 2;
  const arrSum = arr.reduce((sum, num) => sum + num, 0);
  return totalSum - arrSum;
}

```
#### Remove Duplicates from Array
Write a function that removes duplicates from an array.

```javascript
Copy code
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

```
#### Longest Substring Without Repeating Characters
Write a function that returns the length of the longest substring without repeating characters.

    ```javascript
Copy code
function lengthOfLongestSubstring(str) {
  let map = new Map();
  let start = 0, maxLength = 0;
  for (let end = 0; end < str.length; end++) {
    if (map.has(str[end])) {
      start = Math.max(start, map.get(str[end]) + 1);
    }
    map.set(str[end], end);
    maxLength = Math.max(maxLength, end - start + 1);
  }
  return maxLength;
}

```
#### Count Occurrences of Character in String
Write a function to count the number of occurrences of a given character in a string.

```javascript
Copy code
function countOccurrences(str, char) {
  return (str.match(new RegExp(char, 'g')) || []).length;
}

```
### Advanced Level
Find Kth Largest Element in an Array
Write a function to find the kth largest element in an array.

```javascript
Copy code
function findKthLargest(arr, k) {
  arr.sort((a, b) => b - a);
  return arr[k - 1];
}

```
#### Implement Debounce Function
Write a debounce function that limits the rate at which a function can fire.

```javascript
Copy code
function debounce(func, delay) {
  let timeout;
  return function(...args) {
    clearTimeout(timeout);
    timeout = setTimeout(() => func(...args), delay);
  };
}

```
#### Implement Throttle Function
Write a throttle function that only allows a function to be called once every X milliseconds.

```javascript
Copy code
function throttle(func, delay) {
  let lastCall = 0;
  return function(...args) {
    const now = new Date().getTime();
    if (now - lastCall >= delay) {
      lastCall = now;
      func(...args);
    }
  };
}

```
#### Implement a Basic Promise
Implement a basic version of a Promise object.

```javascript
Copy code
class MyPromise {
  constructor(executor) {
    this.value = null;
    this.error = null;
    this.onResolve = null;
    this.onReject = null;

    try {
      executor(this.resolve.bind(this), this.reject.bind(this));
    } catch (e) {
      this.reject(e);
    }
  }

  resolve(value) {
    this.value = value;
    if (this.onResolve) {
      this.onResolve(this.value);
    }
  }

  reject(error) {
    this.error = error;
    if (this.onReject) {
      this.onReject(this.error);
    }
  }

  then(onResolve, onReject) {
    this.onResolve = onResolve;
    this.onReject = onReject;
    return this;
  }
}

```
#### LRU Cache Implementation
Implement an LRU (Least Recently Used) cache using a doubly linked list or map.

```javascript
Copy code
class LRUCache {
  constructor(capacity) {
    this.capacity = capacity;
    this.cache = new Map();
  }

  get(key) {
    if (!this.cache.has(key)) return -1;
    const value = this.cache.get(key);
    this.cache.delete(key);
    this.cache.set(key, value);
    return value;
  }

  put(key, value) {
    if (this.cache.has(key)) {
      this.cache.delete(key);
    } else if (this.cache.size >= this.capacity) {
      this.cache.delete(this.cache.keys().next().value);
    }
    this.cache.set(key, value);
  }
}

```
#### Find Longest Increasing Subsequence
Write a function to find the longest increasing subsequence in an array.

```javascript
Copy code
function longestIncreasingSubsequence(nums) {
  if (!nums.length) return 0;
  const dp = new Array(nums.length).fill(1);
  for (let i = 1; i < nums.length; i++) {
    for (let j = 0; j < i; j++) {
      if (nums[i] > nums[j]) {
        dp[i] = Math.max(dp[i], dp[j] + 1);
      }
    }
  }
  return Math.max(...dp);
}
```