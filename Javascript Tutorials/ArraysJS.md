# Arrays
An `Array` is an object type designed for storing data collections.

Key characteristics of JavaScript arrays are:

- **Elements**: An array is a `list of values`, known as `elements`.
- **Ordered**: Array elements are ordered based on their `index`.
- **Zero indexed**: The first element is at index 0, the second at index 1, and so on.
- **Dynamic size**: Arrays can grow or shrink as elements are `added` or `removed`.
- **Heterogeneous**: Arrays can store elements of different `data types`(numbers, strings, objects and other arrays).

Arrays can be created using two methods 

-  Using the Arrays constructor method 
-  Using square brackets `[]`

```js
//Array creation using [] brackets
let nums = [1, 2, 3, 4, 5];
console.log(nums);

// Array creation using multiple elements
let arr = [1, "Naman", 2, 5];
console.log(arr);

// Array creation using Array constructor
let num = new Array(1, "Naman", 2, 7);
console.log(num);

✅Output: [ 1, 2, 3, 4, 5 ]
           [ 1, 'Naman', 2, 5 ]
           [ 1, 'Naman', 2, 7 ]
```

## How can we access array elements ?
We can access the array elements using the concept of indexing

```let nums = [1, 2, 3, 4, 5] ```
- nums[0] -> 1
- nums[1] -> 2
- nums[2] -> 3
- nums[3] -> 4
- nums[4] -> 5

```js 
// Not important but often we don't notice these features of arrays in JS
let info = ["Naman", 22, 6.1]

info[0] = Naman
info[0][2] = m

info[2] = 5.11

// New array
["Naman", 22, 5.11] // In JS arrays are mutable i.e. we can modify them
```

## Array Methods

| **Category** | **Method** | **Description** | **Returns New Array?** | **Mutates Original?** |
| --- | --- | --- | --- | --- |
| **Adding / Removing Elements** | `push()` | Adds elements to the **end** | ❌ No | ✅ Yes |
|  | `pop()` | Removes last element | ❌ No | ✅ Yes |
|  | `unshift()` | Adds elements to the **start** | ❌ No | ✅ Yes |
|  | `shift()` | Removes first element | ❌ No | ✅ Yes |
|  | `splice(start, deleteCount, ...items)` | Adds/removes at specific index | ❌ No | ✅ Yes |
|  | `slice(start, end)` | Returns portion of array | ✅ Yes | ❌ No |
| **Combining / Splitting** | `concat()` | Combines arrays | ✅ Yes | ❌ No |
|  | `join(separator)` | Joins elements into a string | ❌ No | ❌ No |
| **Searching / Checking** | `indexOf(value)` | Finds index of value | ❌ No | ❌ No |
|  | `lastIndexOf(value)` | Finds last occurrence | ❌ No | ❌ No |
|  | `includes(value)` | Checks if value exists | ❌ No | ❌ No |
|  | `find(callback)` | Returns first element matching condition | ❌ No | ❌ No |
|  | `findIndex(callback)` | Returns index of first match | ❌ No | ❌ No |
| **Transforming Arrays** | `map(callback)` | Transforms each element | ✅ Yes | ❌ No |
|  | `filter(callback)` | Keeps elements that pass condition | ✅ Yes | ❌ No |
|  | `reduce(callback, initialValue)` | Reduces to single value | ❌ No | ❌ No |
|  | `forEach(callback)` | Loops through elements | ❌ No | ❌ No |
|  | `flat(depth)` | Flattens nested arrays | ✅ Yes | ❌ No |
|  | `flatMap(callback)` | Maps + flattens one level | ✅ Yes | ❌ No |
| **Sorting / Reversing** | `sort(compareFn)` | Sorts array (alphabetically by default) | ❌ No | ✅ Yes |
|  | `reverse()` | Reverses array order | ❌ No | ✅ Yes |
| **Testing / Validation** | `every(callback)` | Checks if all match condition | ❌ No | ❌ No |
|  | `some(callback)` | Checks if at least one matches | ❌ No | ❌ No |
| **Conversion & Others** | `toString()` | Converts to string | ❌ No | ❌ No |
|  | `Array.isArray(value)` | Checks if a value is an array | ❌ No | ❌ No |
|  | `fill(value, start, end)` | Fills elements with a value | ❌ No | ✅ Yes |
|  | `copyWithin(target, start, end)` | Copies elements within array | ❌ No | ✅ Yes |

## Nested Arrays
Nested arrays are basically array of arrays 

```js
let nums = [[1, 2], [3, 4], [5, 6]] // Basically 2D arrays 

nums[0] = [1, 2]
nums[0][1] = [1]
```
## There are 3 functions used on Arrays and are really very important!!
3 main methods with some special feature which are map(), filter() and reduce()

 - map() —> The [map()](https://www.geeksforgeeks.org/javascript/javascript-array-map-method/) method in [JavaScript](https://www.geeksforgeeks.org/javascript/javascript-tutorial/) is used to create a new array by applying a function to each element of the original array. It iterates through each element of the array and invokes a callback function for each element. The result of the callback function is then added to the new array.

 ```js 
let arr = [2, 4, 8, 10]
let updatedArr = arr.map(val=> val+2)
console.log(arr);
console.log(updatedArr);

✅Output: [4,6,10,12]
```

- filter() —> The [filter()](https://www.geeksforgeeks.org/javascript/javascript-array-filter-method/) method in JavaScript is used to create a new array with all elements that pass a certain condition defined by a callback function. It iterates through each element of the array and invokes the callback function for each element. If the callback function returns true for an element, that element is included in the new array; otherwise, it is excluded

```js 
let arr = [2, 4, 8, 10];
let updatedArr = arr.slice().filter(val => val < 5);
console.log(arr);
console.log(updatedArr);

✅Output: [8, 10]
```

- reduce() —> The [reduce()](https://www.geeksforgeeks.org/javascript/javascript-array-reduce-method/) method in JavaScript is used to reduce an array to a single value. It executes a provided callback function once for each element in the array, resulting in a single output value. The callback function takes four arguments: accumulator, currentValue, currentIndex, and the array itself.

```js 
let arr = [2, 4, 8, 10];
let updatedArr = arr.slice().filter(val => val < 5);
console.log(arr);
console.log(updatedArr);
```