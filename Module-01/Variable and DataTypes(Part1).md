# Module 1 - JavaScript Fundamentals

# Chapter 2 - Variables and Data Types (Part 1)

> **Level:** Beginner
>
> **Prerequisite:** Chapter 1 - Introduction to JavaScript

---

# Learning Objectives

By the end of this chapter, you will be able to:

- Understand what variables are
- Understand how data is stored in memory
- Declare variables using `let`, `const`, and `var`
- Follow JavaScript naming rules
- Write readable and maintainable code
- Understand why modern JavaScript prefers `let` and `const`

---

# What is a Variable?

Imagine you have several boxes.

Each box has a label on it.

Inside each box, you can store something.

Example:

```
+-----------+
|  Name     |
+-----------+
|   Max     |
+-----------+

+-----------+
|  Age      |
+-----------+
|   20      |
+-----------+
```

A **variable** works exactly like these labeled boxes.

A variable stores information that your program can use later.

---

# Why Do We Need Variables?

Suppose we write:

```javascript
console.log("Max");
console.log("Max");
console.log("Max");
```

What happens if the name changes?

We would need to update it everywhere.

Instead:

```javascript
let name = "Max";

console.log(name);
console.log(name);
console.log(name);
```

Now we only change the value once.

---

# Variables in Real Applications

Variables are everywhere.

Example:

```
Username

Password

Email

Temperature

CPU Usage

RAM Usage

Port Number

API Key

File Path

IP Address
```

Without variables, programming would be impossible.

---

# Memory Visualization

When JavaScript runs, it stores variables in memory.

Example:

```javascript
let age = 20;
```

Conceptually, it looks like this:

```
RAM Memory

+-----------------------+
| age  | 20            |
+-----------------------+
```

Another example:

```javascript
let city = "Nagpur";
```

```
RAM Memory

+-----------------------+
| age  | 20            |
+-----------------------+
| city | Nagpur        |
+-----------------------+
```

> **Note:** This is a simplified view to help you understand the concept. JavaScript engines manage memory internally in a much more complex way.

---

# Declaring Variables

JavaScript provides three keywords:

```javascript
let
const
var
```

Modern JavaScript primarily uses:

- `let`
- `const`

`var` exists for historical reasons.

---

# Understanding let

`let` creates a variable whose value can be changed later.

Example:

```javascript
let age = 20;

console.log(age);
```

Output:

```
20
```

Now change it:

```javascript
let age = 20;

age = 21;

console.log(age);
```

Output:

```
21
```

Since the value changed, `let` is called a **mutable variable**.

---

# More Examples

```javascript
let score = 95;

score = 100;

console.log(score);
```

Output

```
100
```

---

```javascript
let city = "Nagpur";

city = "Pune";

console.log(city);
```

Output

```
Pune
```

---

# Rules of let

✔ Can change value

✔ Cannot be declared twice in the same scope

Correct

```javascript
let age = 20;

age = 25;
```

Incorrect

```javascript
let age = 20;

let age = 25;
```

Error:

```
Identifier 'age' has already been declared
```

---

# Understanding const

Sometimes values should never change.

Example:

```
Pi

Company Name

Birth Date

API Version

Application Name
```

For such values, use `const`.

Example:

```javascript
const PI = 3.14159;
```

This value cannot be reassigned.

---

Example

```javascript
const country = "India";

console.log(country);
```

Output

```
India
```

---

Trying to change it:

```javascript
const country = "India";

country = "Germany";
```

Result:

```
TypeError: Assignment to constant variable.
```

---

# Why const is Preferred

Professional developers use `const` by default.

Reason:

If a value should never change, preventing accidental reassignment reduces bugs.

General rule:

```
Can change?

↓

Yes → let

↓

No → const
```

---

# Understanding var

Before ES6 (2015), JavaScript only had `var`.

Example:

```javascript
var age = 20;
```

Today, avoid using it in new code unless maintaining older projects.

---

# Problems with var

### 1. Redeclaration

```javascript
var age = 20;

var age = 50;

console.log(age);
```

Output

```
50
```

No error occurs, which can hide bugs.

---

### 2. Function Scope Instead of Block Scope

```javascript
if (true) {

    var x = 10;

}

console.log(x);
```

Output

```
10
```

Many beginners expect an error because `x` was declared inside the `if` block.

Now compare with `let`:

```javascript
if (true) {

    let y = 10;

}

console.log(y);
```

Output

```
ReferenceError
```

This safer behavior is why `let` is preferred.

---

# let vs const vs var

| Feature | let | const | var |
|----------|-----|--------|-----|
| Can change value | ✔ | ✘ | ✔ |
| Can redeclare | ✘ | ✘ | ✔ |
| Block scope | ✔ | ✔ | ✘ |
| Modern JavaScript | ✔ | ✔ | ✘ |

---

# Which One Should You Use?

Professional recommendation:

```
Start with const

↓

Need to change the value?

↓

Use let

↓

Avoid var
```

This is the approach followed in most modern JavaScript projects.

---

# Variable Naming Rules

Valid:

```javascript
let age;

let userName;

let first_name;

let $price;

let _temp;
```

---

Invalid:

```javascript
let 123age;

let first-name;

let user name;
```

Reasons:

- Cannot start with a number
- Hyphens are treated as subtraction
- Spaces are not allowed in variable names

---

# Reserved Keywords

You cannot use JavaScript keywords as variable names.

Examples:

```javascript
let if = 10;
```

```javascript
let return = 5;
```

```javascript
let function = 20;
```

These produce syntax errors because the words have predefined meanings in JavaScript.

---

# Naming Conventions

### Bad

```javascript
let a;

let b;

let c;
```

---

### Better

```javascript
let studentAge;

let totalMarks;

let serverIP;

let cpuUsage;
```

Good names make your code easier to understand and maintain.

---

# camelCase

JavaScript follows **camelCase** for naming variables and functions.

Examples:

```javascript
let firstName;

let totalPrice;

let currentTemperature;

let apiResponse;

let studentMarks;
```

Notice:

- First word starts with a lowercase letter.
- Each new word starts with a capital letter.

---

# UPPER_CASE Constants

Constants that never change are often written in uppercase.

Example:

```javascript
const MAX_USERS = 100;

const API_VERSION = "v1";

const PI = 3.14159;
```

This convention signals that the value is intended to remain constant.

---

# Best Practices

✔ Use meaningful names.

✔ Prefer `const` whenever possible.

✔ Use `let` only when the value will change.

✔ Avoid `var` in modern JavaScript.

✔ Follow camelCase for variables and functions.

✔ Keep variable names descriptive but concise.

---

# Common Beginner Mistakes

### Mistake 1

```javascript
let age = 20;

let age = 25;
```

❌ Redeclaring a `let` variable in the same scope.

---

### Mistake 2

```javascript
const score = 90;

score = 95;
```

❌ Reassigning a constant.

---

### Mistake 3

```javascript
let first-name = "Max";
```

❌ Using a hyphen in a variable name.

---

### Mistake 4

```javascript
let 123name = "Max";
```

❌ Starting a variable name with a number.

---

# Mini Exercise

Create a file named:

```
variables.js
```

Write a program that stores:

- Your name
- Your age
- Your college
- Your favorite programming language

Print each value using `console.log()`.

---

# Chapter Progress

✅ What you have learned:

- What variables are
- How variables conceptually relate to memory
- `let`
- `const`
- `var`
- Naming rules
- Naming conventions
- Best practices

---

# Coming Next (Part 2)

In the next part, you'll learn:

- Primitive Data Types
- Number
- String
- Boolean
- Undefined
- Null
- BigInt
- Symbol (Introduction)
- typeof Operator
- Memory Representation
- Hands-on Exercises
