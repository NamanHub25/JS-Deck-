# Strings in JS 
String in JS are text & Sequence of characters 

``` js
name = "Naman"
surname = 'Mehrotra' 

let empty = "" // We can also declare an empty string as a valid string
```

if we want to write code inside quotes then we can go like this
```js 
'this is how we write "code" inside a quote'
```

## Indexing in String

```js 
let name = "Naman"
```
Each letter of Naman can be accessed by indexing

- name[0] -> N
- name[1] -> a
- name[2] -> m
- name[3] -> a
- name[4] -> n

## Undefined & Null in JS 
- Undefined -> A variable that has not been assigned a value is of undefined type

```js
let name; // No value assigned so it is of type undefined 
```

- Null -> The null value represents that there is an intentional absence of an object

```js 
let a = null; // Output: null
```

## Template literals 
Nothing special in order to avoid writing +, "" we use ${} to print the value stored in the variable

```js

let firstName = "John";
let lastName = "Doe";

let text = `Welcome ${firstName}, ${lastName}!`; 
```

## String Methods 

``` js 
// trim() -> Removes white spaces from the end and returns a new string

let str = "Naman"
console.log(str.trim()) // Output: Naman(without white spaces)

// toUpperCase() and toLowerCase()

let str = "Naman"
str.toUpperCase() // NAMAN
str.toLowerCase() // naman

// indexOf() -> Returns the first index of occurance of some value or gives -1 if not found

let str = "I love coding"
str.indexOf("love") // 1
str.indexOf("coding") // 2

// slice() -> Returns a part of the original string as a new string
let str = "I love coding"

console.log(str.slice(1, 6)) // Output: love

// replace() -> Searches for a value in the string and replaces it with the requested value passed as an argument 

let str = "My name is Naman"
console.log(str.replace("Naman", "Kabir")) // Output: My name is Kabir

// repeat() -> Return a string with the number of copies of a string

let str = "Mango"
console.log(str.repeat(3)) // Output: MangoMangoMango
```


