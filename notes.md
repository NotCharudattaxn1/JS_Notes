# JavaScript Fundamentals
> Version: 1.0
> Suitable for: Technical Interviews, Web Development

---

# Table of Contents

1. Introduction to JavaScript
2. Features of JavaScript
3. How JavaScript Works
4. Variables
5. Data Types
6. Operators
7. Type Conversion
8. Conditional Statements
9. Loops
10. Functions
11. Scope
12. Hoisting
13. Arrays
14. Objects
15. Strings
16. DOM (Document Object Model)
17. Events
18. ES6 Features
19. Asynchronous JavaScript
20. Common Interview Questions
21. Quick Revision

---

# 1. Introduction

## What is JavaScript?

JavaScript (JS) is a high-level, interpreted programming language used to make web pages interactive.

Without JavaScript, websites would only display static content.

JavaScript allows developers to create:

- Dynamic websites
- Interactive forms
- Animations
- Games
- Real-time updates
- API communication

---

## Why JavaScript?

JavaScript is one of the three core technologies of web development.

| Technology | Purpose |
|------------|---------|
| HTML | Structure |
| CSS | Styling |
| JavaScript | Functionality & Interactivity |

Example:

HTML creates a button.

CSS styles the button.

JavaScript makes the button respond to clicks.

---

# 2. Features of JavaScript

- Lightweight
- Interpreted language
- Object-Oriented
- Event-driven
- Cross-platform
- Supports asynchronous programming
- Runs in all modern browsers

---

# 3. How JavaScript Works

When a user visits a webpage:

1. Browser downloads HTML.
2. Browser parses HTML.
3. CSS is applied.
4. JavaScript engine executes JavaScript.
5. JavaScript can modify the webpage dynamically.

Popular JavaScript Engines:

- Chrome → V8
- Firefox → SpiderMonkey
- Safari → JavaScriptCore

---

# 4. Variables

Variables store data.

Syntax:

```javascript
let age = 20;
const PI = 3.14;
var name = "Alice";
```

---

## var

Old way of declaring variables.

Problems:

- Function scoped
- Can be redeclared
- Can cause bugs

Example:

```javascript
var x = 10;
var x = 20;
```

Allowed.

---

## let

Modern variable declaration.

Features:

- Block scoped
- Cannot be redeclared in same scope
- Value can change

```javascript
let marks = 95;
marks = 100;
```

---

## const

Constant variable.

Cannot be reassigned.

```javascript
const country = "India";
```

---

# 5. Data Types

## Primitive Types

- Number
- String
- Boolean
- Null
- Undefined
- BigInt
- Symbol

Example:

```javascript
let age = 20;
let name = "Rahul";
let isStudent = true;
```

---

## Non-Primitive Types

- Object
- Array
- Function

Example:

```javascript
const student = {
    name: "Rahul",
    age: 20
};
```

---

# 6. Operators

## Arithmetic

```javascript
+
-
*
/
%
**
```

---

## Comparison

```javascript
==
===
!=
!==
>
<
>=
<=
```

Important:

### ==

Compares values only.

```javascript
5 == "5"
```

Returns:

```
true
```

---

### ===

Compares value AND data type.

```javascript
5 === "5"
```

Returns:

```
false
```

Always prefer `===`.

---

## Logical Operators

```javascript
&&
||
!
```

---

# 7. Type Conversion

Implicit Conversion

JavaScript automatically converts types.

Example:

```javascript
"5" + 2
```

Output:

```
52
```

---

Explicit Conversion

```javascript
Number("5")

String(10)

Boolean(1)
```

---

# 8. Conditional Statements

## if

```javascript
if(age >= 18){
    console.log("Adult");
}
```

---

## if-else

```javascript
if(age >=18){
    console.log("Adult");
}
else{
    console.log("Minor");
}
```

---

## switch

```javascript
switch(day){
case 1:
console.log("Monday");
break;

default:
console.log("Invalid");
}
```

---

# 9. Loops

## for

```javascript
for(let i=0;i<5;i++){
console.log(i);
}
```

---

## while

```javascript
let i=0;

while(i<5){
i++;
}
```

---

## do while

Runs at least once.

---

# 10. Functions

Functions are reusable blocks of code.

Example

```javascript
function add(a,b){
return a+b;
}
```

---

## Arrow Function

```javascript
const add=(a,b)=>{
return a+b;
}
```

Short Version

```javascript
const add=(a,b)=>a+b;
```

---

# 11. Scope

Scope determines where a variable can be accessed.

## Global Scope

Accessible everywhere.

## Function Scope

Accessible only inside function.

## Block Scope

Created using

```
let

const
```

inside

```
{}

```

---

# 12. Hoisting

JavaScript moves declarations to the top before execution.

Example:

```javascript
console.log(a);

var a=10;
```

Output:

```
undefined
```

With

```
let

const
```

Accessing before declaration causes a ReferenceError.

---

# 13. Arrays

Collection of values.

```javascript
let numbers=[10,20,30];
```

Access

```javascript
numbers[0]
```

Useful Methods

```javascript
push()

pop()

shift()

unshift()

slice()

splice()

map()

filter()

find()

includes()
```

---

# 14. Objects

Store key-value pairs.

```javascript
const student={

name:"Rahul",

age:20

};
```

Access

```javascript
student.name

student["name"]
```

---

# 15. Strings

Common Methods

```javascript
length

toUpperCase()

toLowerCase()

trim()

includes()

slice()

replace()

split()
```

---

# 16. DOM

DOM stands for

Document Object Model.

It represents the HTML page as a tree structure.

JavaScript uses the DOM to:

- Change content
- Change styles
- Add elements
- Remove elements

Selecting Elements

```javascript
document.getElementById()

document.querySelector()

document.querySelectorAll()
```

Example

```javascript
document.getElementById("title").innerHTML="Welcome";
```

---

# 17. Events

Events are user interactions.

Examples:

- Click
- Mouseover
- Keypress
- Submit

Example

```javascript
button.addEventListener("click",function(){

alert("Hello");

});
```

---

# 18. ES6 Features

### let

### const

### Arrow Functions

### Template Literals

```javascript
`Hello ${name}`
```

### Destructuring

```javascript
const {name,age}=student;
```

### Spread Operator

```javascript
const newArray=[...oldArray];
```

### Rest Operator

```javascript
function sum(...numbers){}
```

---

# 19. Asynchronous JavaScript

JavaScript executes code one line at a time.

Some operations take time.

Example:

Fetching data from server.

JavaScript does not stop.

It continues executing.

Concepts:

### Callback

Function passed as argument.

### Promise

Represents future completion.

States:

Pending

Fulfilled

Rejected

### async/await

Cleaner syntax for promises.

Example

```javascript
async function getData(){

const response=await fetch(url);

}
```

---

# 20. Common Interview Questions

Q. Difference between let, const and var?

Q. Difference between == and ===?

Q. What is DOM?

Q. What is an Event?

Q. What is Hoisting?

Q. What is Closure?

Q. Difference between null and undefined?

Q. What is Event Bubbling?

Q. What is a Promise?

Q. What is async/await?

Q. Difference between map() and forEach()?

Q. Difference between slice() and splice()?

---

# 21. Quick Revision

✓ JavaScript makes websites interactive.

✓ HTML → Structure

✓ CSS → Styling

✓ JavaScript → Functionality

✓ Prefer `let` and `const`.

✓ Use `===` instead of `==`.

✓ Arrays store ordered values.

✓ Objects store key-value pairs.

✓ DOM represents HTML.

✓ Events respond to user actions.

✓ ES6 introduced arrow functions, template literals, destructuring, and spread operator.

✓ Asynchronous JavaScript uses callbacks, promises, and async/await.

---

# Interview Tips

1. Explain concepts with examples.
2. Write clean code.
3. Prefer modern JavaScript (ES6+).
4. Use `const` by default, `let` when reassignment is needed.
5. Understand the DOM and events—they are common interview topics.
6. Be able to explain **why** you choose a particular feature, not just **what** it does.
