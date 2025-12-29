# Math Object
It is a collection of mathematical properties 

## Properties
- Math.PI
- Math.E

## Methods
- Math.abs(n)
- Math.floor(n)
- Math.ceil(n)
- Math.random()
- Math.pow(a,b)

# setTimeOut() function

The setTimeout() method calls a function after a number of milliseconds.

```js 
const myTimeout = setTimeout(myGreeting, 5000);

function myStopFunction() {
  clearTimeout(myTimeout);
}
```

# setInterval() function
- The setInterval() method calls a function at specified intervals (in milliseconds).
- The setInterval() method continues calling the function until clearInterval() is called, or the window is closed.

```js
setInterval(myTimer, 1000);

function myTimer() {
  const date = new Date();
  document.getElementById("demo").innerHTML = date.toLocaleTimeString();
}
```


