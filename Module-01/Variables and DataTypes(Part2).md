# Module 1 - JavaScript Fundamentals

# Chapter 2 - Variables and Data Types (Part 2)

> **Level:** Beginner
>
> **Prerequisite:** Chapter 2 - Part 1

---

# Learning Objectives

After completing this chapter, you will be able to:

- Understand JavaScript's primitive data types
- Identify the type of any value
- Use the `typeof` operator
- Understand `null` vs `undefined`
- Learn about BigInt and Symbol
- Visualize how values are stored
- Write programs using different data types

---

# What is a Data Type?

A variable stores **data**.

But data can have different forms.

For example:

```
21
```

is a number.

```
"Max"
```

is text.

```
true
```

is a Boolean value.

JavaScript needs to know **what kind of data** it is working with.

This category is called a **Data Type**.

---

# Why Do Data Types Matter?

Imagine asking JavaScript to perform:

```javascript
20 + 30
```

Result

```
50
```

Now try:

```javascript
"20" + "30"
```

Result

```
2030
```

Why?

Because these are **strings**, not numbers.

Understanding data types helps prevent unexpected results.

---

# JavaScript Data Types

JavaScript has two broad categories.

```
Data Types
│
├── Primitive
│
└── Non-Primitive (Objects)
```

In this chapter we focus only on **Primitive Data Types**.

---

# Primitive Data Types

JavaScript has **7 primitive data types**.

```
Primitive Data Types

1. Number

2. String

3. Boolean

4. Undefined

5. Null

6. BigInt

7. Symbol
```

These are the fundamental building blocks of JavaScript.

---

# 1. Number

The **Number** type represents both integers and decimal values.

Examples:

```javascript
let age = 20;

let marks = 98;

let temperature = 36.7;

let price = 499.99;
```

---

## Memory Representation

```javascript
let age = 20;
```

Conceptually:

```
Memory

+-------------------+
| age | 20          |
+-------------------+
```

---

## Mathematical Operations

```javascript
let a = 10;

let b = 5;

console.log(a + b);

console.log(a - b);

console.log(a * b);

console.log(a / b);

console.log(a % b);
```

Output

```
15

5

50

2

0
```

---

## Special Number Values

JavaScript also supports:

```
Infinity

-Infinity

NaN
```

Example

```javascript
console.log(10 / 0);
```

Output

```
Infinity
```

---

Example

```javascript
console.log("Hello" * 5);
```

Output

```
NaN
```

**NaN** means **Not a Number**.

It indicates an invalid mathematical operation.

---

# 2. String

A **String** is a sequence of characters.

Examples:

```javascript
let name = "Max";

let city = "Nagpur";

let course = "JavaScript";
```

---

Strings can use:

```javascript
"Double Quotes"

'Single Quotes'

`Backticks`
```

All three are valid, but backticks have additional features that we'll learn later.

---

## String Memory

```javascript
let city = "Nagpur";
```

Conceptually:

```
Memory

+--------------------+
| city | Nagpur      |
+--------------------+
```

---

## Printing Strings

```javascript
let language = "JavaScript";

console.log(language);
```

Output

```
JavaScript
```

---

# 3. Boolean

A Boolean has only two possible values.

```
true

false
```

Examples:

```javascript
let isAdmin = true;

let isLoggedIn = false;
```

---

## Real World Examples

```
Door Open?

True

False
```

```
User Logged In?

True

False
```

```
Payment Successful?

True

False
```

Booleans are heavily used in conditions.

---

# 4. Undefined

Suppose we declare a variable but don't assign any value.

```javascript
let username;
```

Now print it.

```javascript
console.log(username);
```

Output

```
undefined
```

---

### Why?

JavaScript says:

> "You created the variable, but you never gave it a value."

So the variable contains:

```
undefined
```

---

Memory visualization:

```
Memory

+-----------------------+
| username | undefined  |
+-----------------------+
```

---

# 5. Null

`null` is different.

It represents an **intentional empty value**.

Example

```javascript
let apiToken = null;
```

Meaning:

> "Currently there is no API token."

Unlike `undefined`, we **deliberately** assign `null`.

---

Example

```javascript
let currentUser = null;
```

Later

```javascript
currentUser = "Max";
```

---

# null vs undefined

This is a favorite interview question.

| undefined | null |
|------------|------|
| Value not assigned | Empty value assigned intentionally |
| Default by JavaScript | Assigned by programmer |

Example

```javascript
let x;

console.log(x);
```

Output

```
undefined
```

---

```javascript
let x = null;

console.log(x);
```

Output

```
null
```

Remember:

- **undefined** → JavaScript's decision.
- **null** → Programmer's decision.

---

# 6. BigInt

JavaScript Numbers have limits.

Very large integers can lose precision.

Example:

```javascript
let number = 9007199254740991;
```

For larger integers, use **BigInt**.

```javascript
let huge = 9007199254740991n;
```

Notice the **`n`** at the end.

---

Example

```javascript
const stars = 999999999999999999999999999999999n;
```

BigInt is useful when dealing with extremely large whole numbers, though you won't use it often in everyday JavaScript.

---

# 7. Symbol (Introduction)

A **Symbol** creates a unique identifier.

Example:

```javascript
const id = Symbol();
```

Even if two symbols look similar, they are always unique.

```javascript
const id1 = Symbol();

const id2 = Symbol();

console.log(id1 === id2);
```

Output

```
false
```

Symbols are mostly used in advanced JavaScript and libraries. We'll revisit them later.

---

# The typeof Operator

Sometimes you want to know what type of value a variable contains.

JavaScript provides the `typeof` operator.

Syntax:

```javascript
typeof value
```

---

## Examples

### Number

```javascript
let age = 20;

console.log(typeof age);
```

Output

```
number
```

---

### String

```javascript
let city = "Nagpur";

console.log(typeof city);
```

Output

```
string
```

---

### Boolean

```javascript
let loggedIn = true;

console.log(typeof loggedIn);
```

Output

```
boolean
```

---

### Undefined

```javascript
let username;

console.log(typeof username);
```

Output

```
undefined
```

---

### BigInt

```javascript
let large = 100n;

console.log(typeof large);
```

Output

```
bigint
```

---

### Symbol

```javascript
const id = Symbol();

console.log(typeof id);
```

Output

```
symbol
```

---

# Strange Behavior of typeof

Look at this:

```javascript
console.log(typeof null);
```

Output

```
object
```

Wait…

Isn't `null` a primitive?

Yes.

This is a **historical bug** in JavaScript that has been preserved for backward compatibility.

**Remember for interviews:**

- `null` is a primitive data type.
- `typeof null` returns `"object"`.

This is not a mistake in your code—it is a long-standing behavior of the language.

---

# Summary Table

| Value | Data Type | Example |
|-------|-----------|---------|
| `25` | Number | `let age = 25;` |
| `"Max"` | String | `let name = "Max";` |
| `true` | Boolean | `let isAdmin = true;` |
| `undefined` | Undefined | `let x;` |
| `null` | Null | `let user = null;` |
| `100n` | BigInt | `let big = 100n;` |
| `Symbol()` | Symbol | `const id = Symbol();` |

---

# Mini Exercise

Create a file named:

```
datatypes.js
```

Store the following values:

- Your name
- Your age
- Whether you like JavaScript
- A variable without a value
- A variable with `null`

Print each variable and its type using `console.log()` and `typeof`.

---

# Practice Questions

1. What is a data type?
2. How many primitive data types does JavaScript have?
3. What is the difference between a Number and a String?
4. What does `undefined` mean?
5. What is `null` used for?
6. When would you use `BigInt`?
7. Why are Symbols unique?
8. What does `typeof` do?
9. Why does `typeof null` return `"object"`?
10. Which primitive types have you used most so far?

---

# Chapter Progress

✅ You now understand:

- Primitive data types
- Numbers
- Strings
- Booleans
- Undefined
- Null
- BigInt
- Symbol
- `typeof`
- The `typeof null` interview trap

---

# Coming Next (Part 3)

In the final part of Chapter 2, you'll learn:

- Type Conversion
- Type Coercion
- Truthy and Falsy Values
- Template Literals
- Common Pitfalls
- Mini Project
- Interview Questions
- DevSecOps Best Practices
- Chapter Revision Sheet
