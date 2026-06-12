# 🚀 JavaScript Interview Questions & Answers

A collection of the **most frequently asked JavaScript interview questions**, explained in **simple, easy-to-understand language** with practical examples — perfect for **quick revision** before an interview.

> 🎯 **Who is this for?**
> - Freshers preparing for their first developer job
> - Developers with 1-4 years of experience brushing up before interviews
> - Anyone who wants to understand JavaScript concepts in plain English (no jargon overload)

> 💡 **How to use this repo**
> - Scroll through the questions and answers directly — no clicking required, perfect for quick revision.
> - Use the [Table of Contents](#-table-of-contents) to jump straight to a topic.
> - Run the code examples yourself in your browser console (press `F12` → go to **Console** tab) to see them in action.

---

## 📑 Table of Contents

### 🟢 Section 1: Basics (Fresher Level)
1. [What is JavaScript?](#1-what-is-javascript)
2. [What are the different data types in JavaScript?](#2-what-are-the-different-data-types-in-javascript)
3. [Difference between var, let, and const](#3-difference-between-var-let-and-const)
4. [Difference between == and ===](#4-difference-between--and-)
5. [What is hoisting?](#5-what-is-hoisting)
6. [Difference between null and undefined](#6-difference-between-null-and-undefined)
7. [What are template literals?](#7-what-are-template-literals)
8. [Function declaration vs function expression](#8-function-declaration-vs-function-expression)
9. [What are arrow functions?](#9-what-are-arrow-functions)
10. [Difference between an array and an object](#10-difference-between-an-array-and-an-object)
11. [Common array methods](#11-common-array-methods)
12. [What are parameters and arguments?](#12-what-are-parameters-and-arguments)
13. [Difference between for, while, and forEach](#13-difference-between-for-while-and-foreach)
14. [What is JSON?](#14-what-is-json)
15. [What is the DOM?](#15-what-is-the-dom)

### 🟡 Section 2: Intermediate (1-3 Years Experience)
16. [What is a closure?](#16-what-is-a-closure)
17. [What is the `this` keyword?](#17-what-is-the-this-keyword)
18. [`this` in regular vs arrow functions](#18-this-in-regular-vs-arrow-functions)
19. [map() vs filter() vs reduce()](#19-map-vs-filter-vs-reduce)
20. [What are callbacks?](#20-what-are-callbacks)
21. [What is callback hell?](#21-what-is-callback-hell)
22. [What is a Promise?](#22-what-is-a-promise)
23. [What is async/await?](#23-what-is-asyncawait)
24. [What is the Event Loop?](#24-what-is-the-event-loop)
25. [Synchronous vs Asynchronous code](#25-synchronous-vs-asynchronous-code)
26. [What is destructuring?](#26-what-is-destructuring)
27. [Spread vs Rest operators](#27-spread-vs-rest-operators)
28. [What are JS modules (import/export)?](#28-what-are-js-modules-importexport)
29. [forEach vs map](#29-foreach-vs-map)
30. [Event bubbling and event capturing](#30-event-bubbling-and-event-capturing)

### 🔴 Section 3: Advanced (3-4+ Years Experience)
31. [call, apply, and bind](#31-call-apply-and-bind)
32. [What is prototypal inheritance?](#32-what-is-prototypal-inheritance)
33. [Object.freeze() vs const](#33-objectfreeze-vs-const)
34. [Debouncing vs Throttling](#34-debouncing-vs-throttling)
35. [What is memoization?](#35-what-is-memoization)
36. [Deep copy vs Shallow copy](#36-deep-copy-vs-shallow-copy)
37. [What are higher-order functions?](#37-what-are-higher-order-functions)
38. [What is currying?](#38-what-is-currying)
39. [Promise.all() vs Promise.race() vs Promise.allSettled()](#39-promiseall-vs-promiserace-vs-promiseallsettled)
40. [localStorage vs sessionStorage vs cookies](#40-localstorage-vs-sessionstorage-vs-cookies)
41. [What is event delegation?](#41-what-is-event-delegation)
42. [What are generators?](#42-what-are-generators)
43. [setTimeout vs setInterval](#43-settimeout-vs-setinterval)
44. [null vs undefined vs NaN](#44-null-vs-undefined-vs-nan)
45. [Error handling with try/catch and async/await](#45-error-handling-with-trycatch-and-asyncawait)
46. [Array.from() vs Array.of()](#46-arrayfrom-vs-arrayof)
47. [WeakMap and WeakSet](#47-weakmap-and-weakset)
48. [What is the Virtual DOM?](#48-what-is-the-virtual-dom)
49. [Optional chaining (?.) and nullish coalescing (??)](#49-optional-chaining--and-nullish-coalescing-)
50. [Pure function vs Impure function](#50-pure-function-vs-impure-function)

---

## 🟢 Section 1: Basics (Fresher Level)

### 1. What is JavaScript?

JavaScript is a programming language used to make websites interactive. While HTML gives structure and CSS gives style, JavaScript adds behavior — like button clicks, animations, and form validation.

```javascript
alert("Hello, welcome to the website!");
```
This simple line shows a pop-up message on the screen.

---

### 2. What are the different data types in JavaScript?

JavaScript has two categories of data types:

**Primitive types** (simple, single values):
- **String** (text) → `"Hello"`
- **Number** → `25`, `3.14`
- **Boolean** → `true` / `false`
- **Undefined** → a variable declared but not given a value
- **Null** → represents "nothing" intentionally
- **Symbol** → unique identifiers (advanced use)
- **BigInt** → very large numbers

**Non-primitive type:**
- **Object** (including arrays and functions)

```javascript
let name = "Rahul";      // String
let age = 25;            // Number
let isStudent = true;    // Boolean
let car;                 // Undefined
let result = null;       // Null
```

---

### 3. Difference between var, let, and const

Think of these as three ways to "create a box" to store a value, but with different rules:

- **`var`**: Old way. Can be re-declared and updated. Has function scope.
- **`let`**: Modern way. Can be updated but not re-declared in the same scope. Has block scope (only works inside `{ }`).
- **`const`**: Used for values that should never change. Cannot be updated or re-declared.

```javascript
var a = 10;
a = 20;       // OK

let b = 10;
b = 20;       // OK

const c = 10;
c = 20;       // ERROR! Cannot change a const value
```

**Analogy:** `const` is permanent ink, `let` is pencil you can erase and rewrite, and `var` is an old pencil that sometimes behaves unexpectedly.

---

### 4. Difference between == and ===

- **`==`** (loose equality): Compares values only, converting types if needed.
- **`===`** (strict equality): Compares both value AND type. No conversion happens.

```javascript
console.log(5 == "5");   // true  (because "5" is converted to 5)
console.log(5 === "5");  // false (different types: number vs string)
```

**Tip:** Always prefer `===` to avoid unexpected bugs caused by type conversion.

---

### 5. What is hoisting?

Hoisting means JavaScript moves variable and function **declarations** to the top of their scope before running the code. So you can sometimes use a function or variable before it's actually written in the code.

```javascript
sayHello(); // Works! Output: Hello

function sayHello() {
  console.log("Hello");
}
```

With `var`, the variable is hoisted but its value is not:
```javascript
console.log(x); // undefined (not an error)
var x = 5;
```

With `let` and `const`, hoisting happens too, but you can't use them before declaration — this is called the **"temporal dead zone."**

---

### 6. Difference between null and undefined

- **`undefined`**: A variable has been created but has not been assigned any value yet. JavaScript sets this automatically.
- **`null`**: A variable has been intentionally set to "no value" by the programmer.

```javascript
let a;            // undefined - JS hasn't assigned anything
let b = null;     // null - we deliberately said "this is empty"

console.log(a); // undefined
console.log(b); // null
```

**Analogy:** `undefined` is an empty box that nobody has labeled yet. `null` is a box deliberately marked as "empty."

---

### 7. What are template literals?

Template literals let you create strings using backticks (`` ` ``) instead of quotes, and you can directly insert variables using `${}`.

```javascript
let name = "Sara";
let age = 22;

// Old way
console.log("My name is " + name + " and I am " + age + " years old.");

// New way (template literal)
console.log(`My name is ${name} and I am ${age} years old.`);
```

Both print the same thing, but template literals are cleaner and easier to read.

---

### 8. Function declaration vs function expression

- **Function Declaration:** Defined with the `function` keyword and a name. It is hoisted (can be called before it's defined).
- **Function Expression:** A function stored inside a variable. It is NOT hoisted the same way.

```javascript
// Function Declaration
function greet() {
  console.log("Hello!");
}

// Function Expression
const greetAgain = function() {
  console.log("Hi there!");
};
```

---

### 9. What are arrow functions?

Arrow functions are a shorter way to write functions, introduced in ES6.

```javascript
// Normal function
function add(a, b) {
  return a + b;
}

// Arrow function
const add2 = (a, b) => a + b;

console.log(add(2, 3));   // 5
console.log(add2(2, 3));  // 5
```

Arrow functions are shorter and also handle `this` differently (see Q18).

---

### 10. Difference between an array and an object

- **Array:** A list of items, accessed by index numbers (starting from 0).
- **Object:** A collection of data stored as key-value pairs, accessed by names (keys).

```javascript
// Array
let fruits = ["Apple", "Banana", "Mango"];
console.log(fruits[0]); // Apple

// Object
let person = {
  name: "Aman",
  age: 30
};
console.log(person.name); // Aman
```

**Analogy:** An array is a numbered list of items in a cart. An object is a form where each field has a label (name, age, etc.) and a value.

---

### 11. Common array methods

| Method | What it does | Example |
|---|---|---|
| `push()` | Adds item to the end | `arr.push(5)` |
| `pop()` | Removes the last item | `arr.pop()` |
| `shift()` | Removes the first item | `arr.shift()` |
| `unshift()` | Adds item to the start | `arr.unshift(0)` |
| `map()` | Creates a new array by transforming each item | see below |
| `filter()` | Creates a new array with items that pass a condition | see below |
| `reduce()` | Combines all items into a single value | see below |

```javascript
let numbers = [1, 2, 3, 4, 5];

// map: double each number
let doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// filter: keep only even numbers
let evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // [2, 4]

// reduce: add all numbers together
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 15
```

---

### 12. What are parameters and arguments?

A function is a reusable block of code that performs a task. **Parameters** are placeholders in the function definition. **Arguments** are the actual values passed when calling the function.

```javascript
function greet(name) {  // "name" is a parameter
  console.log(`Hello, ${name}!`);
}

greet("Priya"); // "Priya" is an argument
// Output: Hello, Priya!
```

---

### 13. Difference between for, while, and forEach

- **`for`**: Used when you know exactly how many times to repeat something.
- **`while`**: Used when you want to repeat something until a condition becomes false.
- **`forEach`**: A method specifically for arrays, to run a function on each item.

```javascript
// for loop
for (let i = 0; i < 3; i++) {
  console.log("for loop:", i);
}

// while loop
let i = 0;
while (i < 3) {
  console.log("while loop:", i);
  i++;
}

// forEach loop (only for arrays)
[10, 20, 30].forEach(item => {
  console.log("forEach:", item);
});
```

---

### 14. What is JSON?

JSON stands for **JavaScript Object Notation**. It's a lightweight text format used to store and exchange data, especially between a browser and a server (APIs).

```javascript
// JSON data (looks like an object, but it's text)
let jsonData = '{"name": "John", "age": 28}';

// Convert JSON text into a JavaScript object
let obj = JSON.parse(jsonData);
console.log(obj.name); // John

// Convert a JavaScript object into JSON text
let backToJson = JSON.stringify(obj);
console.log(backToJson); // '{"name":"John","age":28}'
```

**Remember:** `JSON.parse()` = text → object. `JSON.stringify()` = object → text.

---

### 15. What is the DOM?

DOM stands for **Document Object Model**. It is a representation of the webpage as a tree of objects that JavaScript can read and change.

```javascript
// Change the text of an element with id="title"
document.getElementById("title").innerText = "New Heading";

// Change the background color of the page
document.body.style.backgroundColor = "lightblue";
```

**Analogy:** The DOM is a tree of boxes representing every part of your webpage (headings, paragraphs, buttons). JavaScript can grab any box and change its content, style, or behavior.

---

## 🟡 Section 2: Intermediate (1-3 Years Experience)

### 16. What is a closure?

A closure is when a function "remembers" the variables from the place it was created, even after that outer function has finished running.

```javascript
function outerFunction() {
  let count = 0;

  return function innerFunction() {
    count++;
    console.log(count);
  };
}

const counter = outerFunction();
counter(); // 1
counter(); // 2
counter(); // 3
```

Even though `outerFunction()` has already finished, `innerFunction` still remembers and can use `count`. This is a closure.

**Real-life use:** Closures are commonly used to create private variables, like a counter that can't be changed directly from outside.

---

### 17. What is the `this` keyword?

`this` refers to the object that is currently "calling" or "owning" the function. Its value depends on HOW a function is called, not where it's written.

```javascript
const person = {
  name: "Vikas",
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};

person.greet(); // Hello, my name is Vikas
```

Here, `this` refers to `person` because `greet` was called using `person.greet()`.

---

### 18. `this` in regular vs arrow functions

- Regular functions get their own `this`, which depends on how they are called.
- Arrow functions do NOT have their own `this`. They use the `this` from their surrounding (parent) scope.

```javascript
const obj = {
  name: "Test",
  regularFunc: function() {
    console.log(this.name); // "Test" - works fine
  },
  arrowFunc: () => {
    console.log(this.name); // undefined - "this" comes from outside
  }
};

obj.regularFunc();
obj.arrowFunc();
```

---

### 19. map() vs filter() vs reduce()

All three work on arrays, but for different purposes:

- **`map()`**: Transforms each item and returns a NEW array of the SAME length.
- **`filter()`**: Returns a NEW array with only the items that pass a test (can be shorter).
- **`reduce()`**: Combines all items into a SINGLE value (like a total sum).

```javascript
let prices = [100, 200, 300];

let withTax = prices.map(price => price * 1.18);     // [118, 236, 354]
let expensive = prices.filter(price => price > 150);  // [200, 300]
let total = prices.reduce((sum, price) => sum + price, 0); // 600
```

---

### 20. What are callbacks?

A callback is a function passed as an argument to another function, to be run later (often after some task completes).

```javascript
function fetchData(callback) {
  console.log("Fetching data...");
  setTimeout(() => {
    callback("Data received!");
  }, 2000);
}

fetchData(function(result) {
  console.log(result);
});

// Output (after 2 seconds):
// Fetching data...
// Data received!
```

**Real-life analogy:** You order food online and give your phone number (callback). The restaurant calls you when the food is ready, instead of you waiting at the counter.

---

### 21. What is callback hell?

Callback hell happens when you nest many callbacks inside each other, making code hard to read — often shaped like a pyramid.

```javascript
getUser(1, function(user) {
  getPosts(user.id, function(posts) {
    getComments(posts[0].id, function(comments) {
      console.log(comments);
      // This keeps growing sideways...
    });
  });
});
```

**Solution:** Use Promises or `async/await` to write cleaner, more readable code.

---

### 22. What is a Promise?

A Promise is an object that represents a task that will finish in the future — either successfully (`resolved`) or with an error (`rejected`).

```javascript
let myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Task completed!");
  } else {
    reject("Task failed!");
  }
});

myPromise
  .then(result => console.log(result))   // runs if resolved
  .catch(error => console.log(error));   // runs if rejected
```

**Analogy:** A Promise is like ordering a pizza. You get a "promise" (receipt) immediately, and later you either get the pizza (resolved) or get told it's out of stock (rejected).

---

### 23. What is async/await?

`async/await` is a cleaner way to work with Promises. It lets you write asynchronous code that looks like normal step-by-step (synchronous) code.

```javascript
function getData() {
  return new Promise(resolve => {
    setTimeout(() => resolve("Here is your data"), 1000);
  });
}

async function showData() {
  console.log("Loading...");
  let result = await getData(); // waits for the promise to finish
  console.log(result);
}

showData();
// Output:
// Loading...
// (after 1 second) Here is your data
```

**Rule:** `await` can only be used inside a function marked `async`.

---

### 24. What is the Event Loop?

JavaScript runs on a single thread, meaning it can do one thing at a time. The **Event Loop** is the mechanism that allows JavaScript to handle asynchronous tasks (like `setTimeout`, API calls) without freezing the program.

```javascript
console.log("1");

setTimeout(() => {
  console.log("2");
}, 0);

console.log("3");

// Output:
// 1
// 3
// 2
```

Even though the `setTimeout` has a delay of 0, "2" prints last. This is because `setTimeout` is sent to a queue and only runs after all normal code finishes. The event loop manages this queue.

---

### 25. Synchronous vs Asynchronous code

- **Synchronous:** Code runs line-by-line, one task must finish before the next starts.
- **Asynchronous:** Some tasks (like loading data from a server) run in the background, and the rest of the code continues without waiting.

```javascript
console.log("Start");

setTimeout(() => {
  console.log("Middle (this took 2 seconds)");
}, 2000);

console.log("End");

// Output:
// Start
// End
// Middle (this took 2 seconds)
```

---

### 26. What is destructuring?

Destructuring lets you quickly "unpack" values from arrays or objects into separate variables.

```javascript
// Object destructuring
const person = { name: "Neha", age: 27 };
const { name, age } = person;
console.log(name); // Neha
console.log(age);  // 27

// Array destructuring
const colors = ["red", "green", "blue"];
const [first, second] = colors;
console.log(first);  // red
console.log(second); // green
```

---

### 27. Spread vs Rest operators

They look the same (`...`) but are used differently:

- **Spread:** "Expands" items from an array/object into individual elements.
- **Rest:** "Collects" multiple values into a single array.

```javascript
// Spread - combining arrays
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combined = [...arr1, ...arr2];
console.log(combined); // [1, 2, 3, 4, 5, 6]

// Spread - copying an object
const original = { a: 1, b: 2 };
const copy = { ...original, c: 3 };
console.log(copy); // { a: 1, b: 2, c: 3 }

// Rest - collecting arguments
function sum(...numbers) {
  return numbers.reduce((total, n) => total + n, 0);
}
console.log(sum(1, 2, 3, 4)); // 10
```

---

### 28. What are JS modules (import/export)?

Modules let you split your code into separate files and share code between them using `export` (to share) and `import` (to use).

`math.js`:
```javascript
export function add(a, b) {
  return a + b;
}
```

`app.js`:
```javascript
import { add } from './math.js';

console.log(add(5, 3)); // 8
```

This keeps code organized, reusable, and easier to maintain — especially in large projects.

---

### 29. forEach vs map

- **`forEach`**: Runs a function on each item but does NOT return a new array (returns `undefined`).
- **`map`**: Runs a function on each item AND returns a new array with the results.

```javascript
let numbers = [1, 2, 3];

let result1 = numbers.forEach(n => n * 2);
console.log(result1); // undefined

let result2 = numbers.map(n => n * 2);
console.log(result2); // [2, 4, 6]
```

**Tip:** Use `forEach` when you just want to "do something" with each item (like printing). Use `map` when you want a new, transformed array.

---

### 30. Event bubbling and event capturing

When you click on an element, the click event doesn't just affect that element — it travels through the DOM tree.

- **Bubbling:** The event starts at the clicked element and moves UP to its parent elements (default behavior).
- **Capturing:** The event starts from the top (root) and moves DOWN to the clicked element.

```javascript
document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
});

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});

// If you click the child element, output is:
// Child clicked
// Parent clicked   (event "bubbles up" to the parent)
```

---

## 🔴 Section 3: Advanced (3-4+ Years Experience)

### 31. call, apply, and bind

All three are used to control what `this` refers to inside a function.

- **`call()`**: Calls the function immediately, passing arguments one by one.
- **`apply()`**: Calls the function immediately, passing arguments as an array.
- **`bind()`**: Returns a NEW function with `this` fixed, but does NOT call it immediately.

```javascript
const person1 = { name: "Aarav" };
const person2 = { name: "Diya" };

function greet(greeting) {
  console.log(`${greeting}, ${this.name}`);
}

greet.call(person1, "Hello");   // Hello, Aarav
greet.apply(person2, ["Hi"]);   // Hi, Diya

const boundGreet = greet.bind(person1, "Hey");
boundGreet(); // Hey, Aarav
```

---

### 32. What is prototypal inheritance?

In JavaScript, objects can "inherit" properties and methods from other objects through something called a **prototype**. Every object has a hidden link to another object (its prototype), and if a property isn't found on the object, JavaScript looks at the prototype.

```javascript
const animal = {
  eat: function() {
    console.log("Eating...");
  }
};

const dog = Object.create(animal); // dog "inherits" from animal
dog.bark = function() {
  console.log("Barking...");
};

dog.eat();  // Eating... (inherited from animal)
dog.bark(); // Barking... (its own method)
```

---

### 33. Object.freeze() vs const

- **`const`** prevents you from reassigning the VARIABLE to a new value.
- **`Object.freeze()`** prevents you from changing the CONTENTS of an object.

```javascript
const person = { name: "Karan" };

person.name = "Rohan"; // This works! const doesn't protect object content
console.log(person.name); // Rohan

const frozenPerson = Object.freeze({ name: "Karan" });
frozenPerson.name = "Rohan"; // Silently ignored (or throws error in strict mode)
console.log(frozenPerson.name); // Karan
```

---

### 34. Debouncing vs Throttling

Both are techniques to control how often a function runs, especially for events like scrolling, resizing, or typing — to improve performance.

- **Debouncing:** Wait until the user STOPS doing the action for a certain time, then run the function once.
- **Throttling:** Run the function at most once every fixed time interval, no matter how often the event happens.

```javascript
function debounce(func, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer);
    timer = setTimeout(() => func(...args), delay);
  };
}

const search = debounce((query) => {
  console.log("Searching for:", query);
}, 500);

// Even if the user types fast, "Searching for..." 
// only runs 500ms after they STOP typing
```

**Real-life analogy:**
- Debounce = an elevator that waits a few seconds after the last person enters before closing the door.
- Throttle = a water tap that only lets water out once every 5 seconds, no matter how much you press it.

---

### 35. What is memoization?

Memoization is a performance technique where you "remember" (cache) the results of expensive function calls, so if the same input is given again, the function returns the saved result instead of recalculating.

```javascript
function memoizedAdd() {
  const cache = {};

  return function(num) {
    if (cache[num]) {
      console.log("Returning from cache");
      return cache[num];
    } else {
      console.log("Calculating result");
      const result = num + 10;
      cache[num] = result;
      return result;
    }
  };
}

const add = memoizedAdd();
console.log(add(5)); // Calculating result -> 15
console.log(add(5)); // Returning from cache -> 15
```

---

### 36. Deep copy vs Shallow copy

- **Shallow copy:** Copies only the top-level properties. If a property is an object/array, both the original and copy still point to the SAME nested object.
- **Deep copy:** Copies everything, including nested objects, so the copy is completely independent.

```javascript
const original = { name: "Tina", address: { city: "Delhi" } };

// Shallow copy
const shallow = { ...original };
shallow.address.city = "Mumbai";
console.log(original.address.city); // Mumbai (changed too! - same nested object)

// Deep copy
const deep = JSON.parse(JSON.stringify(original));
deep.address.city = "Pune";
console.log(original.address.city); // Mumbai (NOT changed - fully independent)
```

---

### 37. What are higher-order functions?

A higher-order function is a function that either:
1. Takes another function as an argument, OR
2. Returns a function as its result.

```javascript
// Takes a function as argument
function processArray(arr, callback) {
  return arr.map(callback);
}

const doubled = processArray([1, 2, 3], (num) => num * 2);
console.log(doubled); // [2, 4, 6]

// Returns a function
function multiplier(factor) {
  return function(num) {
    return num * factor;
  };
}

const double = multiplier(2);
console.log(double(5)); // 10
```

`map`, `filter`, and `reduce` are all examples of higher-order functions.

---

### 38. What is currying?

Currying is a technique where a function that takes multiple arguments is transformed into a series of functions that each take ONE argument.

```javascript
// Normal function
function add(a, b, c) {
  return a + b + c;
}
console.log(add(1, 2, 3)); // 6

// Curried function
function curriedAdd(a) {
  return function(b) {
    return function(c) {
      return a + b + c;
    };
  };
}
console.log(curriedAdd(1)(2)(3)); // 6
```

**Why it's useful:** It allows you to create specialized versions of a function by "pre-filling" some arguments.

```javascript
const add5 = curriedAdd(5);
const add5and10 = add5(10);
console.log(add5and10(20)); // 35
```

---

### 39. Promise.all() vs Promise.race() vs Promise.allSettled()

These help manage multiple Promises at once:

- **`Promise.all()`**: Waits for ALL promises to finish. If even one fails, the whole thing fails.
- **`Promise.race()`**: Returns the result of whichever promise finishes FIRST (success or failure).
- **`Promise.allSettled()`**: Waits for ALL promises to finish, regardless of success or failure, and gives results for each.

```javascript
const p1 = new Promise(resolve => setTimeout(() => resolve("P1 done"), 1000));
const p2 = new Promise(resolve => setTimeout(() => resolve("P2 done"), 2000));

Promise.all([p1, p2]).then(results => {
  console.log(results); // ["P1 done", "P2 done"] - after 2 seconds
});

Promise.race([p1, p2]).then(result => {
  console.log(result); // "P1 done" - after 1 second (fastest one)
});
```

---

### 40. localStorage vs sessionStorage vs cookies

All three are used to store small amounts of data in the browser, but with differences:

| Feature | localStorage | sessionStorage | Cookies |
|---|---|---|---|
| Storage limit | ~5-10 MB | ~5-10 MB | ~4 KB |
| Expiry | Never (until manually cleared) | When the tab/browser is closed | Can be set with an expiry date |
| Sent to server? | No | No | Yes, with every request |

```javascript
// localStorage - stays even after closing the browser
localStorage.setItem("username", "John");
console.log(localStorage.getItem("username")); // John

// sessionStorage - cleared when tab is closed
sessionStorage.setItem("tempData", "123");
console.log(sessionStorage.getItem("tempData")); // 123
```

---

### 41. What is event delegation?

Event delegation means attaching a single event listener to a PARENT element instead of adding listeners to many CHILD elements individually. This works because of event bubbling.

```javascript
// Instead of adding a click listener to every <li>, 
// add ONE listener to the parent <ul>
document.getElementById("list").addEventListener("click", function(event) {
  if (event.target.tagName === "LI") {
    console.log("You clicked:", event.target.textContent);
  }
});
```

**Why it's useful:** Better performance, and it automatically works for new items added later (like dynamically added list items).

---

### 42. What are generators?

A generator is a special type of function that can be paused and resumed. It uses the `function*` syntax and the `yield` keyword.

```javascript
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
}

const gen = numberGenerator();

console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3
```

Each call to `.next()` runs the function until the next `yield`, then pauses.

---

### 43. setTimeout vs setInterval

- **`setTimeout`**: Runs a function ONCE after a specified delay.
- **`setInterval`**: Runs a function REPEATEDLY at a specified interval, until stopped.

```javascript
// Runs once after 2 seconds
setTimeout(() => {
  console.log("This runs once after 2 seconds");
}, 2000);

// Runs every 2 seconds, repeatedly
const intervalId = setInterval(() => {
  console.log("This repeats every 2 seconds");
}, 2000);

// To stop it after some time:
setTimeout(() => clearInterval(intervalId), 10000);
```

---

### 44. null vs undefined vs NaN

- **`undefined`**: A variable exists but has no value yet.
- **`null`**: Intentional "empty" value, set by the programmer.
- **`NaN`**: Stands for "Not a Number" — happens when a math operation fails to produce a valid number.

```javascript
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null

let c = "hello" * 2;
console.log(c); // NaN

console.log(typeof a);   // "undefined"
console.log(typeof b);   // "object" (this is a known quirk in JavaScript!)
console.log(typeof c);   // "number" (yes, NaN is technically of type "number")
```

---

### 45. Error handling with try/catch and async/await

With `async/await`, you can use regular `try/catch` blocks (just like synchronous code) to handle errors from Promises.

```javascript
async function getUserData() {
  try {
    let response = await fetch("https://api.example.com/user");
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.log("Something went wrong:", error.message);
  }
}

getUserData();
```

If `fetch` fails (e.g., no internet), the `catch` block runs instead of crashing the program.

---

### 46. Array.from() vs Array.of()

- **`Array.from()`**: Creates an array from an array-like or iterable object (like a string, Set, or NodeList).
- **`Array.of()`**: Creates an array from the given arguments directly.

```javascript
console.log(Array.from("hello"));    // ['h', 'e', 'l', 'l', 'o']
console.log(Array.from({length: 3}, (_, i) => i * 2)); // [0, 2, 4]

console.log(Array.of(7));            // [7]
console.log(new Array(7));           // [ <7 empty items> ] -- different!
```

---

### 47. WeakMap and WeakSet

`WeakMap` and `WeakSet` are like `Map` and `Set`, but they hold "weak" references to objects. This means if an object stored in them is no longer used anywhere else in the program, it can be automatically removed from memory (garbage collected).

```javascript
let user = { name: "Sahil" };

const weakMap = new WeakMap();
weakMap.set(user, "Some extra data about Sahil");

console.log(weakMap.get(user)); // "Some extra data about Sahil"

user = null; // Now, since nothing else references the original object,
             // it can be cleared from memory, along with its WeakMap entry.
```

**Use case:** Useful for storing extra/private data tied to objects without causing memory leaks.

---

### 48. What is the Virtual DOM?

The Virtual DOM is a lightweight "copy" of the real DOM, kept in memory. When data changes, frameworks like React first update the Virtual DOM, compare it with the previous version (called "diffing"), and then update only the parts of the REAL DOM that actually changed.

**Why it matters:** Updating the real DOM directly is slow. By only changing what's necessary, apps run faster and smoother.

**Analogy:** Imagine editing a 100-page document. Instead of reprinting all 100 pages every time you fix one typo, you only reprint the ONE page that changed. The Virtual DOM helps the browser do something similar.

---

### 49. Optional chaining (?.) and nullish coalescing (??)

Optional chaining (`?.`) lets you safely access deeply nested properties without worrying about errors if something in the middle is `null` or `undefined`.

```javascript
const user = {
  name: "Mira",
  address: {
    city: "Bangalore"
  }
};

console.log(user.address.city); // Bangalore

const user2 = { name: "Arjun" }; // no "address" field

// Without optional chaining, this would throw:
// Cannot read property 'city' of undefined
// console.log(user2.address.city);

// With optional chaining - safe, returns undefined instead of error
console.log(user2.address?.city); // undefined
```

There's also the **nullish coalescing operator** (`??`), which provides a default value when something is `null` or `undefined`:

```javascript
console.log(user2.address?.city ?? "City not available"); // "City not available"
```

---

### 50. Pure function vs Impure function

- **Pure function:** Always returns the same output for the same input, and does NOT change anything outside itself (no side effects).
- **Impure function:** May return different outputs for the same input, or changes something outside itself (like a global variable, the DOM, or a file).

```javascript
// Pure function
function add(a, b) {
  return a + b;
}
console.log(add(2, 3)); // always 5

// Impure function
let total = 0;
function addToTotal(num) {
  total += num; // changes a variable outside the function (side effect)
  return total;
}
console.log(addToTotal(5)); // 5
console.log(addToTotal(5)); // 10 - different output for the same input!
```

**Why it matters:** Pure functions are easier to test, debug, and reason about — which is why they're encouraged in modern JavaScript and frameworks like React.

---

## 💡 Quick Tips for Interview Day

1. Don't just memorize answers — run the code examples yourself in the browser console (`F12` → **Console** tab) to really understand them.
2. When asked a question, first give a simple one-line definition, then explain with an example — this shows clarity of thought.
3. It's okay to say "I'm not 100% sure, but here's my understanding" — interviewers value honesty and a clear thinking process over perfection.
4. Practice explaining these concepts out loud to a friend or even to yourself — this builds confidence for the real interview.

---

## 🤝 Contributing

Found a mistake or want to add more questions? Feel free to open an **Issue** or submit a **Pull Request** — this repo is meant to grow with help from the community.

## ⭐ Support

If this repo helped you in your interview prep, consider giving it a ⭐ star — it helps others find it too!

---

**Good luck with your interview preparation! 🎉**
