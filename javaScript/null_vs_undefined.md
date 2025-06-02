

## ⚖️ `null` vs `undefined` in JavaScript

| Feature        | `null`                           | `undefined`                             |
| -------------- | -------------------------------- | --------------------------------------- |
| **Type**       | `object` (🛑 historical bug)     | `undefined`                             |
| **Represents** | Intentional absence of value     | Variable declared but not assigned      |
| **Set by**     | Developer                        | JavaScript (automatically)              |
| **Use case**   | Empty values, intentional resets | Uninitialized variables, missing params |
| **Falsy?**     | ✅ Yes                            | ✅ Yes                                   |

---

## 🧪 Examples

### 🔹 `undefined`

```javascript
let x;
console.log(x); // 👉 undefined

function doSomething(y) {
  console.log(y);
}
doSomething(); // 👉 undefined
```

### 🔹 `null`

```javascript
let user = null;
console.log(user); // 👉 null
```

---

## 🧮 Equality Comparison: `null` vs `undefined`

### 1. **Loose Equality (`==`)**

```javascript
null == undefined // 👉 true
```

> They are *loosely equal* because JavaScript performs type coercion.

---

### 2. **Strict Equality (`===`)**

```javascript
null === undefined // 👉 false
```

> They are *not strictly equal* — because their **types are different**.

---

## ✅ Summary

| Comparison           | Result  | Why                                       |
| -------------------- | ------- | ----------------------------------------- |
| `null == undefined`  | ✅ true  | Loose equality; both mean "no value"      |
| `null === undefined` | ❌ false | Different types (`object` vs `undefined`) |

---

## 🔍 Quick Rules of Thumb

* Use `undefined` for:

  * Default function parameters
  * Uninitialized variables
  * Optional object properties

* Use `null` for:

  * Explicitly resetting or emptying values
  * Placeholder for objects that are expected later


```Equality Operator
  console.log(2==2); // true
  console.log("2"===2) // false
   == will not check datatype, but if you use === if will check for datatype
```

---
