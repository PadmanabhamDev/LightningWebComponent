In JavaScript, **data types** define the kind of value a variable can hold. There are two main categories:

---

## 📂 1. **Primitive Data Types**

These are immutable and stored directly in the variable.

| Type        | Example                           | Description                        |
| ----------- | --------------------------------- | ---------------------------------- |
| `String`    | `"Hello"` or `'Hi'`               | Text data                          |
| `Number`    | `42`, `3.14`, `-7`                | Integer and floating-point numbers |
| `BigInt`    | `12345678901234567890n`           | Very large integers                |
| `Boolean`   | `true`, `false`                   | Logical values                     |
| `undefined` | A declared variable with no value | Default value if not assigned      |
| `null`      | `null`                            | Represents "no value"              |
| `Symbol`    | `Symbol("id")`                    | Unique identifiers (rarely used)   |

---

## 📦 2. **Non-Primitive (Reference) Data Types**

Stored as references (pointers) to memory locations.

| Type       | Example                        | Description                      |
| ---------- | ------------------------------ | -------------------------------- |
| `Object`   | `{ name: "Alice", age: 25 }`   | Collection of key-value pairs    |
| `Array`    | `[1, 2, 3]`                    | List-like object                 |
| `Function` | `function() { ... }`           | Callable object (also an object) |
| `Date`     | `new Date()`                   | Date and time                    |
| `RegExp`   | `/abc/` or `new RegExp('abc')` | Regular expressions              |

---

## 🔍 Type Detection with `typeof`

```javascript
typeof "hello"      // "string"
typeof 42           // "number"
typeof true         // "boolean"
typeof undefined    // "undefined"
typeof null         // "object" ❗ (this is a historical bug)
typeof {}           // "object"
typeof []           // "object"
typeof function(){} // "function"
```

---

## 🧪 Type Coercion

JavaScript is **dynamically typed**, meaning:

```javascript
let x = 10;      // Number
x = "Ten";       // Now a String
```

It also performs **implicit type coercion**:

```javascript
"5" + 1   // "51" (number is coerced to string)
"5" - 1   // 4 (string is coerced to number)
```

---

## 🧠 Quick Summary

### ✅ Primitive:

* string, number, bigint, boolean, undefined, null, symbol

### ✅ Non-Primitive:

* object, array, function, date, regex, etc.
* Rest all are object in some form 
  ```markdown
  Array, Date, Math, String, etc
  ```

