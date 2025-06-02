# destructuring in JavaScript #
---

## What is Destructuring in JavaScript?

**Destructuring** is a convenient way to extract values from arrays or properties from objects into distinct variables.

---

### 1. Array Destructuring

You can extract values from an array and assign them to variables in a single line:

```js
const numbers = [10, 20, 30];

// Traditional way:
const a = numbers[0];
const b = numbers[1];

// Using destructuring:
const [x, y, z] = numbers;

console.log(x); // 10
console.log(y); // 20
console.log(z); // 30
```

You can also skip some elements:

```js
const [first, , third] = numbers;
console.log(first); // 10
console.log(third); // 30
```

---

### 2. Object Destructuring

Extract properties from objects into variables by matching property names:

```js
const person = {
  name: "Alice",
  age: 25,
  city: "New York"
};

const name1 = person.name;

const { name, age } = person;

console.log(name); // Alice
console.log(age);  // 25
```

You can also rename variables:

```js
const { name: fullName, city } = person;
console.log(fullName); // Alice
console.log(city);     // New York
```

---

### 3. Default Values

You can provide default values in case the property or array element is `undefined`:

```js
const { country = "USA" } = person;
console.log(country); // USA
```

---

### 4. Nested Destructuring

Destructure nested objects or arrays easily:

```js
const user = {
  id: 101,
  profile: {
    username: "alice123",
    email: "alice@example.com"
  }
};

const { profile: { username, email } } = user;
console.log(username); // alice123
console.log(email);    // alice@example.com
```

---

### Summary

* **Array destructuring:** `const [a, b] = arr;`
* **Object destructuring:** `const { key1, key2 } = obj;`
* Supports defaults, renaming, nested patterns.

---

If you want, I can provide more examples or explain how destructuring is used in functions or parameters! Would you like that?
