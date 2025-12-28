## Identifiers in JS 

Identifiers are names used to identify variables, functions, classes, or other user-defined items in JavaScript.

Rules for Identifiers

Can contain:

- Letters (A–Z, a–z)
- Digits (0–9)
- Underscore (_)
- Dollar sign ($)
- Cannot start with a digit.
- Case-sensitive — myVar and myvar are different.
- Cannot be a reserved keyword (like if, for, class).
- Can use Unicode characters (e.g., π, 变量), but not recommended for code readability.

``` js 
let name;
let _count;
let $price;
let user1;
let πvalue;
```

❌ Invalid identifiers:

``` js
let 1name;     // starts with a digit
let for;       // reserved keyword
let my-name;   // hyphen not allowed
```

## Keywords in JS 

Keywords are reserved words in JavaScript that have a predefined meaning and cannot be used as identifiers.

# Common JS keywords 
| Category | Examples |
|----------|----------|
| Control Flow | `if`, `else`, `switch`, `case`, `default` |
| Loops | `for`, `while`, `do`, `break`, `continue` |
| Declarations | `var`, `let`, `const`, `function`, `class` |
| Values | `true`, `false`, `null`, `undefined` |
| Operators | `instanceof`, `typeof`, `delete`, `in` |
| Error Handling | `try`, `catch`, `throw`, `finally` |
| Modules | `import`, `export` |
| Others | `this`, `super`, `new`, `return`, `yield` |

## Some important keyowrds in JS used commonly!
There are three ways to declare variables:

- var (old way)
- let (modern)
- const (modern & preferred for constants)

1️⃣ var
- var is the oldest way to declare variables in JavaScript (before ES6).

📍 Scope
- Function scoped
- NOT block scoped

``` js 
function testVar() {
  var x = 10;
  if (true) {
    var x = 20;
    console.log(x); // 20
  }
  console.log(x); // 20
}
testVar();
```
👉 var ignores block {} scope.

⚠️ Hoisting
- var is hoisted
- Initialized with undefined

``` js
console.log(a); // undefined
var a = 5;
```

❌ Common Mistakes
- Unexpected value changes due to lack of block scope
- Using var instead of let in loops

``` js for (var i = 0; i < 3; i++) 
console.log(i); // 3 (leaks outside loop)
```

❌ Why avoid var?

- Causes bugs
- Not predictable
- Rarely used in modern JavaScript

✅ Best Use Case
- When variable value will change
- Loops, conditions, counters

2️⃣ let
- let is a modern way to declare variables introduced in ES6.

📍 Scope
- Block scoped
- Limited to {} where it is declared


``` js 
let x = 10;
if (true) {
  let x = 20;
  console.log(x); // 20
}
console.log(x); // 10
```
⚠️ Hoisting
- let is hoisted
- But not initialized
- Exists in Temporal Dead Zone (TDZ)

``` js 
console.log(a); // ReferenceError
let a = 10;
```

❌ Common Mistakes
- Using before declaration
- Confusing hoisting behavior

```js
{
  console.log(x); // ❌ Error
  let x = 5;
}
```

✅ Best Use Case
- When variable value will change
- Loops, conditions, counters

3️⃣ const
- const is used to declare constants whose reference cannot be changed.

📍 Scope
Block scoped (same as let)

``` js 
const pi = 3.14;
console.log(pi); // 3.14
```
❌ Reassignment Not Allowed

```js
const x = 10;
x = 20; // ❌ TypeError
```

⚠️ Important Concept (Objects & Arrays)
❗ const does NOT make values immutable

```js 
const arr = [1, 2, 3];
arr.push(4); // ✅ Allowed
console.log(arr);
```

```js
const obj = { name: "JS" };
obj.name = "JavaScript"; // ✅ Allowed
```

🚫 But reassigning is not allowed:
``` js 
arr = []; // ❌ Error
```
❌ Common Mistakes
- Thinking const means value can’t change
- Forgetting to initialize


✅ Best Use Case
- When variable should not be reassigned
- Objects, arrays, fixed values

| Feature   | var             | let       | const     |
| --------- | --------------- | --------- | --------- |
| Scope     | Function        | Block     | Block     |
| Hoisted   | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
| Reassign  | ✅               | ✅         | ❌         |
| Redeclare | ✅               | ❌         | ❌         |
| Use Today | ❌               | ✅         | ✅         |

