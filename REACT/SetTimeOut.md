**setTimeout()*:*


The `setTimeout()` method calls a function after a number of milliseconds.

1 second = 1000 milliseconds.

## Notes:

- The `setTimeout()` is executed only once.

- If you need repeated executions, use `setInterval()` instead.

- Use the `clearTimeout()` method to prevent the function from starting.

- To clear a timeout, use the **id** returned from `setTimeout()`:

- myTimeout = setTimeout(_function_, _milliseconds_);

- Then you can to stop the execution by calling clearTimeout():

clearTimeout(myTimeout);


```js
function App() {

  let count = 0;

  const alertMe = () => {

    console.log(++count);

  };

  // console.log(alertMe);

  const stop= setTimeout(alertMe, 100);
 
```

**setInterval():**

The `setInterval()` method calls a function at specified intervals (in milliseconds).

The `setInterval()` method continues calling the function until `clearInterval()` is called, or the window is closed.

1 second = 1000 milliseconds.

## Note

To execute the function only once, use the `setTimeout()` method instead.

To clear an interval, use the **id** returned from setInterval():

myInterval = setInterval(_function_, _milliseconds_);

Then you can to stop the execution by calling clearInterval():

clearInterval(myInterval);

```js
function App() {

  let count = 0;
  const interval = () => {
    console.log(++count);
  };
  setInterval(interval, 2000000);
  
	//to stop use
	clearTimeout(fun)
}

```
