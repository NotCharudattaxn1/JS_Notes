# Module 1 – JavaScript Fundamentals

# Chapter 5 – Loops

> **Level:** Beginner (Programming Experience Assumed)
>
> **Prerequisites**
>
> - Variables & Data Types
> - Operators
> - Conditional Statements

---

# Learning Objectives

After completing this chapter, you will be able to:

- Use all JavaScript loop constructs
- Choose the appropriate loop for a given problem
- Understand `break` and `continue`
- Understand `for...of` and `for...in`
- Avoid common loop mistakes
- Write efficient iteration code
- Apply loops in automation scripts

---

# Python/C++ → JavaScript Migration

| Task | Python | C++ | JavaScript |
|------|---------|------|------------|
| Standard loop | `for i in range()` | `for()` | `for()` |
| While loop | `while` | `while` | `while` |
| Do while | — | `do...while` | `do...while` |
| Iterate values | `for x in list` | Range-based `for` | `for...of` |
| Iterate keys | `dict.keys()` | Iterator | `for...in` |

---

# Choosing the Right Loop

| Situation | Loop |
|-----------|------|
| Known number of iterations | `for` |
| Unknown number of iterations | `while` |
| Execute at least once | `do...while` |
| Iterate array values | `for...of` |
| Iterate object properties | `for...in` |

---

# The `for` Loop

The standard counting loop.

Syntax

```javascript
for (initialization; condition; update) {

    // code

}
```

Example

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

Output

```
1
2
3
4
5
```

---

# Execution Flow

```
Initialization

↓

Condition

↓

Body

↓

Update

↓

Condition

↓

...
```

---

# Example – Sum of Numbers

```javascript
let sum = 0;

for (let i = 1; i <= 10; i++) {
    sum += i;
}

console.log(sum);
```

Output

```
55
```

---

# The `while` Loop

Use when the number of iterations isn't known beforehand.

```javascript
let count = 1;

while (count <= 5) {
    console.log(count);
    count++;
}
```

Output

```
1
2
3
4
5
```

---

# Infinite Loop

```javascript
while (true) {

}
```

Useful only when there's an explicit exit condition.

Example

```javascript
while (true) {

    if (shutdownRequested) {
        break;
    }

}
```

---

# The `do...while` Loop

Executes the body **before** checking the condition.

```javascript
let count = 1;

do {

    console.log(count);

    count++;

} while (count <= 5);
```

Output

```
1
2
3
4
5
```

---

Even if the condition is false initially:

```javascript
let count = 10;

do {

    console.log(count);

} while (count < 5);
```

Output

```
10
```

The body runs once.

---

# `break`

Immediately exits the loop.

```javascript
for (let i = 1; i <= 10; i++) {

    if (i === 6) {
        break;
    }

    console.log(i);

}
```

Output

```
1
2
3
4
5
```

---

# `continue`

Skips the current iteration.

```javascript
for (let i = 1; i <= 5; i++) {

    if (i === 3) {
        continue;
    }

    console.log(i);

}
```

Output

```
1
2
4
5
```

---

# `for...of`

One of the most commonly used loops in modern JavaScript.

Iterates over **values**.

```javascript
const languages = [

    "Python",
    "C++",
    "JavaScript"

];

for (const language of languages) {

    console.log(language);

}
```

Output

```
Python
C++
JavaScript
```

---

Equivalent Python

```python
for language in languages:
    print(language)
```

If you're coming from Python, `for...of` will feel very natural.

---

# `for...in`

Iterates over **property names (keys)**.

```javascript
const student = {

    name: "Max",
    age: 20,
    city: "Nagpur"

};

for (const key in student) {

    console.log(key);

}
```

Output

```
name
age
city
```

Access values

```javascript
for (const key in student) {

    console.log(student[key]);

}
```

Output

```
Max
20
Nagpur
```

---

# `for...of` vs `for...in`

| `for...of` | `for...in` |
|------------|------------|
| Values | Keys |
| Arrays | Objects |
| Most common for arrays | Most common for objects |

---

# Which Loop Should You Use?

| Situation | Recommendation |
|-----------|----------------|
| Fixed number of iterations | `for` |
| Reading every array element | `for...of` |
| Reading object properties | `for...in` |
| Waiting until a condition changes | `while` |
| Run at least once | `do...while` |

---

# Nested Loops

```javascript
for (let row = 1; row <= 3; row++) {

    for (let column = 1; column <= 3; column++) {

        console.log(row, column);

    }

}
```

Useful for:

- Matrices
- Tables
- Grids
- Pattern printing

---

# Time Complexity

| Loop | Complexity |
|------|------------|
| Single loop | O(n) |
| Nested loop | O(n²) |
| Triple nested loop | O(n³) |

Always think about complexity when processing large datasets.

---

# Common Mistakes

## Forgetting the Update

```javascript
while (count < 10) {

}
```

Infinite loop.

---

## Using `for...in` on Arrays

```javascript
for (const index in array)
```

This gives indexes, not values.

Prefer

```javascript
for (const value of array)
```

---

## Modifying Loop Variables Unexpectedly

Avoid changing the counter inside the loop body unless absolutely necessary.

---

## Deeply Nested Loops

Nested loops are sometimes necessary, but excessive nesting often indicates that the logic can be simplified.

---

# Best Practices

✔ Use `for...of` for arrays.

✔ Use `for...in` for objects.

✔ Use meaningful loop variable names.

✔ Avoid unnecessary nesting.

✔ Keep loop bodies short.

✔ Exit early using `break` when possible.

---

# DevSecOps Connection

Loops are everywhere in automation.

---

## Scanning Multiple Servers

```javascript
for (const server of servers) {

    scan(server);

}
```

---

## Reading Configuration Files

```javascript
for (const key in config) {

    console.log(config[key]);

}
```

---

## Processing Log Entries

```javascript
for (const log of logs) {

    analyze(log);

}
```

---

## Docker Containers

```javascript
for (const container of containers) {

    restart(container);

}
```

---

## Kubernetes Pods

```javascript
for (const pod of pods) {

    checkHealth(pod);

}
```

---

# Mini Project

Create

```
system-report.js
```

Requirements

Store

```javascript
const services = [

    "nginx",
    "docker",
    "redis",
    "postgres"

];
```

Print

```
Checking nginx...

Checking docker...

Checking redis...

Checking postgres...
```

After the loop

```
Health Check Complete
```

Bonus

Stop the loop immediately if the service name is `"redis"` using `break`.

---

# Practice Questions

1. Difference between `for` and `while`?
2. When should you use `do...while`?
3. Difference between `break` and `continue`?
4. Difference between `for...of` and `for...in`?
5. Which loop is preferred for arrays?
6. Which loop is preferred for objects?
7. What causes an infinite loop?
8. Why should nested loops be used carefully?
9. Give one DevSecOps use case for loops.
10. What is the time complexity of a single loop?

---

# Interview Questions

### Q1

Difference between

```javascript
for...of

and

for...in
```

---

### Q2

Does `break` terminate only the current iteration?

No.

It exits the loop completely.

---

### Q3

Does `continue` stop the loop?

No.

It skips the current iteration and continues with the next one.

---

### Q4

Which loop would you use to iterate over a JSON array?

`for...of`

---

# Key Takeaways

- Use `for` for counting.
- Use `while` when the iteration count is unknown.
- Use `do...while` when the body must execute at least once.
- Use `for...of` for arrays and iterable objects.
- Use `for...in` for object properties.
- Use `break` and `continue` thoughtfully.
- Always consider readability and time complexity.

---

# Summary

You now know:

- `for`
- `while`
- `do...while`
- `break`
- `continue`
- `for...of`
- `for...in`
- Nested loops
- Time complexity
- Best practices
- DevSecOps applications

---

# Next Chapter

## Chapter 6 – Functions

Topics include:

- Function declarations
- Function expressions
- Arrow functions
- Parameters
- Return values
- Default parameters
- Rest parameters
- Scope
- Closures (introduction)
- Higher-order functions (introduction)
- DevSecOps examples
