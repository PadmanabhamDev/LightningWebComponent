
---

## What is String Interpolation?

**String interpolation** is a way to embed expressions (like variables or calculations) directly inside a string, making it easier to build dynamic strings.

---

## How to do String Interpolation in JavaScript?

JavaScript uses **template literals** (backticks \`\`) for string interpolation.

### Syntax:

```js
const name = "Alice";
const greeting = `Hello, ${name}!`;
console.log(greeting);  // Output: Hello, Alice!
```

---

### More Examples:

#### Embedding expressions:

```js
const a = 5;
const b = 10;
console.log(`The sum of ${a} and ${b} is ${a + b}.`); 
// Output: The sum of 5 and 10 is 15.
```

#### Multiline strings with interpolation:

```js
const multiline = `This is line 1
This is line 2 with variable: ${name}`;
console.log(multiline);
```

---

### Why use string interpolation?

* Easier to read and write than concatenation.
* Supports multiline strings.
* Allows embedding any JavaScript expression inside `${...}`.

---
