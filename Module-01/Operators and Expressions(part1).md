# Module 1 - JavaScript Fundamentals

# Chapter 3 - Operators and Expressions (Part 1)

> **Level:** Beginner
>
> **Prerequisite:** Chapter 2 - Variables and Data Types

---

# Learning Objectives

After completing this chapter, you will be able to:

- Understand what operators are
- Perform mathematical calculations
- Use assignment operators
- Understand unary operators
- Write cleaner JavaScript expressions
- Avoid common beginner mistakes

---

# What is an Operator?

An **operator** is a symbol that tells JavaScript to perform an operation.

Example:

```javascript
5 + 3
```

Here,

```
+
```

is an operator.

It tells JavaScript to **add** two values.

---

# What is an Operand?

The values on which an operator works are called **operands**.

Example:

```javascript
5 + 3
```

```
5

↓

Operand

+

↓

Operator

3

↓

Operand
```

---

# Types of Operators

JavaScript has many kinds of operators.

```
Operators

│

├── Arithmetic

├── Assignment

├── Comparison

├── Logical

├── Unary

├── Bitwise

├── Ternary

└── Others
```

In this chapter we'll begin with the most common ones.

---

# Arithmetic Operators

Arithmetic operators perform mathematical calculations.

| Operator | Meaning |
|----------|---------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Modulus |
| ** | Exponentiation |

---

# Addition (+)

```javascript
let a = 10;
let b = 5;

console.log(a + b);
```

Output

```
15
```

---

# Subtraction (-)

```javascript
let a = 20;
let b = 8;

console.log(a - b);
```

Output

```
12
```

---

# Multiplication (*)

```javascript
let a = 6;
let b = 7;

console.log(a * b);
```

Output

```
42
```

---

# Division (/)

```javascript
let a = 20;
let b = 5;

console.log(a / b);
```

Output

```
4
```

---

# Modulus (%)

Many beginners misunderstand this operator.

The modulus operator returns the **remainder** after division.

Example

```javascript
10 % 3
```

```
10 ÷ 3

↓

Quotient = 3

↓

Remainder = 1
```

Output

```
1
```

---

Example

```javascript
15 % 4
```

Output

```
3
```

---

## Why is Modulus Useful?

Finding even numbers

```javascript
if(number % 2 === 0)
```

Finding odd numbers

```javascript
if(number % 2 !== 0)
```

Checking whether a value is divisible by another number

Creating cyclic patterns

Round-robin scheduling

---

# Exponentiation (**)

Raises one number to the power of another.

```javascript
console.log(2 ** 3);
```

Output

```
8
```

Because

```
2 × 2 × 2
```

---

Another example

```javascript
console.log(5 ** 2);
```

Output

```
25
```

---

# Operator Precedence

Consider:

```javascript
10 + 5 * 2
```

Does JavaScript calculate

```
(10 + 5) × 2
```

or

```
10 + (5 × 2)
```

It follows mathematical precedence.

Multiplication happens first.

```
10 + 10

↓

20
```

---

Example

```javascript
console.log(10 + 5 * 2);
```

Output

```
20
```

---

Use parentheses when needed.

```javascript
console.log((10 + 5) * 2);
```

Output

```
30
```

---

# Expressions

An **expression** is anything that produces a value.

Examples

```javascript
10 + 5
```

```javascript
age > 18
```

```javascript
true && false
```

Every expression evaluates to a result.

---

# Assignment Operator (=)

The assignment operator stores a value inside a variable.

```javascript
let age = 20;
```

```
20

↓

Stored inside

↓

age
```

---

# Compound Assignment Operators

Instead of writing

```javascript
age = age + 1;
```

You can write

```javascript
age += 1;
```

Much cleaner.

---

## +=

```javascript
let score = 50;

score += 20;

console.log(score);
```

Output

```
70
```

---

## -=

```javascript
let money = 1000;

money -= 300;

console.log(money);
```

Output

```
700
```

---

## *=

```javascript
let number = 10;

number *= 3;

console.log(number);
```

Output

```
30
```

---

## /=

```javascript
let value = 20;

value /= 4;

console.log(value);
```

Output

```
5
```

---

## %=

```javascript
let x = 10;

x %= 3;

console.log(x);
```

Output

```
1
```

---

# Unary Operators

A unary operator works with **one operand**.

Example

```
++
```

```
--
```

---

# Increment (++)

Adds one.

```javascript
let count = 5;

count++;

console.log(count);
```

Output

```
6
```

---

# Decrement (--)

Subtracts one.

```javascript
let count = 5;

count--;

console.log(count);
```

Output

```
4
```

---

# Prefix Increment

```javascript
let x = 5;

console.log(++x);
```

Output

```
6
```

Increment happens first.

---

# Postfix Increment

```javascript
let x = 5;

console.log(x++);
```

Output

```
5
```

Then

```
x becomes 6
```

---

Memory visualization

```
Before

x = 5

↓

Print 5

↓

Increase

↓

x = 6
```

---

# Prefix vs Postfix

```javascript
let x = 5;

console.log(++x);
```

```
Increase

↓

Print

↓

6
```

---

```javascript
let x = 5;

console.log(x++);
```

```
Print

↓

Increase

↓

5
```

---

# Should You Use ++?

Yes, but don't overuse it in complex expressions.

Prefer:

```javascript
count++;
```

Avoid writing confusing expressions like:

```javascript
x = ++a + b--;
```

Simple code is easier to read and maintain.

---

# Common Beginner Mistakes

### Mistake 1

```javascript
10 / 0
```

This results in:

```
Infinity
```

Not an error.

---

### Mistake 2

Confusing `%` with percentage.

```
%

↓

Remainder

NOT Percentage
```

---

### Mistake 3

Expecting

```javascript
5 / 2
```

to return

```
2
```

Actual result

```
2.5
```

JavaScript performs floating-point division by default.

---

### Mistake 4

Misunderstanding postfix increment.

```javascript
let x = 5;

console.log(x++);
```

Output

```
5
```

Many beginners expect `6`.

---

# Best Practices

✔ Use parentheses for clarity.

✔ Use meaningful variable names.

✔ Keep expressions simple.

✔ Prefer compound assignment when appropriate.

✔ Avoid writing overly complex one-line expressions.

---

# Mini Exercise

Create a file:

```
calculator.js
```

Store two numbers.

Print:

- Sum
- Difference
- Product
- Quotient
- Remainder
- Square of the first number

---

# Practice Questions

1. What is an operator?
2. What is an operand?
3. What is an expression?
4. Explain the modulus operator.
5. What does `**` do?
6. Difference between `=` and `+=`?
7. Explain prefix increment.
8. Explain postfix increment.
9. Why should expressions be kept simple?
10. What is operator precedence?

---

# Chapter Progress

✅ Completed

- Operators
- Operands
- Expressions
- Arithmetic Operators
- Assignment Operators
- Unary Operators
- Operator Precedence

---

# Coming Next

In **Part 2**, you'll learn:

- Comparison Operators
- `==` vs `===`
- `!=` vs `!==`
- Logical Operators
- Short-Circuit Evaluation
- Operator Precedence with Comparisons
- Real-world examples
- DevSecOps use cases
