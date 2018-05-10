# JavaScript-Cheatsheet

## Table of Contents 

1. [Basics](#Basics)

<a name="Basics"></a>

## 1. Basics

### 1. Variable declaration: 

  ```
  var camelCaseString = 'Some string'
  ```
  
  ```
  var camelCaseInt = 24
  ```

  ```
  var camelCaseFloat = 2.40
  ```

  ```
  var camelCaseBoolean = true
  ```

  ```
  var camelCaseArray = ['Some string', 513, false, [ 1,3,2 ], { someKey: someValue }]
  ```

  ```
  var camelCaseObject = { key: value, anotherKey: anotherValue }
  ```

  ```
  // In-line comments look like this
  ```

  ``` 
  /* 
  Block level comments
  look like this 
  */
  ```

###  2. Conditionals: 

#### If statements:

  ``` 
  if (thisValue > thisOtherValue) {
    // do something here
  } else if (thisValue === someRandomValue) {
    // do something else here
  } else {
    // do something completely different
  }
  ```

#### Switch statements:

  ```
  switch (someVariableToSwitchOn) {
    case ifX: 
      // do something here
      break;
    case ifY:
      // do something else here
      break;
    case ifY: 
      // do something completely different
      break;
    default:
      // if none of the cases are met, do this by default
  }
  ```

### 3. Loops:

#### For-Loop:

  ```
  for (var iteratingVariable = <someStartingValue>; some conditional statement; some increment or decrement value) {
    // do anything written in this code block until the above condition has been met
  }
  ```

#### While-loop:
  ```
  while (someConditional) {
    // do something while the above conditional is satisfied
    if (<some other condition is satisfied>) {
      return someValue;
      // Don't forget to have some sort of an exit from a while loop, or else you'll have created an infinite loop, which can cause your program to crash!
    }
  }
  ```

  Note: There are several other types of loops but we can go over those later :) 

### 4. Operators:

| Operator        | Explanation           | Symbols  | Example   |
| -------------   |:---------------------:|:--------:|:---------:|
| Addition       | Adds numbers or strings | +    |    3 + 5; "This is " + "cool!"|
| Subtraction, Multiplication, Division       | These do what you'd expect them to do in basic math | - , * , /    |    4 - 1; 9 * 2; 12 / 2|
| Modulo       | Finds the remainder of two numbers | %    |    11 % 3 // Returns 2 |
| Modulo       | Finds the remainder of two numbers | %    |    11 % 3 // Returns 2 |

