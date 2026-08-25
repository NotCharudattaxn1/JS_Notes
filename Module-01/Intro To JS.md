# Module 1 - JavaScript Fundamentals

# Chapter 1 - Introduction to JavaScript

> **Level:** Beginner (No Prior JavaScript Knowledge Required)
>
> **Goal:** Understand what JavaScript is, how it works, and set up your development environment.

---

# Learning Objectives

After completing this chapter, you will be able to:

- Explain what JavaScript is
- Understand where JavaScript is used
- Differentiate JavaScript from Java
- Install Node.js
- Write your first JavaScript program
- Understand JavaScript syntax
- Use comments
- Print output using console.log()
- Avoid common beginner mistakes

---

# Prerequisites

You only need:

- Basic computer knowledge
- VS Code installed
- No programming experience required

---

# What is JavaScript?

JavaScript is a **high-level**, **interpreted**, and **dynamic** programming language.

It allows developers to create applications that can interact with users, process data, communicate with servers, and automate tasks.

Originally, JavaScript was created to make web pages interactive.

Today it powers:

- Websites
- Backend servers
- Cloud applications
- Desktop software
- Mobile apps
- APIs
- Automation tools
- DevOps utilities

---

# Why Should a DevSecOps Engineer Learn JavaScript?

Many DevSecOps tools use JavaScript or Node.js.

Examples include:

| Tool | JavaScript Usage |
|--------|------------------|
| GitHub Actions | Workflow automation |
| Node.js | Automation scripts |
| AWS Lambda | Serverless functions |
| Azure Functions | Cloud automation |
| Express.js | Backend APIs |
| npm | Package management |
| VS Code Extensions | JavaScript |

As a DevSecOps engineer, you may write scripts that:

- Scan log files
- Monitor servers
- Automate deployments
- Call cloud APIs
- Parse JSON files
- Generate reports

> **Important:** We are **not** learning JavaScript to become a frontend developer. We are learning it to automate infrastructure, cloud, and security tasks.

---

# A Brief History of JavaScript

| Year | Event |
|------|-------|
| 1995 | Created by Brendan Eich |
| 1996 | Netscape Navigator adopted JavaScript |
| 1997 | ECMAScript standard introduced |
| 2009 | Node.js released |
| Today | Used in web, cloud, automation, and DevOps |

---

# JavaScript vs Java

Many beginners confuse JavaScript with Java.

They are completely different languages.

| JavaScript | Java |
|------------|------|
| Lightweight scripting language | Object-oriented programming language |
| Runs in browsers and Node.js | Runs on the Java Virtual Machine (JVM) |
| Dynamic typing | Static typing |
| Primarily used for web and automation | Enterprise software, Android, backend systems |

---

# Where Can JavaScript Run?

JavaScript can run in two major environments.

## 1. Browser

Examples:

- Chrome
- Firefox
- Edge
- Safari

Browser JavaScript is mainly used to make websites interactive.

---

## 2. Node.js

Node.js allows JavaScript to run outside the browser.

This is the environment most relevant to DevSecOps.

Examples of tasks:

- Reading files
- Calling REST APIs
- Monitoring servers
- Automating deployments
- Working with Docker
- Working with Kubernetes

---

# How JavaScript Works

```
Your Code
     │
     ▼
JavaScript Engine
(V8)
     │
     ▼
Machine Code
     │
     ▼
Computer Executes Instructions
```

Google Chrome uses the **V8 Engine**.

Node.js also uses the **V8 Engine**.

That means JavaScript behaves similarly in both environments.

---

# Installing Node.js

Visit the official website:

https://nodejs.org

Download the **LTS (Long-Term Support)** version.

After installation, open a terminal and verify the installation.

```

node -v

```

Example output

```

v22.x.x

```

Check npm

```

npm -v

```

Example

```

10.x.x

```

If both commands work, your installation is successful.

---

# What is npm?

npm stands for

**Node Package Manager**

It allows developers to install reusable JavaScript packages.

Example:

```

npm install express

```

Later in this course, we will use npm to install:

- Express
- Axios
- ESLint
- Jest
- dotenv

---

# Setting Up VS Code

Install the following extensions:

- JavaScript (ES6) snippets
- ESLint
- Prettier
- Error Lens
- GitLens (optional)

These extensions improve productivity and code quality.

---

# Creating Your First JavaScript Program

Create a new folder:

```

JavaScript

```

Inside it, create a file:

```

hello.js

```

Write the following code:

```javascript
console.log("Hello, World!");
```

Save the file.

Run it using:

```

node hello.js

```

Output:

```

Hello, World!

```

Congratulations! 🎉 You have written your first JavaScript program.

---

# Understanding console.log()

`console.log()` prints information to the console.

Example:

```javascript
console.log("JavaScript");
console.log(100);
console.log(true);
```

Output:

```

JavaScript
100
true

```

You can print almost any data type.

---

# JavaScript Syntax

A programming language follows rules called **syntax**.

Example:

```javascript
console.log("Correct Syntax");
```

Incorrect:

```javascript
console.log("Missing bracket"
```

This results in a syntax error.

---

# Statements

A statement is an instruction.

Example:

```javascript
console.log("Statement 1");

console.log("Statement 2");
```

Each statement tells the computer to perform an action.

---

# Semicolons

JavaScript automatically inserts semicolons in many cases.

Example:

```javascript
console.log("Hello")
console.log("World")
```

This works.

However, professional developers still write:

```javascript
console.log("Hello");
console.log("World");
```

Using semicolons consistently improves readability and avoids edge-case bugs.

---

# Comments

Comments are ignored by the JavaScript engine.

They help explain code.

## Single-line comment

```javascript
// This is a comment
console.log("Hello");
```

## Multi-line comment

```javascript
/*
This
is
a
multi-line
comment.
*/
```

---

# Keywords

Keywords have special meaning.

Examples:

```
if
else
return
let
const
for
while
function
```

Do not use keywords as variable names.

Incorrect:

```javascript
let if = 10;
```

---

# Identifiers

Identifiers are names given to variables, functions, or classes.

Good examples:

```javascript
userName

totalMarks

serverIP

studentAge
```

Bad examples:

```javascript
123name

user-name

let
```

---

# Case Sensitivity

JavaScript is case-sensitive.

```javascript
let age = 20;

let Age = 30;
```

These are different variables.

---

# Common Errors Beginners Make

### 1. Forgetting quotation marks

Incorrect

```javascript
console.log(Hello);
```

Correct

```javascript
console.log("Hello");
```

---

### 2. Misspelling console.log

Incorrect

```javascript
consle.log("Hello");
```

---

### 3. Forgetting parentheses

Incorrect

```javascript
console.log;
```

---

### 4. Editing the wrong file

Always check the filename before running your program.

---

# Best Practices

✔ Name files clearly

✔ Keep code properly indented

✔ Use comments when necessary

✔ Write meaningful names

✔ Practice every day

✔ Learn by building programs

---

# Mini Exercise

Create a file named:

```
intro.js
```

Print the following:

```
Welcome to JavaScript

I want to become a DevSecOps Engineer

Learning JavaScript Step by Step
```

---

# Practice Questions

1. What is JavaScript?

2. Who created JavaScript?

3. What is Node.js?

4. What is npm?

5. Why is JavaScript useful for DevSecOps?

6. What is `console.log()` used for?

7. Explain the difference between Java and JavaScript.

8. What are comments?

9. What are identifiers?

10. Is JavaScript case-sensitive?

---

# Interview Questions

### Q1. What is JavaScript?

JavaScript is a high-level programming language used for building interactive websites, backend applications, APIs, automation scripts, and cloud services.

---

### Q2. What is Node.js?

Node.js is a runtime environment that allows JavaScript to run outside the browser.

---

### Q3. Why do DevSecOps engineers learn JavaScript?

Because JavaScript is widely used in automation, CI/CD pipelines, cloud functions, APIs, and Node.js-based tooling.

---

### Q4. What is npm?

npm (Node Package Manager) is the default package manager for Node.js. It is used to install and manage JavaScript libraries.

---

# Chapter Summary

In this chapter, you learned:

- What JavaScript is
- The history of JavaScript
- JavaScript vs Java
- Browser vs Node.js
- How JavaScript executes code
- Installing Node.js
- Running your first program
- Using `console.log()`
- Writing comments
- JavaScript syntax rules
- Common beginner mistakes

---

# What's Next?

In **Chapter 2**, we will learn:

- Variables
- Data Types
- Memory
- `let`, `const`, and `var`
- `typeof`
- Type Conversion
- Naming Conventions
- Best Practices

These concepts form the foundation of every JavaScript program you'll write.
