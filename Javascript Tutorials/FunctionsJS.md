# Functions 
🧩 Why Do We Need Functions?
- Imagine writing a large program without functions — every time you need a specific logic (say, calculating tax or formatting a date), you’d have to **copy–paste** that logic again and again.

Functions solve this problem by letting us:

- **Reuse code** (write once, use many times)
- **Organize logic** (split program into small logical blocks)
- **Reduce errors** (fix in one place → fixed everywhere)
- **Improve readability** and testing

👉 So conceptually, a **function** is just a **block of code that performs a specific task**, which can be “called” whenever needed.

Just like an automobile only performs its task (moving) when **you start it**, a **JavaScript function** also does nothing until it’s **called (invoked)**.

Let’s link that analogy directly to code:
- When you **define** a function, you’re *building the car*.
- When you **call** a function, you’re *turning the key to start it*.

🚀 Basic Function Syntax (Function Declaration)

```js
function functionname(paramater1, parameter2){
    // code to be executed
}

functionname(parameter1, parameter2) // function calling
```

```js

// Function declaration
function myname() {
  let name = "Naman Mehrotra";
  console.log(`My name is ${name}`);
}

// Function use --> Function call
myname();

✅Output: My name is Naman Mehrotra
```

```js 
function parafunc(num){
    console.log(`The number is: ${num}`);
}

parafunc(10);

✅Output: The number is: 10
```

```js 
// Return function 
function returnsum(num1, num2){
    let sum = (num1 + hnum2)
    return sum;
}

let result = returnsum(10, 20);
console.log(`Total sum is: ${result}`);

✅Output: Total sum is: 30
```

## Function expression & Arrow functions


```js
// Function expression

let greet = function(name){
    return `Hello ${name}`;
}

console.log(greet("Naman"));
✅Output: Hello Naman
```

```js
// Arrow Functions

let greet = (name) => {
    return `Good Morning ${Naman}`;
}
console.log(greet("Naman"));

✅Output: Good morning Naman
```

