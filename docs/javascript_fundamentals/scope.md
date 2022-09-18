# Scope

Variable is the fundamental part in programming. We declare variable to store different data types. To declare a variable we use the key word _var_, _let_ and _const_. A variable can declared at different scope. In this section we will see the scope, scope of variables when we use var or let.
Variables scopes can be:

- Window
- Global
- Local

Variable can be declared globally or locally or window scope. We will see both global and local scope.
Anything declared without let, var or const is scoped at window level.

Let us image we have a scope.js file.

## Window Scope

Without using console.log() open your browser and check, you will see the value of a and b if you write a or b on the browser. That means a and b are already available in the window.

```js
//scope.js
a = "JavaScript"; // is a window scope this found anywhere
b = 10; // this is a window scope variable
function letsLearnScope() {
  console.log(a, b);
  if (true) {
    console.log(a, b);
  }
}
console.log(a, b); // accessible
```

## Global scope

A globally declared variable can be accessed every where in the same file. But the term global is relative. It can be global to the file or it can be global relative to some block of codes.

```js
//scope.js
let a = "JavaScript"; // is a global scope it will be found anywhere in this file
let b = 10; // is a global scope it will be found anywhere in this file
function letsLearnScope() {
  console.log(a, b); // JavaScript 10, accessible
  if (true) {
    let a = "Python";
    let b = 100;
    console.log(a, b); // Python 100
  }
  console.log(a, b);
}
letsLearnScope();
console.log(a, b); // JavaScript 10, accessible
```

## Local scope

A variable declared as local can be accessed only in certain block code.

```js
//scope.js
let a = "JavaScript"; // is a global scope it will be found anywhere in this file
let b = 10; // is a global scope it will be found anywhere in this file
function letsLearnScope() {
  console.log(a, b); // JavaScript 10, accessible
  let c = 30;
  if (true) {
    // we can access from the function and outside the function but
    // variables declared inside the if will not be accessed outside the if block
    let a = "Python";
    let b = 20;
    let d = 40;
    console.log(a, b, c); // Python 20 30
  }
  // we can not access c because c's scope is only the if block
  console.log(a, b); // JavaScript 10
}
letsLearnScope();
console.log(a, b); // JavaScript 10, accessible
```

Now, you have an understanding of scope. A variable declared with _var_ only scoped to function but variable declared with _let_ or _const_ is block scope(function block, if block, loop etc). Block in JavaScript is a code in between two curly brackets ({}).

```js
//scope.js
function letsLearnScope() {
  var gravity = 9.81;
  console.log(gravity);
}
// console.log(gravity), Uncaught ReferenceError: gravity is not defined

if (true) {
  var gravity = 9.81;
  console.log(gravity); // 9.81
}
console.log(gravity); // 9.81

for (var i = 0; i < 3; i++) {
  console.log(i); // 1, 2, 3
}
console.log(i);
```

In ES6 and above there is _let_ and _const_, so you will not suffer from the sneakiness of _var_. When we use _let_ our variable is block scoped and it will not infect other parts of our code.

```js
//scope.js
function letsLearnScope() {
  // you can use let or const, but gravity is constant I prefer to use const
  const gravity = 9.81;
  console.log(gravity);
}
// console.log(gravity), Uncaught ReferenceError: gravity is not defined

if (true) {
  const gravity = 9.81;
  console.log(gravity); // 9.81
}
// console.log(gravity), Uncaught ReferenceError: gravity is not defined

for (let i = 0; i < 3; i++) {
  console.log(i); // 1, 2, 3
}
// console.log(i), Uncaught ReferenceError: gravity is not defined
```

The scope _let_ and _const_ is the same. The difference is only reassigning. We can not change or reassign the value of const variable. I would strongly suggest you to use _let_ and _const_, by using _let_ and _const_ you will writ clean code and avoid hard to debug mistakes. As a rule of thumb, you can use _let_ for any value which change, _const_ for any constant value, and for array, object, arrow function and function expression.
