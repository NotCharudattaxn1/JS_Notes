# JavaScript Fundamentals

## Chapter 1 -- What is JavaScript?

### Introduction

Imagine opening a website like YouTube.

When you click the **Like** button:

-   The button changes color.
-   The number of likes increases.
-   The page doesn't reload.

How is this possible?

HTML only creates the button.

CSS only changes how it looks.

Something has to tell the browser:

> "When the user clicks this button, increase the number of likes."

That "something" is **JavaScript**.

------------------------------------------------------------------------

## Definition

JavaScript is a **high-level programming language** primarily used to
add **behavior, logic, and interactivity** to websites.

Without JavaScript, websites would mostly contain static information.

------------------------------------------------------------------------

## Real-Life Analogy

Imagine building a car.

-   **HTML** is the body of the car.
-   **CSS** is the paint and design.
-   **JavaScript** is the engine.

Without an engine, the car may look beautiful but it cannot move.

Similarly, without JavaScript, your webpage may look beautiful, but
nothing will happen when users interact with it.

------------------------------------------------------------------------

## Why was JavaScript created?

In the early days of the internet, websites only displayed information.

Example:

``` text
Welcome to ABC Company

About Us

Contact Us
```

Nothing moved.

Nothing changed.

Users couldn't interact.

People wanted websites to behave like applications.

So JavaScript was created in **1995** by **Brendan Eich** in just **10
days**.

Today JavaScript powers websites like:

-   YouTube
-   Facebook
-   Instagram
-   Netflix
-   Amazon

------------------------------------------------------------------------

## What can JavaScript do?

JavaScript can:

-   Change webpage content
-   Change webpage styles
-   Validate forms
-   Create games
-   Build mobile apps
-   Build backend servers using Node.js
-   Fetch data from APIs
-   Create animations
-   Develop full-stack applications

------------------------------------------------------------------------

## How JavaScript Works

### Step 1

Your browser downloads:

``` text
index.html
```

### Step 2

The browser reads HTML and creates the webpage structure.

``` text
Heading

Paragraph

Button

Image
```

### Step 3

CSS is applied.

### Step 4

The browser sees:

``` html
<script src="app.js"></script>
```

Now it knows it needs to execute JavaScript.

### Step 5

The JavaScript Engine executes the code.

Example:

``` javascript
button.onclick = function () {
    alert("Hello");
}
```

The browser now remembers that when someone clicks the button, it should
show a popup.

------------------------------------------------------------------------

## Browser JavaScript Engines

  Browser   Engine
  --------- ----------------
  Chrome    V8
  Edge      V8
  Firefox   SpiderMonkey
  Safari    JavaScriptCore

The engine converts JavaScript into machine code that your computer can
execute.

------------------------------------------------------------------------

## Why JavaScript is called an Interpreted Language

Unlike C++, JavaScript doesn't create an executable file.

Instead, the browser reads the code, understands it, and executes it
immediately.

------------------------------------------------------------------------

## Common Interview Questions

### Q1. Why do we need JavaScript if HTML already exists?

**Answer:**

HTML creates the webpage structure.

JavaScript makes the webpage interactive.

Without JavaScript, websites cannot respond dynamically to user actions.

------------------------------------------------------------------------

### Q2. Can JavaScript run without HTML?

Yes.

JavaScript can run:

-   Inside browsers
-   Inside Node.js
-   On servers
-   In desktop applications

------------------------------------------------------------------------

### Q3. Is JavaScript the same as Java?

No.

They are completely different programming languages.

The names are similar because of historical marketing reasons.

------------------------------------------------------------------------

## Summary

-   JavaScript adds behavior to webpages.
-   It runs inside a browser or a JavaScript runtime like Node.js.
-   It enables interactive and dynamic websites.
-   It is one of the three core web technologies along with HTML and
    CSS.
-   Modern web development relies heavily on JavaScript.

------------------------------------------------------------------------

## Interview Tip

When an interviewer asks, **"What is JavaScript?"**, avoid saying only:

> JavaScript is a scripting language.

Instead, explain what it does, where it runs, and why it's important.

> JavaScript is a high-level programming language that adds logic and
> interactivity to websites. It runs in the browser using a JavaScript
> engine and allows developers to build dynamic user interfaces,
> communicate with servers, validate forms, and create modern web
> applications.
