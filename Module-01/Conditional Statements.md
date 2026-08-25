# Module 1 – JavaScript Fundamentals

# Chapter 4 – Conditional Statements

> **Level:** Beginner (Programming Experience Assumed)
>
> **Prerequisites**
>
> - Python Basics
> - C++ Basics
> - Variables & Data Types
> - Operators & Expressions

---

# Learning Objectives

After completing this chapter, you will be able to:

- Use `if`, `else`, and `else if`
- Write nested conditional statements
- Use `switch` effectively
- Decide when to use `if` vs `switch`
- Write clean conditional logic
- Apply conditional statements in real-world automation scripts

---

# Python/C++ → JavaScript Migration

| Python | C++ | JavaScript |
|---------|------|------------|
| `if:` | `if(){}` | `if(){}` |
| `elif` | `else if` | `else if` |
| `else:` | `else` | `else` |
| `match` (Python 3.10+) | `switch` | `switch` |

If you know Python or C++, JavaScript conditionals will feel familiar. The primary differences are syntax and the use of `switch`.

---

# What Are Conditional Statements?

A conditional statement allows your program to make decisions based on whether a condition evaluates to `true` or `false`.

```
Condition

↓

true ?

↓

Yes --------> Execute Block A

No ---------> Execute Block B
```

---

# The `if` Statement

Executes a block only when the condition is `true`.

Syntax

```javascript
if (condition) {
    // code
}
```

Example

```javascript
const age = 20;

if (age >= 18) {
    console.log("Eligible to vote");
}
```

Output

```
Eligible to vote
```

---

# The `if...else` Statement

Runs one block if the condition is true and another if it is false.

```javascript
const marks = 45;

if (marks >= 40) {
    console.log("Pass");
} else {
    console.log("Fail");
}
```

Output

```
Pass
```

---

# The `else if` Ladder

Useful when there are multiple possible outcomes.

```javascript
const score = 86;

if (score >= 90) {
    console.log("Grade A");
} else if (score >= 75) {
    console.log("Grade B");
} else if (score >= 60) {
    console.log("Grade C");
} else {
    console.log("Grade D");
}
```

Output

```
Grade B
```

Evaluation stops after the first matching condition.

---

# Nested `if`

An `if` statement inside another `if` statement.

```javascript
const loggedIn = true;
const isAdmin = false;

if (loggedIn) {
    if (isAdmin) {
        console.log("Admin Dashboard");
    } else {
        console.log("User Dashboard");
    }
}
```

Output

```
User Dashboard
```

Use nesting sparingly. Deep nesting reduces readability.

---

# The `switch` Statement

`switch` is useful when comparing one value against many fixed options.

Syntax

```javascript
switch (expression) {

    case value1:
        // code
        break;

    case value2:
        // code
        break;

    default:
        // code
}
```

---

# Example

```javascript
const day = 3;

switch (day) {

    case 1:
        console.log("Monday");
        break;

    case 2:
        console.log("Tuesday");
        break;

    case 3:
        console.log("Wednesday");
        break;

    default:
        console.log("Invalid Day");
}
```

Output

```
Wednesday
```

---

# Why Is `break` Important?

Without `break`, execution continues into the next case.

Example

```javascript
const day = 1;

switch (day) {

    case 1:
        console.log("Monday");

    case 2:
        console.log("Tuesday");

    case 3:
        console.log("Wednesday");
}
```

Output

```
Monday
Tuesday
Wednesday
```

This behavior is called **fall-through**.

---

# Intentional Fall-Through

Sometimes fall-through is useful.

```javascript
const role = "admin";

switch (role) {

    case "admin":
    case "manager":
        console.log("Can manage users");
        break;

    default:
        console.log("Limited access");
}
```

Both `"admin"` and `"manager"` share the same logic.

---

# `if` vs `switch`

| Use `if` | Use `switch` |
|-----------|--------------|
| Ranges (`age > 18`) | Fixed values |
| Multiple conditions | One variable, many cases |
| Complex logic | Simple menu-like logic |

---

# Ternary Operator Review

For simple conditions, the ternary operator is often cleaner.

```javascript
const age = 20;

const status = age >= 18 ? "Adult" : "Minor";

console.log(status);
```

---

# Best Practices

### Prefer Early Returns

Instead of

```javascript
if (user) {
    console.log("Welcome");
}
```

Avoid deeply nested code whenever possible.

---

### Use Braces

Even for a single statement.

Good

```javascript
if (isAdmin) {
    deploy();
}
```

Avoid

```javascript
if (isAdmin)
    deploy();
```

Braces reduce the risk of future bugs.

---

### Keep Conditions Simple

Instead of

```javascript
if (a && b && c && d && e)
```

Consider splitting complex logic into named variables.

```javascript
const hasAccess = a && b && c;

if (hasAccess) {
    deploy();
}
```

---

# Common Mistakes

### Assignment Instead of Comparison

Incorrect

```javascript
if (age = 18) {

}
```

This assigns a value instead of comparing.

Correct

```javascript
if (age === 18) {

}
```

---

### Forgetting `break`

The most common `switch` mistake.

---

### Deep Nesting

Instead of

```javascript
if (...) {
    if (...) {
        if (...) {
            ...
        }
    }
}
```

Break the logic into smaller functions when possible.

---

# DevSecOps Connection

Conditional statements are everywhere in automation.

## Deployment

```javascript
if (testsPassed && securityScanPassed) {
    deploy();
}
```

---

## Secret Validation

```javascript
if (!process.env.API_KEY) {
    console.error("API Key Missing");
}
```

---

## Docker Automation

```javascript
if (containerRunning) {
    restartContainer();
}
```

---

## CI/CD Pipeline

```javascript
if (branch === "main") {
    runProductionDeployment();
} else {
    runStagingDeployment();
}
```

---

## Log Monitoring

```javascript
if (failedLogins > 10) {
    sendAlert();
}
```

---

# Mini Project

Create

```
access-control.js
```

Requirements

Store

```javascript
const role = "admin";
const authenticated = true;
```

Output

- Admin Access
- User Access
- Guest Access
- Access Denied

Use both `if...else` and `switch`.

---

# Practice Questions

1. Difference between `if` and `switch`?
2. When should you use `switch`?
3. What is fall-through?
4. Why is `break` necessary?
5. What is a nested `if`?
6. What is an `else if` ladder?
7. Why are early returns considered good practice?
8. Why should you avoid deep nesting?
9. Give one DevSecOps use case for conditional statements.
10. Which conditional structure would you choose for validating HTTP status codes?

---

# Interview Questions

### Q1

Difference between `==` and `===` inside an `if` statement?

---

### Q2

Can `switch` compare ranges?

No. It compares against discrete values.

---

### Q3

Can multiple `case` labels execute the same code?

Yes. This is intentional fall-through.

---

### Q4

What happens if `break` is omitted?

Execution continues into subsequent cases.

---

# Key Takeaways

- Use `if` for ranges and complex conditions.
- Use `switch` for one variable with many fixed values.
- Always prefer `===` over `==`.
- Avoid deep nesting.
- Use braces consistently.
- Keep conditions readable.
- Conditional logic forms the backbone of automation scripts.

---

# Summary

You now know:

- `if`
- `if...else`
- `else if`
- Nested `if`
- `switch`
- `break`
- Fall-through
- Choosing between `if` and `switch`
- Common mistakes
- Best practices
- DevSecOps applications

---

# Next Chapter

## Chapter 5 – Loops

Topics include:

- `for`
- `while`
- `do...while`
- `for...of`
- `for...in`
- `break`
- `continue`
- Nested loops
- Performance considerations
- DevSecOps use cases
