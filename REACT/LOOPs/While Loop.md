
The syntax of the `while` loop is:

```js
while (condition) {
    // body of loop
}
```
Here,

1.  A `while` loop evaluates the **condition** inside the parenthesis `()`.
2.  If the **condition** evaluates to `true`, the code inside the `while` loop is executed.
3.  The **condition** is evaluated again.
4.  This process continues until the **condition** is `false`.
5.  When the **condition** evaluates to `false`, the loop stops.


![[Pasted image 20221005105535.png]] 


# do…while Statements

A similar way to set up a `while` loop is with a `do…while`. A `do…while` statement is similar to a `while` loop in the fact that it will continue to run until the condition becomes false. *The only difference is the order in which the loop runs.* Here’s a simple example of a do…while statement:

```js
let i = 0;

do {

i += 1;

console.log(i);

} while (i < 5);
```

# Infinite Loops

Something that you need to be careful of when dealing with loops is creating one where a stopping condition is never met. This loop will run forever (infinitely) and can have negative consequences on your computer such as having it freeze and become unresponsive. Let’s take a look at a simple infinite while loop so you know how to avoid running into them.

```js
let i = 0;

while (i < 5) {

console.log(i);

}
```