```js
function App() {

  let count = 0;

  const alertMe = () => {

    console.log(++count);

  };

  // console.log(alertMe);

  const stop= setTimeout(alertMe, 100);
 
```

SetInterval
```js
function App() {

  let count = 0;

  const interval = () => {

    console.log(++count);

  };

  setInterval(interval, 2000000);

}
```
to stop use *clearTimeout(fun)*