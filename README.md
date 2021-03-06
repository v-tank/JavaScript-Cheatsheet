# Cheatsheet

## Table of Contents 

**JavaScript**:
1. [Variable Declaration](#variable-declaration)
2. [Conditionals](#conditionals)
  1. [If Statements](#if-statements)
  2. [Switch Statements](#switch-statements)
3. [Loops](#loops) 
  1. [For Loops](#for-loop)
  2. [While Loops](#while-loop)
4. [Operators](#operators)
5. [Functions](#functions)

**jQuery**:
1. [Basics](#jq-basics)

*** 

<a name="variable-declaration"></a>
### 1. Variable declaration: 

  ```
  var camelCaseString = 'Some string';
  ```
  
  ```
  var camelCaseInt = 24;
  ```

  ```
  var camelCaseFloat = 2.40;
  ```

  ```
  var camelCaseBoolean = true;
  ```

  ```
  var camelCaseArray = ['Some string', 513, false, [ 1,3,2 ], { someKey: someValue }];
  ```

  ```
  var camelCaseObject = { key: value, anotherKey: anotherValue };
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

<a name="conditionals"></a>
###  2. Conditionals: 

<a name="if-statements"></a>
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

<a name="switch-statements"></a>
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

<a name="loops"></a>
### 3. Loops:

<a name="#for-loop"></a>
#### For-Loop:

  ```
  for (var iteratingVariable = <someStartingValue>; some conditional statement; some increment or decrement value) {
    // do anything written in this code block until the above condition has been met
  }
  ```

<a name="#while-loop"></a>
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

<a name="operators"></a>
### 4. Operators:

| Operator | Explanation | Symbols | Example |
|:--------:|-------------|---------|---------|
| Addition | Adds numbers or strings | `+` | `3 + 5; "This is " + "cool!"` |
| Subtraction, Multiplication, Division | These do what you'd expect them to do in basic math | `-` , `*` , `/` | `4 - 1; 9 * 2; 12 / 2` |
| Modulo | Finds the remainder of two numbers | `%` | ` 11 % 3 // Returns 2 ` |
| Assignment | Assigns a value to a variable | `=` | `var testing = 'Tank';` |
| Equality | Tests to see if two values are equal | `===` | `var test = 1; var test2 = 2; test === test2; // Returns false` |
| Not / Does-not-equal | Returns the logically opposite value of what it precedes; it turns a true into a false, etc. When it is used alongside the Equality operator, the negation operator tests whether two values are not equal. | `!`, `!==` | `var myVariable = 3; !(myVariable === 3); // The basic expression is true, but the comparison returns false because we've negated it. var myVariable = 3; myVariable !== 3; Here we are testing "is myVariable NOT equal to 3". This returns false because myVariable IS equal to 3.` |

<a name="functions"></a>
### 5. Functions:
Functions are a way to create some functionality that can be repeated multiple times in your code without rewriting the code each time. They help modularize functionality to help keep the code clean. There are 2 types of functions that are slightly different in terms of syntax as well as the behavior: 

1. Function Declaration
2. Function Expression

Declarative functions are hoisted to the top of the page when the page loads, which means that we can call the function even before declaring it in the code. As soon as the page loads, the function jumps, or 'hoists', to the top of the page, which makes it available to use throughout the page.

Expression functions are **not** hoisted to the top of the page, so one cannot call a function in the code before it has been declared.  

#### Defining functions without arguments:

1. Function Declaration (hoisted to the top of the page)
```
function greetUser() {
  console.log("Hello, friend! Welcome to the page!");
}
```
or 

2. Function Expression (not hoisted to the top unlike declarations)
```
var greeting = function() {
  console.log("Hello, friend! Welcome to the page!");
}
```

#### Defining functions that take in arguments:
```
function convertToCelsius(degF){

  // uses the argument variable `degF` to convert to Celsius
  var degC = (degF - 32) * 5 / 9;

  return degC; // returns the converted value
}
```

or 
```
var area = function(length, width) {
  return length * width; // returns the calculated area of a rectangle
}
```

#### Calling a function to use 
```
greetUser()  // calls function to greet the user without any arguments
```   

```
var result = area(20, 10)   // calls function to calculate area of a rectangle by passing in a length (20) and a width (10); will return the calculated value and store it in the 'result' variable
```

---

## jQuery

<a name="jq-basics"></a>
### 1. Basics:

#### Referencing existing elements on HTML:
If an element such as a div or a button already exists on the HTML, we can create a reference to that element using the following syntax in jQuery:
```
var someVariable = $("button");   // references a button on the page
// target a specific class or id using the $(".className") or $("#idName") syntax.
```

#### Creating a new element dynamically via jQuery:
To dynamically create a new element using jQuery, we can use the following syntax:
```
var newDiv = $("<div>");    // creates an instance of a new div; does not appear on screen yet until appended
newDiv.attr("class", "mainContent");  // adds a new class called `mainContent` to the newly created div

var existingDiv = $("div");   // creates a reference to some existing parent div on the HTML page that will hold the newDiv
existingDiv.append(newDiv);   // appends the dynamically created div to existingDiv as a child
```
