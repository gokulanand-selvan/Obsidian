**1)What is React Router?**

- It is one of React Library
- It is a fully-Featured ***client and server side*** Routing library for React
- It helps to ***Create and Navigate between URL'ss***  that make our web application
- It provides unique URL's for the different components and makes the UI easily shareable with other users.

**2) Installation:**

```npm
npm install react-router-dom@6 
(or)
yarn add react-router-dom@6 
```





**Configuring Routes :**

*step 1:* 
In Index.js  Add BrowserRouter to the App component. (Root of the components)

```js

 <React.StrictMode>

    <BrowserRouter>

      <App />

    </BrowserRouter>

  </React.StrictMode>
```

*step 2:*

Create the required components that need to rendered in different URL paths
Eg:
LoginPage.jsx , SignUpPage.Jsx

*Step 3: 

So in App.js import and set the path for the Components.

```js
import { Routes,Route } from "react-router-dom";

function App() {

  return (

    <Routes>

      <Route path="/" element={<Login />} />

      <Route path="/signUp" element={<SignUp />} />

    </Routes>

  );

}
```

In the browser search as localhost:3000/ =>it shows as the login page ,  localhost:3000/signUp =>it shows as the signUp page.

***3) Links :***

Links helps to Navigate to different Routes in the UI. If we click it rout to that page.

```js

import { Link } from "react-router-dom"; //Importing the links from the router

import React from "react";

export const NavBar = () => {

  return (

    <nav> // nav 

      <Link to="/">Login </Link>   \\ Links contains the path to the components 

      <br />

      <Link to="/SignUp">SignUp</Link>

    </nav>

  );

};

```

***4) Active Links :*** 

The active links are the **Navlink** Which highlights the active link which we can make use in *styling.* If we use nav link and go to the browser just inspect the page the clicked link will be *active.*  In the case of styling we can style by using *Nav a.active* in Css. 
The NavLink is specifically used for Navigation Bar , Bread Crumbs, or set of Tabs which we like to highlight. 

```js
import { Link } from "react-router-dom";

import React from "react";

  

export const NavBar = () => {

  return (

    <nav>

      <NavLink to="/"> Login </NavLink>

      <br />

      <NavLink to="/SignUp"> SignUp </NavLink>

    </nav>

  );

};

```

***5) Navigating Programmatically :***

For Navigating programmatically we use ***useNavigate*** hook.

```js
import { useNavigate } from "react-router-dom";

export const Login = () => {

 const navigate = useNavigate();
 
  \\ useNavigate returns a funcuntion called navigate\\

return(
<> 
<button type="Submit" onClick={() => navigate("/signUp")}>SignUp</button>
</>
);

}

```

***6) No Match Route :***

No match route is used  when the url does not exists.

```js
import React from "react";

export const NoMatch = () => {

  return <div>Page Not Found</div>;

\\ In app.js

  <Routes>
<Route path="*" element={<NoMatch />} />
</Routes>

};
```