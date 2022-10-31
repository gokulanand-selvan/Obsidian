The *switch* statement is used to perform different actions based on different conditions.

### Syntax

``` js
switch(_expression_) {  
  case _x_:  
    _// code block_    break;  
  case _y_:  
    _// code block_    break;  
  default:  
    // _code block_  
}

```
This is how it works:

-   The switch expression is evaluated once.
-   The value of the expression is compared with the values of each case.
-   If there is a match, the associated block of code is executed.
-   If there is no match, the default code block is executed.