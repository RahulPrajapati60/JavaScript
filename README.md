
# 📘 JavaScript Interview Notes (Basic → Advanced)

> Simple definitions + small code examples for interview preparation.


## 1️⃣ What is JavaScript?
JavaScript is a programming language used to make web pages interactive.  
It runs in the browser and on the server using Node.js.

```js
console.log("Hello JavaScript");
````

---

## 2️⃣ Variables (var, let, const)

Variables are used to store data.
Prefer `let` and `const` because they are block-scoped.

```js
let a = 10;
const b = 20;
// var c = 30; (avoid var)
```

---

## 3️⃣ Data Types

JavaScript has primitive and non-primitive data types.
Objects and arrays are reference types.

```js
let num = 10;        // number
let name = "Guru";  // string
let isOk = true;    // boolean
let obj = { x: 1 }; // object
                    // null
                    // Undefined
                    // BigInt
```

---

## 4️⃣ Explicit Type Conversion

Manually converting one type to another is explicit conversion.

```js
Number("10");   // 10
String(100);    // "100"
Boolean(1);     // true
```

---

## 5️⃣ Operators (== vs ===)

`==` does type conversion, `===` checks type + value.

```js
5 == "5";   // true
5 === "5";  // false
```

---

## 6️⃣ Function

Functions are reusable blocks of code.

```js
function add(a, b) {
  return a + b;
}
```

---

## 7️⃣ Parameters vs Arguments

Parameters are variables in function definition.
Arguments are actual values passed while calling.

```js
function sum(a, b) {  // parameters
  return a + b;
}
sum(2, 3);           // arguments
```

---

## 8️⃣ Arrow Function vs Normal Function

Arrow functions have shorter syntax and no own `this`.

```js
const add = (a, b) => a + b;

function normal() {
  console.log(this);
}
```

---

## 9️⃣ this Keyword

`this` refers to the current object.

```js
const user = {
  name: "Guru",
  getName() {
    return this.name;
  }
};
```

---

## 🔟 Hoisting

`var` is hoisted with `undefined`.
`let` and `const` are in Temporal Dead Zone.

```js
console.log(a); // undefined
var a = 10;
```

---

## 1️⃣1️⃣ Object

Objects store data in key-value pairs.

```js
const car = {
  brand: "BMW",
  start() {
    return "Car started";
  }
};
```

---

## 1️⃣2️⃣ Prototype (Prototypal Inheritance)

Objects can inherit properties from another object.

```js
function Person(name) {
  this.name = name;
}
Person.prototype.sayHi = function () {
  return "Hi " + this.name;
};
```

---

## 1️⃣3️⃣ Class (ES6)

Classes are blueprints for creating objects.

```js
class User {
  constructor(name) {
    this.name = name;
  }
}
```

---

## 1️⃣4️⃣ Array + map()

`map()` returns a new array.

```js
const arr = [1, 2, 3];
const newArr = arr.map(n => n * 2);
```

---

## 1️⃣5️⃣ Map

Map stores key-value pairs with any type of keys.

```js
const map = new Map();
map.set("a", 1);
```

---

## 1️⃣6️⃣ Set

Set stores only unique values.

```js
const set = new Set([1, 1, 2, 3]);
```

---

## 1️⃣7️⃣ Callback

A function passed as an argument to another function.

```js
setTimeout(() => {
  console.log("Hello");
}, 1000);
```

---

## 1️⃣8️⃣ Promise

Promise represents a future value.

```js
const p = new Promise((resolve, reject) => {
  resolve("Done");
});

p.then(data => console.log(data));
```

---

## 1️⃣9️⃣ Async/Await + Error Handling

Async/Await makes async code readable.
Errors handled using try-catch.

```js
async function getData() {
  try {
    const res = await fetch("https://api.example.com");
    const data = await res.json();
    console.log(data);
  } catch (error) {
    console.log(error);
  }
}
```

---

## 2️⃣0️⃣ DOM

DOM represents HTML as a tree structure.

```js
document.querySelector("h1").innerText = "Hello DOM";
```

---

## 2️⃣1️⃣ Event Listener

Handles user events like click.

```js
document.getElementById("btn")
  .addEventListener("click", () => {
    alert("Button clicked");
  });
```

---

## 2️⃣2️⃣ Closure

Inner function remembers outer variables.

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}
```

---

## 2️⃣3️⃣ IIFE

Immediately Invoked Function Expression.

```js
(() => {
  console.log("IIFE executed");
})();
```

---

## 2️⃣4️⃣ Bundlers

Bundlers combine multiple JS files into one optimized file.
Examples: Webpack, Vite, Parcel.

---

## ✅ Interview Quick Notes

* `===` is better than `==`
* Arrow function has no own `this`
* Closure = function + lexical scope
* Async/Await = cleaner Promises
* Map allows any type of keys

