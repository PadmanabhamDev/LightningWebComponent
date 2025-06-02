
---

# JavaScript Object and JSON Operations

---

## 1. Creating Objects

```js
const person = {
  name: "Alice",
  age: 30,
  city: "New York"
};
```

---

## 2. Accessing Object Properties

* Dot notation:

```js
console.log(person.name);  // "Alice"
```

* Bracket notation (useful if property name is dynamic or has spaces):

```js
console.log(person["age"]);  // 30
```

---

## 3. Adding/Updating Properties

```js
person.email = "alice@example.com";  // add new property
person.age = 31;                     // update existing
```

---

## 4. Deleting Properties

```js
delete person.city;
```

---

## 5. Looping Over Object Properties

* Using `for...in` loop:

```js
for (let key in person) {
  console.log(key, person[key]);
}
```

* Using `Object.keys()`:

```js
Object.keys(person).forEach(key => {
  console.log(key, person[key]);
});
```

---

## 6. Checking if Property Exists

```js
console.log("name" in person);  // true
console.log(person.hasOwnProperty("email"));  // true
```

---

## 7. Cloning Objects

* Shallow clone using spread operator:

```js
const clone = {...person};
```

* Shallow clone using `Object.assign()`:

```js
const clone2 = Object.assign({}, person);
```

---

## 8. Merging Objects

```js
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const merged = {...obj1, ...obj2};
console.log(merged); // { a: 1, b: 3, c: 4 }
```

---

## 9. JSON Operations

* Convert object to JSON string:

```js
const jsonString = JSON.stringify(person);
console.log(jsonString);
```

* Parse JSON string back to object:

```js
const jsonObj = JSON.parse(jsonString);
console.log(jsonObj.name);  // "Alice"
```

---

## 10. Deep Copy (Using JSON methods for simple objects)

```js
const deepCopy = JSON.parse(JSON.stringify(person));
```

## 11. JSON Operation
```
let options ={
  title:"zero to hero",
  age:23,
  type:"CRM"
}

console.log(Object.values(options));

//JSON.Stringify

console.log(JSON.parse(JSON.stringify(options)));

console.log(Object.keys(options));

for(let key in options){
  console.log(key, options[key]);
}

Object.keys(options).forEach(key =>{
  console.log(key, options[key]);
})
```

```js
const deepCopy = JSON.parse(JSON.stringify(person));
```

---
