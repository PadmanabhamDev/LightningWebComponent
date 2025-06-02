
---

### ✅ **Two Common Ways to Add Events in JavaScript**

---

#### **1. HTML Event Handler Attributes**

These are directly added in the HTML element using attributes like:

```html
<button onclick="handleChange1()">Click me1</button>
```

* This method is **inline**.
* Events always begin with the keyword `on` (e.g., `onclick`, `onchange`, `onkeyup`).
* It couples JavaScript logic with the HTML structure — not recommended for large applications.

---

#### **2. `addEventListener()`**

This is a **JavaScript way** to attach event listeners:

```js
let btn1 = document.querySelector("#random");
btn1.addEventListener("click", handleChange2);
```

* More flexible and reusable.
* Can attach multiple listeners to the same event without overwriting.
* Recommended in modern development.

##### Remove listener:

```js
btn1.removeEventListener("click", handleChange2);
```

---

### 🌀 **Event Bubbling**

* Events in the DOM bubble from the **target element upward to its parents**.
* Allows parent elements to handle events from children.
* Can be controlled using `stopPropagation()`.

Example (not shown in your code, but implied if you had nested elements):

```js
element.addEventListener("click", (event) => {
  event.stopPropagation(); // Stops bubbling
});
```

---

### ⚙️ **Custom Events in JavaScript (and LWC)**

Custom Events are useful when you want to **trigger an event manually**, often to communicate between components.

#### Syntax:

```js
const myEvent = new CustomEvent("hello", {
  detail: { name: "John" }
});
element.dispatchEvent(myEvent);
```

❌ Your example had a small mistake:

```js
element.dispatchEvent(newCustomEvent("hello"),{detail : {name:"John"}}); // incorrect
```

✅ Corrected:

```js
const event = new CustomEvent("hello", { detail: { name: "John" } });
element.dispatchEvent(event);
```

---

### ⚡️ Now, Connect This with LWC

In **LWC**, event handling is inspired by modern JavaScript. Here's how these concepts apply:

#### 1. **Template Event Binding (like inline `onclick`)**:

```html
<template>
  <button onclick={handleClick}>Click Me</button>
</template>
```

#### 2. **JavaScript AddEventListener in LWC**:

Usually done in the `renderedCallback` lifecycle hook:

```js
renderedCallback() {
  this.template.querySelector("button").addEventListener("click", this.handleClick);
}
```

#### 3. **CustomEvent in LWC** (for parent-child communication):

From child component:

```js
this.dispatchEvent(new CustomEvent('hello', {
  detail: { name: 'John' }
}));
```

In parent component:

```html
<c-child onhello={handleHello}></c-child>
```

---

### ✅ Summary Using Your HTML Example:

| HTML Button | Method Used                                          | JavaScript Logic                    |
| ----------- | ---------------------------------------------------- | ----------------------------------- |
| `Click me1` | Inline `onclick`                                     | Directly calls `handleChange1`      |
| `Click me2` | Both `onclick` and `addEventListener`                | `handleChange2` may be called twice |
| `Click me3` | `onclick` + `mousemove` event via `addEventListener` | Shows `Math.random()` on hover      |

---
