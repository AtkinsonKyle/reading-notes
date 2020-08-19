# Daily Reading 10
## Javascript
<hr>

### Chapter 10 - Debugging
#### Things To Know
- Debugging is the process of finding errors. It involves deduction
- Theconsole helps narrow down where the error is coming from so you can find the exact error
- Javascript has several types of errors. Each has its own error object, which can tell you its line number and give a description of the error
- Try, catch, finally statements can help if you know you may get an error. Use them to give users helpful feedback
- The Javascript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks the new function on top of the current task
- If a Javascript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.
<br>

#### Types of Errors
- SyntaxError
- ReferenceError
- URIError
- EvalError
- TypeError
- RangeError
- NaN
<br>

#### Exceptions
- Try: Execute this code
- Catch: If there's an exception execute this code
- Finally: This code always runs