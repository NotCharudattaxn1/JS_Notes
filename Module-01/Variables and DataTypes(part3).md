# Module 1 - JavaScript Fundamentals

# Chapter 2 - Variables and Data Types (Part 3)

> **Level:** Beginner
>
> **Prerequisite:** Chapter 2 - Part 2

---

# Learning Objectives

By the end of this chapter, you will be able to:

- Understand Type Conversion
- Understand Type Coercion
- Differentiate between implicit and explicit conversion
- Use template literals
- Understand truthy and falsy values
- Avoid common JavaScript mistakes
- Apply these concepts in real-world programs

---

# What is Type Conversion?

Sometimes a value needs to change from one data type to another.

Example:

```
"25"
```

is a String.

```
25
```

is a Number.

JavaScript allows converting one type into another.

This process is called **Type Conversion**.

---

# Why Do We Need Type Conversion?

Imagine a user enters their age.

```
Input

"21"
```

The value is received as a String.

But if we want to calculate:

```
21 + 5
```

we need a Number.

Therefore we convert:

```
String

↓

Number
```

---

# Two Types of Conversion

```
Type Conversion

│

├── Explicit Conversion

│

└── Implicit Conversion (Coercion)
```

---

# Explicit Type Conversion

The programmer manually converts the data type.

Example:

```javascript
let age = "20";

let numberAge = Number(age);

console.log(numberAge);
```

Output

```
20
```

Now check the type.

```javascript
console.log(typeof numberAge);
```

Output

```
number
```

---

# Number()

Converts values into Numbers.

Examples

```javascript
Number("100")
```

Result

```
100
```

---

```javascript
Number("45.7")
```

Result

```
45.7
```

---

```javascript
Number(true)
```

Result

```
1
```

---

```javascript
Number(false)
```

Result

```
0
```

---

```javascript
Number("Hello")
```

Result

```
NaN
```

Because JavaScript cannot convert "Hello" into a number.

---

# String()

Converts values into Strings.

Example

```javascript
let marks = 95;

let text = String(marks);

console.log(text);
```

Output

```
95
```

Check the type.

```javascript
console.log(typeof text);
```

Output

```
string
```

---

# Boolean()

Converts values into Boolean.

Example

```javascript
Boolean(1)
```

Result

```
true
```

---

```javascript
Boolean(0)
```

Result

```
false
```

---

```javascript
Boolean("")
```

Result

```
false
```

---

```javascript
Boolean("Hello")
```

Result

```
true
```

---

# Type Coercion

Sometimes JavaScript converts values automatically.

This automatic conversion is called **Type Coercion**.

Example

```javascript
console.log("5" + 5);
```

Output

```
55
```

JavaScript converts:

```
5

↓

"5"
```

Then joins them.

---

Another example

```javascript
console.log("10" - 2);
```

Output

```
8
```

Why?

Because subtraction requires numbers.

JavaScript converts:

```
"10"

↓

10
```

---

# Examples of Type Coercion

### Example 1

```javascript
console.log(5 + "5");
```

Output

```
55
```

---

### Example 2

```javascript
console.log("5" * 2);
```

Output

```
10
```

---

### Example 3

```javascript
console.log("20" / 4);
```

Output

```
5
```

---

### Example 4

```javascript
console.log(true + 1);
```

Output

```
2
```

Because:

```
true

↓

1
```

---

### Example 5

```javascript
console.log(false + 5);
```

Output

```
5
```

Because:

```
false

↓

0
```

---

# Why Is Type Coercion Dangerous?

Look carefully.

```javascript
console.log("10" + 5);
```

Output

```
105
```

Now

```javascript
console.log("10" - 5);
```

Output

```
5
```

Notice:

```
+

↓

String Concatenation

-

↓

Numeric Subtraction
```

This behavior surprises many beginners.

---

# Best Practice

Avoid relying on automatic conversion.

Instead:

```javascript
const age = Number(userInput);
```

Explicit conversion makes your code predictable.

---

# Truthy and Falsy Values

Every value in JavaScript behaves like either:

```
true

or

false
```

when used inside conditions.

---

# Falsy Values

JavaScript has only a few falsy values.

```
false

0

-0

0n

""

null

undefined

NaN
```

Everything else is **truthy**.

---

# Example

```javascript
if ("Hello") {

    console.log("Runs");

}
```

Output

```
Runs
```

Because:

```
"Hello"

↓

Truthy
```

---

Example

```javascript
if ("") {

    console.log("Hello");

}
```

Output

Nothing.

Empty strings are falsy.

---

Example

```javascript
if (100) {

    console.log("Valid");

}
```

Output

```
Valid
```

---

Example

```javascript
if (0) {

    console.log("Hello");

}
```

Output

Nothing.

---

# Why Truthy/Falsy Matters

Suppose:

```javascript
let token = "";
```

Instead of writing:

```javascript
if(token !== "")
```

you can simply write:

```javascript
if(token){

}
```

Cleaner and easier to read.

---

# Template Literals

Old style:

```javascript
let name = "Max";

console.log("Hello " + name);
```

Modern JavaScript uses Template Literals.

Syntax:

```javascript
``
```

Example

```javascript
let name = "Max";

console.log(`Hello ${name}`);
```

Output

```
Hello Max
```

---

Multiple variables

```javascript
let city = "Nagpur";

let age = 20;

console.log(`${city} ${age}`);
```

Output

```
Nagpur 20
```

---

# Multi-line Strings

Without template literals:

```javascript
console.log("Hello
World");
```

Error.

Using backticks:

```javascript
console.log(`Hello

World`);
```

Output

```
Hello

World
```

---

# Common Beginner Mistakes

### Mistake 1

```javascript
"5" + 5
```

Expecting:

```
10
```

Actual:

```
55
```

---

### Mistake 2

```javascript
Number("Hello")
```

Result

```
NaN
```

---

### Mistake 3

Thinking

```javascript
null

===

undefined
```

They are different values.

---

### Mistake 4

Using

```javascript
==

instead of

===
```

We'll learn comparisons in the next chapter, but professional JavaScript code generally prefers `===` because it avoids unexpected type coercion.

---

# Mini Project

Create:

```
student.js
```

Store:

- Name
- Age
- College
- CGPA
- Is Hosteller

Print the output using template literals.

Example:

```
Name : Max

Age : 20

College : PCCOE

CGPA : 9.4

Hosteller : false
```

---

# DevSecOps Connection

As a DevSecOps engineer, you will often receive data from:

- REST APIs
- JSON files
- Environment variables
- Configuration files
- Command-line arguments

Most of this data arrives as **strings**.

Example:

```javascript
process.env.PORT
```

Although it represents a port number, its type is **string**.

A common practice is to convert it explicitly:

```javascript
const port = Number(process.env.PORT);
```

This avoids subtle bugs caused by unexpected data types.

---

# Interview Questions

### Q1. What is Type Conversion?

Changing a value from one data type to another.

---

### Q2. What is Type Coercion?

Automatic type conversion performed by JavaScript.

---

### Q3. Difference between Type Conversion and Type Coercion?

| Type Conversion | Type Coercion |
|-----------------|---------------|
| Manual | Automatic |
| Programmer controls it | JavaScript controls it |

---

### Q4. What are Truthy values?

Values that evaluate to `true` in a Boolean context.

---

### Q5. Name all Falsy values.

- false
- 0
- -0
- 0n
- ""
- null
- undefined
- NaN

---

### Q6. Why use Template Literals?

They make string formatting cleaner, easier to read, and support embedded expressions and multi-line strings.

---

# Chapter 2 Revision

✔ Variables

✔ let

✔ const

✔ var

✔ Primitive Data Types

✔ typeof

✔ null vs undefined

✔ Type Conversion

✔ Type Coercion

✔ Truthy & Falsy

✔ Template Literals

---

# What You've Learned So Far

You can now:

- Store data in variables
- Choose the appropriate data type
- Convert between types
- Recognize JavaScript's automatic type coercion
- Use template literals for modern string formatting
- Understand truthy and falsy values
- Apply these concepts in small programs

These are foundational skills that you'll use in every JavaScript project.

---

# Next Chapter

## Chapter 3 - Operators and Expressions

Topics include:

- Arithmetic Operators
- Assignment Operators
- Comparison Operators
- Logical Operators
- Unary Operators
- Increment & Decrement
- Operator Precedence
- Equality (`==` vs `===`)
- Practical Exercises
- Mini Calculator Project
