# **1) Introduction**

# **2) What are side effects and introducing useEffect()**
         side effect is also called Effect. So what is an effect?

## What are side effects in React?

Side effects are *not predictable* because they are actions which are performed with the *"outside world"*. We perform a side effect when we *need to reach outside of our React components* to do something. Performing a side effect, however, will not give us a *predictable result*.


   *1).* So the React library itself has one main job to render the UI, to React to our user input, to re-render the UI when it's needed.
   
  *2).*  *The main job of React we learnt so far* :
  We wanna evaluate and render the JSX code and the Dom. We wanna manage state and props to make sure that every component has the data it needs and that we reflect the user input correctly. We wanna React to user events as mentioned and of course React is there to also re-evaluate our components and their JSX code and manipulate the real Dom as needed. So that's all baked into React with the tools and features. 
  So everything we have in the *component function* is to up to bring *something* on the screen.
  
  In side effects for example if we send an *http:* request directly in a function it send the *http:* request whenever the function *re-runs* , if it re-runs it creates the infinite loop or it sends too manty http:: request, Therefore we have a  tool to handle the sideEffects which is called ***useEffect()*** 

### useEffect() Hook:
The useEffect() hook is a built-in hook Function.
- The useEffect() is called with *two arguments with two parameters*
- The first argument is a *function* that should be *executed* after every *component evaluation* if a specified *dependencies* is changed.
- And the *specified dependencies* are the *second arguments* you passed in.

- SYNTAX:    

``` js
useEffect( () => {...}, [ dependencies ] );
```

[ In short, **useEffect is a tool that lets us interact with the outside world but not affect the rendering or performance of the component that it's in.** ]

**Dependencies in useEffect():**
 - There is a dependency array **to control when the effect should run**.
 - It runs when the component is mounted and when it is re-rendered while a dependency of the useEffect() has changed.