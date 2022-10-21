Method 1:

We can write in img tag

```js 
import img from "./comp/imges/logo.svg"
<img src={img}/>
```

method 2 :
 as an function

```js
<logo>
```
method 3

as a component

```js
function Forward() {

return (

<svg

stroke="currentColor"

fill="currentColor"

stroke-width="0"

viewBox="0 0 24 24"

height="20px"

width="20px"

xmlns="http://www.w3.org/2000/svg"

>

<path fill="none" d="M0 0h24v24H0V0z"></path>

<path d="M12 4l-1.41 1.41L16.17 11H4v2h12.17l-5.58 5.59L12 20l8-8-8-8z"></path>

</svg>

);

}
```