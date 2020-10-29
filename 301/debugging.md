# The Call Stack and Debugging

## The Call Stack defined on MDN

- A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

```
function greeting() {
   // [1] Some codes here
   sayHi();
   // [2] Some codes here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();

// [3] Some codes here
```

## Understanding the JavaScript Call Stack

- The call stack is primarily used for function invocation. Since the call stack is single, function execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

- A call stack is a data structure that uses the Last In, First Out principle to temporarily store and manage function invocation

- A stack overflow occurs when there is a recursive function without an exit point. The browser has a maximum stack call that it can accomodate before throwing a stack error

## JavaScript Error Messages

- Reference Errors
  - As simple as when you try to use a variable that is not yet declared you get this type of error

- Syntax Errors
  - This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse

- Range Errors
  - Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up

- Type Errors
  - This type of error shows up when the types you are trying to use or access are incompatible, like accessing a property in an undefined type of variable

- A `try…catch` which would make an error be thrown but not “uncaught” so we can send it to an error log to be checked later and send a fallback to the function so that our code continues without problems