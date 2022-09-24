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