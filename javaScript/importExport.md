
# 📦 JavaScript Export & Import in LWC

In **Lightning Web Components (LWC)**, modular JavaScript helps keep code clean, reusable, and well-organized. You can export constants, functions, or classes from one file and import them into your component JavaScript files.

---

## 🔹 Exporting

### ✅ Named Export

Use the `export` keyword to export **multiple variables or functions** from a file.

```js
// utils.js
export const name = "Padmanabham";

export function getName() {
  return 'Hanu';
}
```

### ✅ Default Export

Use `export default` to export **only one** function or variable from a file.

```js
// user.js
const user = "salesforce";
export default user;
```

OR

```js
export default function minus(a, b) {
  console.log(a - b);
}
```

---

## 🔹 Importing

Use the `import` keyword to bring in functions or variables from another file/module.

### 👉 Multiple Named Imports

```js
import { name, getName } from './utils';
```

### 👉 Import All as Object

```js
import * as utils from './utils';

console.log(utils.name);
utils.getName();
```

### 👉 Default Import

```js
import user from './user';
```

### 👉 Combined Default and Named Imports

```js
import minus, { PI, add } from './utils';
```

---

## 🔸 Example: Utility Module in LWC

```js
// utils.js
const PI_DATA = 3.14;

function add(a, b) {
  console.log(a + b);
}

export { PI_DATA as PI, add };

export default function minus(a, b) {
  console.log(a - b);
}
```

```js
// someComponent.js
import minus, { PI, add } from './utils';

add(5, 3);        // Output: 8
minus(10, 4);     // Output: 6
console.log(PI);  // Output: 3.14
```
```js
Exporting - use export keyword to export many variable or many method from a file

export const name ="Padmanabham"

export function getName(){
  return 'Hanu';
}

Default export use export keyword to export only one variable or a method from a file

export default user = "salesforce";

importing - use import keyword to import variable or method from a given file path or module

multiple imports 
import {name,getName} from './filePath';

import * as utils from './filePath';

import user from './filePath';

examples

const PI_DATA = 3.14;

function add(a,b){
  console.log(a+b);
}

export {PI_DATA as PI ,add}

//ecport with default
export default function minus(a,b){
  console.log(a-b);
}


import minus, {PI,add} from './utils';





```
---

## 💡 LWC Use Cases for Export/Import

* Create **shared helper functions** (e.g., formatting dates, validation).
* Manage **Apex logic** in separate JS modules for cleaner component files.
* Split code into **reusable utilities** across multiple components.

---

> 📁 Tip: Keep utility files inside a `utils` folder in your LWC module or component directory for better structure.
