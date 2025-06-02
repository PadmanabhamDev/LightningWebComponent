
---

# JavaScript String Methods

JavaScript strings come with many built-in methods to work with text. Here are some commonly used ones:

---

### 1. `.length`

Returns the length of the string.

```js
let str = "Hello";
console.log(str.length);  // Output: 5
```

---

### 2. `.toUpperCase()` and `.toLowerCase()`

Convert string to uppercase or lowercase.

```js
console.log("hello".toUpperCase());  // "HELLO"
console.log("WORLD".toLowerCase());  // "world"
```

---

### 3. `.indexOf()`

Returns the index of the first occurrence of a substring (or -1 if not found).

```js
let str = "JavaScript";
console.log(str.indexOf("Script"));  // 4
console.log(str.indexOf("script"));  // -1 (case-sensitive)
```

---

### 4. `.includes()`

Returns `true` if substring is found, else `false`.

```js
console.log("Hello world".includes("world"));  // true
```

---

### 5. `.slice()` and `.substring()`

Extract a part of a string.

```js
let str = "Hello world";
console.log(str.slice(0, 5));      // "Hello"
console.log(str.substring(6, 11)); // "world"
```

---

### 6. `.replace()`

Replace part of a string (only the first occurrence unless using regex).

```js
let str = "Hello world";
console.log(str.replace("world", "there"));  // "Hello there"
```

---

### 7. `.split()`

Split string into an array by a separator.

```js
let str = "a,b,c,d";
console.log(str.split(","));  // ["a", "b", "c", "d"]
```

---

### 8. `.trim()`

Remove whitespace from both ends of a string.

```js
let str = "   hello   ";
console.log(str.trim());  // "hello"
```

---

### 9. `.charAt()`

Returns character at a given index.

```js
let str = "hello";
console.log(str.charAt(1));  // "e"
```

---

### 10. `.repeat()`

Repeats the string a specified number of times.

```js
console.log("ha".repeat(3));  // "hahaha"
```

---

If you want, I can show you code examples or explain any specific method in detail! Just let me know.
