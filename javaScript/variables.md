In JavaScript, **scope** refers to the accessibility of variables and functions in different parts of your code. Understanding the different types of scope is crucial for writing clean, bug-free programs.

Here’s a breakdown of the three main scopes in JavaScript:

---

## 🌐 1. Global Scope

* Variables declared **outside** any function or block.
* Accessible from **anywhere** in your code (unless shadowed).
* Defined using `var`, `let`, or `const` at the top level.

### Example:

```javascript
let globalVar = "I'm global";

function printGlobal() {
  console.log(globalVar); // ✅ accessible
}
printGlobal();
```

---

## 🧱 2. Block Scope

* Variables declared **inside a block** (between `{ }`) using `let` or `const`.
* Not accessible **outside** that block.

### Example:

```javascript
{
  let blockVar = "I'm in a block";
  console.log(blockVar); // ✅ accessible here
}
console.log(blockVar); // ❌ ReferenceError
```

> ❗ `var` is **not block-scoped** — it leaks out of blocks.

```javascript
{
  var leakyVar = "Oops";
}
console.log(leakyVar); // ✅ still accessible
```

---

## 🔧 3. Function Scope

* Variables declared **inside a function** using `var`, `let`, or `const`.
* Accessible **only within** that function.

### Example:

```javascript
function myFunction() {
  let functionVar = "Inside function";
  console.log(functionVar); // ✅ accessible
}
myFunction();
console.log(functionVar); // ❌ ReferenceError
```

---

## 🧠 Summary Table

| Scope Type | Declared with         | Accessible From                        | Notes                                      |
| ---------- | --------------------- | -------------------------------------- | ------------------------------------------ |
| Global     | `var`, `let`, `const` | Anywhere in the code                   | Avoid polluting global scope               |
| Block      | `let`, `const`        | Only inside `{}`                       | Best practice for loops, if-blocks         |
| Function   | `var`, `let`, `const` | Only inside the function where defined | `var` is function-scoped, not block-scoped |

---


### 🧠 What This Diagram Shows:

* **Global Scope** contains everything.
* **Function Scope** exists inside the global.
* **Block Scope** is nested within functions (or even loops/conditionals).

---

## ✅ Example Using `let`, `const`, and `var` in All Scopes

```javascript
// 🌐 Global Scope
var globalVar = "I'm a global var";
let globalLet = "I'm a global let";
const globalConst = "I'm a global const";

function exampleFunction() {
  // 🔧 Function Scope
  var functionVar = "I'm a function-scoped var";
  let functionLet = "I'm a function-scoped let";
  const functionConst = "I'm a function-scoped const";

  console.log("--- Inside function ---");
  console.log(globalVar);      // ✅ accessible
  console.log(globalLet);      // ✅ accessible
  console.log(globalConst);    // ✅ accessible
  console.log(functionVar);    // ✅ accessible
  console.log(functionLet);    // ✅ accessible
  console.log(functionConst);  // ✅ accessible

  if (true) {
    // 🧱 Block Scope
    var blockVar = "I'm a block var (but leak out!)";
    let blockLet = "I'm a block-scoped let";
    const blockConst = "I'm a block-scoped const";

    console.log("--- Inside block ---");
    console.log(blockVar);     // ✅ accessible
    console.log(blockLet);     // ✅ accessible
    console.log(blockConst);   // ✅ accessible
  }

  console.log("--- After block ---");
  console.log(blockVar);       // ✅ still accessible (var is NOT block-scoped)
  // console.log(blockLet);    // ❌ ReferenceError
  // console.log(blockConst);  // ❌ ReferenceError
}

exampleFunction();

console.log("--- Global scope again ---");
console.log(globalVar);        // ✅ accessible
console.log(globalLet);        // ✅ accessible
console.log(globalConst);      // ✅ accessible
// console.log(functionVar);   // ❌ ReferenceError
// console.log(blockVar);      // ❌ ReferenceError
```

---

## 🔍 Key Takeaways

| Keyword | Scope Type      | Can Reassign? | Can Redeclare in Same Scope? | Block Scoped? |
| ------- | --------------- | ------------- | ---------------------------- | ------------- |
| `var`   | Function/global | ✅ Yes         | ✅ Yes                        | ❌ No          |
| `let`   | Block           | ✅ Yes         | ❌ No                         | ✅ Yes         |
| `const` | Block           | ❌ No          | ❌ No                         | ✅ Yes         |

---

Let me know if you want this in a downloadable file, with comments and visualization!
