In JavaScript, arrays come with a rich set of built-in methods that make it easy to manipulate and work with data. Here’s a categorized list of commonly used **array methods** in JavaScript:

---

### 🔹 **Creating Arrays**

* `Array.of(...items)` – Creates a new array from arguments.
* `Array.from(arrayLike)` – Creates a new array from an array-like or iterable object.

---

### 🔹 **Adding/Removing Elements**

* `push(item)` – Adds item(s) to the **end**.
* `pop()` – Removes item from the **end**.
* `unshift(item)` – Adds item(s) to the **beginning**.
* `shift()` – Removes item from the **beginning**.
* `splice(start, deleteCount, ...items)` – Add/remove items at any position.
* `slice(start, end)` – Returns a portion of the array (does not modify the original).

---

### 🔹 **Iteration and Transformation**

* `forEach(callback)` – Iterates over each item (no return).
* `map(callback)` – Transforms array and returns a new array.
* `filter(callback)` – Filters array based on condition.
* `reduce(callback, initialValue)` – Reduces array to a single value.
* `some(callback)` – Returns `true` if at least one element matches the condition.
* `every(callback)` – Returns `true` if **all** elements match the condition.
* `find(callback)` – Returns the **first** element matching the condition.
* `findIndex(callback)` – Returns the **index** of the first match.

---

### 🔹 **Searching & Indexing**

* `indexOf(item)` – First index of the item.
* `lastIndexOf(item)` – Last index of the item.
* `includes(item)` – Checks if the array contains the item.

---

### 🔹 **Sorting and Reversing**

* `sort(compareFunction)` – Sorts the array (default is lexicographic).
* `reverse()` – Reverses the array in place.

---

### 🔹 **Joining & Conversion**

* `join(separator)` – Joins elements into a string.
* `toString()` – Converts the array to a string (comma-separated).
* `flat(depth)` – Flattens nested arrays.
* `flatMap(callback)` – Maps and flattens in one go.

---

### 🔹 **Utility**

* `isArray(obj)` – Checks if the object is an array.
* `fill(value, start, end)` – Fills with static values.
* `copyWithin(target, start, end)` – Copies part of the array to another position.

---

### 🔹 Example

```javascript
let numbers = [1, 2, 3, 4, 5];

// Map: square each number
let squares = numbers.map(n => n * n); // [1, 4, 9, 16, 25]

// Filter: even numbers
let evens = numbers.filter(n => n % 2 === 0); // [2, 4]

// Reduce: sum of all numbers
let sum = numbers.reduce((acc, curr) => acc + curr, 0); // 15

// Push: add 6 to end
numbers.push(6); // [1, 2, 3, 4, 5, 6]

let arr = [2,3,4,5,6,7,8];

//map
//Syntax
/**
arr.methodName(function(currentItem,index,actualArray){
  
})//map always return array
*/

//forEach : will not return anything



let newArray = arr.map(function(currentItem,index,array){
  console.log(`currentItem is ${currentItem} index ${index} arr ${array}`)
  return currentItem*2
})

let newArray1 = arr.map(item=>{
  return (item>3)
})

console.log(newArray1)

let arr1 = arr.map(item=>{
  return item*item;
})

console.log(arr1);

console.log(newArray);

//filter

let filterValue = arr.filter(function(currentItem,index,arr){
  return currentItem>5;
})

console.log(filterValue);

let arr2 = [15,16,17,18,19,20];

let isAdult = arr2.some(item =>{
  return item>18
})

console.log(isAdult);


//sort 

var name = ['nikil','hanu','test'];
console.log(name.sort());//sort in alphabetical order

var nums = [4,1,7,9,10,2,13,56];
console.log(nums.sort((a,b) => {
  return (a-b)//desending order for acending b-a
}));

//reduce methods

/*
array.reduce(function(total,currentValue,index,array){
  
},initialValue)
*/

let num = [12,78,30];

let sum = num.reduce(function(total,currentValue){
  return total+currentValue
},0)

console.log(sum);




```

---

