Context provides a way to pass data through the component tree without having to pass the *props* down manually.


***Steps to create useContext:*

***Step 1)***

creating Context:


```jsx
const Context= React.createContext();
```

***Step 2)***

ceate provider:

warp the *provider* the parent where you want to store the data 

```jsx
<Context.Provider value={ //string or obj of values or array of values depends upon your usecase}> 

<Parent />

<Context.Provider>
```

***step 3)***
 in the child component  use the cosume

```jsx
import {useContext} from "./parent"

function child{

}
```

ctrl+space => it specifies the path of imported components

In my terms:

- first global ah oru context create pannikirom athan [const Context= React.createContext();]
- Then we provide access to the state by warping with provider. so provider kullla value kudukurom antha values thaan namma goloball ah use panna porom.  athan 
```jsx
<Context.Provider value={ //string or obj of values or array of values depends upon your usecase}> 

<Parent />

<Context.Provider>

```
- Then namba yentha component la use panna porom oh athula poi first import useContext, then inside the function of the component just create a variable which contains useContext the global value. Eg:
```jsx
import { CartContext } from '../App'

export default function Navbar() {
   const cartbox = useContext(CartContext)
   
   return ()
```

I've done this in Ecomm project so refer it for doubts (Navbar)