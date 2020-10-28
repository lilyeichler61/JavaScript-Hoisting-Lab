# Hoisting

## Objectives
+ Explain what hoisting is
+ Explain why hoisting is important to remember

## What Is Hoisting

JavaScript has a well-intentioned trick that can often lead to trouble (and nowadays, even when the trick is used well, it can make code less readable). Here's the gist:

``` javascript
// When we declare and assign a variable with `var`

var myVariable = 1;

// JavaScript actually treats it as a separate declaration and assignment:

var myVariable;
myVariable = 1;

// Here's the thing: JavaScript *hoists* variables like this to the _top_ of the file.
// So if we have a long file like this

var doSomethingComplicated = function() {
  // complicated stuff happening in here...
  // takes
  // a
  // lot
  // of
  // lines
  // of
  // code
}

var myVariable = 1;


// JavaScript actually interprets the file like

var doSomethingComplicated, myVariable;

doSomethingComplicated = function() {
  // ...
}

myVariable = 1
```

We call this process **hoisting**. For all intents and purposes, hoisting applies primarily to variables declared with `var` and to function declarations. Variables declared with `let` and `const` are _technically_ hoisted, but they cannot be referenced until they're assigned. 

## Instructions

Make sure you run the tests in `test/hoisting-test.js`. You'll be coding your solutions in `hoisting.js`. You'll find a bunch of pre-written broken code. Your job is to fix the code to pass the tests.

+ Use your knowledge of variable hoisting to get the function `callMe` to return `"maybe"`.

+ Use your function hoisting expertise to fix the function `thisIsCrazy` to `console.log` the string `"hey!!!"`.

+ Fix the code inside the function `sayMyName` to get the function to print out `"Kristin"` to the console.
