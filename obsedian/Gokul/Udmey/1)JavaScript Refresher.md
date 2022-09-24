**1) Let, Constant**

**2)Arrow Functions:**
Arrow Function helps to overcome "this" keyword or method.

**3) Exports and Imports :**

   *Default Export:*
   
    You choose the name.
```js
import Anyname from './person.jsx'
```

*Named Export:*

   We can't give any name ,we have to mention the Given name.

**4)Classes**

**5)Spread Operators & Rest Operators:**
     *Spread :*
     
     Spread used to copy the old objects or  array and display in new object or array.
```js
[...arr,myobj]
```
  
  *Rest:*
  
     The Rest operator used to merge a list of funcuntion arguments in array.
     
**6)Destructing:**

Easily Extracts array elements or object properties and store them in  variables.

**7)Reference and Primitive Data Types:**

 *Primitive:*
     Number, strings, Booleans, there are primitive data types. Whenever we re-assign or store a variable in another variable it will copy the value. 
 ```Js
 const number= 1;
 const num2 = number;
 console log(num2)
```
Output= 1 .

*Reference:*
  The objects and arrays are the reference data types. If we Reassign them You are copying the pointer not the value.
    Therefore if you want to do this in a real copy way, you will have to create a new object and copy the properties not the entire objects.
```js 
const Person ={
name= "person"
}

const secondPerson = Person;
person.name='gokul'
Console log(SecondPrson)

OUTPUT:
[object,object]{
name: 'gokul'
}
```

```js
const person ={
name:'max'
}
const scondPerson={ ...person};
person.name ="gokul";
console log( secondPerson)

O/P

[object,object]{
name="Max"
}
```

**8) Reffering Array Funcuntions:**

*1)map:*
      It is a Built in method in JavaScript.
  So map takes Function as an input and executed on each element in array and it returns a new Value or Array.
```js
const numbers=[1,2,3,4]

const arr = numbers.map((num) => {return num*2;})


O/P
[1,2,3] and [2,4,6]
```
This internal area functions depends on which area of function you are using.
