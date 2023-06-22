# JS Interview Question and Ans

## ***Day 1*** 
 ---
## Q1 Difference between “ == “ and “ === “ operators.
### Ans-
      1. The "==" operator performs type coercion,    which means it   tries to convert the operands to a common type before making the comparison. For example, if you compare a string and a number using "==" like "10" == 10, it will try to convert the string to a number and then compare the values. In this case, it would return true because the string "10" can be converted to the number 10.

     2. On the other hand, the "===" operator does not perform type coercion. It compares both the value and the type of the operands directly. So, "10" === 10 would return false because the string "10" is not of the same type as the number 10.
---
## Q2- What are the differences between var, let and const?
### var - 
    1. Redeclare and reinitilized
    2. Global scope and Function Scope
    3. Hoisting
    4. Used before introduce ES6
### let
    1. not Redeclare and reinitilized
    2. no Hoisting
    3. Block scope, Global Scope
    4. TDZ
    5. introduce in ES6
### const
    1. not Redeclare and Not reinitilized 
    2. no Hoisting
    3. Block scope, Global Scope
    4. TDZ
    5. introduce in ES6
---
## Type of Scope
    1. Global Scope
    2. Function Scope
    3. Block Scope
    4. 
## Q3. Hoisting -
### Ans-
    Hoisting is the js mechanism where var and function declaration are moved to top of their scope before code execution.
    1. function Hoisting
    2. var keyword Hoisting
   Examples----

   
    console.log(a);
    var a = 10;

    Abc();
    function Abc(){
    console.log("Section!!!");
    }

## Q4. What is a Temporal Dead Zone (TDZ)?
    - when trying to acceess a variable before it's decleration with let and const keyword it throws a reference Error.
    - introduce to imporve the code quality by detecting & preventing to use variable.
## Q5. What is meant by first class functions?
    1. Assign a function to a variable is first class function.
   
    2. The ability of functions to be treated as values.
   
    3. passed as arguments to other functions, and returned as values from other functions.
--- 
## Q6 . Pure Function - 
    A pure function in JavaScript is a function that returns the same result if the same arguments(input) are passed in the function.

    Example----

    function Sum(a, b){
    return a * b;
    }
    Sum(10, 20)
    Sum(20, 20)
    Sum(20, 30)
---

## ***Day 2*** 
---
## Q7- What is execution context?
### Ans- 
For Synchronous JS

    1.GEC :It includes all the variables and functions declared in the global scope.

    2.Function Execution Context
    3.Memory Allocation
    4. Code Execution

For Asynchronous JS
    
    1.Event Loop
    2.Callback Queue 
    3.Call stack
---
## Q8- What is an event loop and call stack?
### Ans-
Call Stack:

    The call stack is a data structure that keeps track of function calls in the execution context. It follows the Last-In-First-Out (LIFO) principle, meaning that the last function pushed into the stack is the first one to be executed. When a function is called, it is pushed onto the stack, and when it completes, it is popped off the stack. This allows JavaScript to keep track of function calls and their execution order.

Event Loop:
    
    The event loop is a mechanism in JavaScript that handles asynchronous operations and ensures non-blocking behavior. JavaScript is single-threaded, meaning it can only execute one piece of code at a time. However, it can perform non-blocking operations such as fetching data from an API or waiting for a timer to complete without freezing the entire program.
 The event loop works by continuously checking if the call stack is empty. If the call stack is empty, it checks if there are any pending tasks or events in the event queue. If there are, it pushes the corresponding callbacks or event handlers onto the call stack for execution. This allows JavaScript to handle asynchronous operations and callbacks in an ordered and efficient manner.

 ---   

 ## Q9-What is creation phase and execution phase?
 ### Ans-
     Creation Phase: 
     
    During this phase, JavaScript sets up the environment for code execution by creating the Variable Object, setting up the Scope Chain, and determining the value of 'this'. It also performs hoisting by moving function declarations and variable declarations to the top of their respective scopes.

Execution Phase: 
     
     In this phase, JavaScript executes the code line by line, performing variable assignments, function invocations, expression evaluations, and control flow operations.
     
---
## Q9- What is the spread operator?
### Ans- 
     - Spread operator allows us to destructure the non-primitive datatype like object and array to access elemnets individually.
    - The spread operator is a feature in JavaScript that allows an iterable (such as an array or a string) to be expanded into individual elements. The spread operator is denoted by three dots (...).
    - The JavaScript spread operator ( ... ) allows us to quickly copy all or part of an existing array or object into another array or object.
---
## Q10- What is use of setTimeout?
    - it is used to delay the output with given time.
    - The setTimeout() method sets a timer which executes a function or specified piece of code once the timer expires.
## Q11-  What is setInterval?
    - They are going to excute the code after given time peroid.
  ---
## Q12-  What are callbacks?
    - A function that can pass inside another function as an argument.
    - A callback is a function that passed as an argument to another function.
  
  ---
## Q13-  Callback Hell
    - Callback Hell is essentially nested callbacks stacked below one another forming a pyramid structure.
---
## Q14-  Difference between undefined vs not defined vs NaN?
1. undefine - It represents a value that is declared but has not been assigned a value or does not exist.

Example-

     var x;
     console.log(x); // Output: undefined

2. not define -
    It refers to a variable or identifier that has not been declared or does not exist within the current scope.

 Example:

    console.log(y); // Output: ReferenceError: y is not defined

        
3. NaN - Not a Number

Example:

     console.log(0 / 0); // Output: NaN
---

## ***Day 3*** 

## What are promises and why do we need them?
    - Promises are a feature in JavaScript that help handle asynchronous operations. They represent the eventual completion or failure of an -     - asynchronous task and allow you to write asynchronous code in a more readable and manageable way.

    - Here are a few reasons why we need promises:

1. Improved Readability: Promises provide a more structured and readable approach to asynchronous programming compared to callback-based code. They allow you to chain multiple asynchronous operations together, making the code flow more linear and easier to understand.

2. Error Handling: Promises provide built-in error handling capabilities. They allow you to attach a `.catch()` callback to handle any errors that occur during the execution of asynchronous operations. This simplifies the error-handling process and allows you to centralize error handling logic.

3. Avoid Callback Hell: Promises help avoid the problem of callback hell, which occurs when dealing with multiple nested callbacks. Promises allow you to chain asynchronous operations together using `.then()` callbacks, creating a more readable and manageable code structure.

4. Asynchronous Control Flow: Promises provide control over the flow of asynchronous operations. They allow you to define dependencies between multiple asynchronous tasks, ensuring that one task executes only after another has completed successfully.

5. Compatibility: Promises are supported in modern JavaScript environments, making them widely compatible across different platforms and browsers. They are now a standard part of the JavaScript language and are often used in conjunction with other asynchronous features like `async/await`.

Overall, promises provide a more elegant and structured approach to asynchronous programming in JavaScript, making code easier to read, write, and maintain. They streamline error handling and control flow, leading to more robust and manageable asynchronous code.

## What is promise chaining

  - Promise chaining is a technique used to sequentially execute multiple asynchronous operations that depend on each other. It allows you to 
  - chain -together multiple promises, where each promise represents an asynchronous task, and the result of one promise is used as input for the - next -promise in the chain.

   - In promise chaining, you can use the `.then()` method to attach a callback function to a promise. This callback function receives the 
   - resolved -value of the previous promise and returns a new promise. By returning a new promise, you can chain another `.then()` method to it, and so on.

   - Here's an example of promise chaining:

    ```javascript
     Examples----
     function fetchUser() {
     return new Promise(function(resolve, reject) {
      setTimeout(function() {
      resolve({ id: 1, name: 'John Doe' });
      }, 1000);
     });
    }

    function fetchPosts(userId) {
     return new Promise(function(resolve, reject) {
       setTimeout(function() {
         if (userId === 1) {
        resolve(['Post 1', 'Post 2', 'Post 3']);
         } else {
          reject('User not found');
         }
       }, 1000);
     });
    }

    fetchUser()
    .then(function(user) {
    console.log('User:', user);
    return fetchPosts(user.id);
     })
     .then(function(posts) {
    console.log('Posts:', posts);
     })
     .catch(function(error) {
    console.log('Error:', error);
    });



## What is the DOM?
    - The DOM (Document Object Model) is a programming interface provided by web browsers that represents the structure of an HTML or XML document - as a tree-like structure. It defines the way in which web pages are structured and how they can be manipulated and interacted with using - - - programming languages like JavaScript.


## What are closures? Give an example of closure
  - Closures are a combination of a function and the lexical environment within which that function was declared. They allow a function to retain 
  - access to variables from its outer scope even after the outer function has finished executing.
     ```javascript
    Examples----
    function outerFunction() {
    var outerVariable = 'Hello';

    function innerFunction() {
     var innerVariable = 'World';
    console.log(outerVariable + ' ' + innerVariable);
    }

    return innerFunction;
   }

    var closure = outerFunction();
    closure(); // Output: Hello World

    ----

   




##  How many operators do we have in JS ?
  - JavaScript has various operators that allow you to perform different operations on values. Here's an overview of the different types of
  - operators in JavaScript:

1. Arithmetic Operators: Used for performing mathematical calculations, such as addition (+), subtraction (-), multiplication (*), division (/), modulo (%), increment (++), and decrement (--).

2. Assignment Operators: Used to assign values to variables, including simple assignment (=), compound assignment with arithmetic operators (+=, -=, *=, /=, %=), and others (e.g., **= for exponentiation).

3. Comparison Operators: Used to compare values and return a Boolean result, including equal to (==), not equal to (!=), strict equal to (===), strict not equal to (!==), greater than (>), less than (<), greater than or equal to (>=), and less than or equal to (<=).

4. Logical Operators: Used to perform logical operations and return a Boolean result, including logical AND (&&), logical OR (||), and logical NOT (!).

5. Bitwise Operators: Used to perform bitwise operations on binary representations of numbers, including bitwise AND (&), bitwise OR (|), bitwise XOR (^), bitwise NOT (~), left shift (<<), right shift (>>), and unsigned right shift (>>>).

6. Unary Operators: Used to operate on a single operand, including unary plus (+), unary minus (-), prefix increment (++), prefix decrement (--), logical NOT (!), bitwise NOT (~), typeof, and delete.

7. Ternary Operator: The only ternary operator in JavaScript is the conditional operator (?:), which provides a shorthand way of writing if-else statements.

8. String Operators: The plus (+) operator is used for concatenating strings together.

9. Type Operators: Used to determine the type of a value, including typeof and instanceof.

10. Comma Operator: The comma operator (,) is used to evaluate multiple expressions and return the result of the last expression.

## What are objects in javascript?

  -In JavaScript, objects are one of the fundamental data types and are used to represent real-world entities, concepts, or structures. They are
  - collections of key-value pairs, where each value can be of any data type, including other objects.
    
     ```javascript
    Example----
     var person = {
    name: 'John Doe',
    age: 30,
    email: 'johndoe@example.com',
    sayHello: function() {
    console.log('Hello!');
    }
    };
    

    


## ***Day 4*** 
