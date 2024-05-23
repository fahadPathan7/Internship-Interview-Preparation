# Interview Preparation on JavaScipt

## Index
- [Interview Preparation on JavaScipt](#interview-preparation-on-javascipt)
  - [Index](#index)
  - [🚀 Topics covered from miscellaneous sources](#-topics-covered-from-miscellaneous-sources)
    - [🍂 What is javascript?](#-what-is-javascript)
    - [🍂 What is ECMAScript?](#-what-is-ecmascript)
    - [🍂 Explain the key features in ES6.](#-explain-the-key-features-in-es6)
    - [🍂 What is the difference between `null` and `undefined`?](#-what-is-the-difference-between-null-and-undefined)
    - [🍂 What is the difference between `==` and `===`?](#-what-is-the-difference-between--and-)
    - [🍂 What is the difference between `let`, `const`, and `var`?](#-what-is-the-difference-between-let-const-and-var)
    - [🍂 What is hoisting in JavaScript?](#-what-is-hoisting-in-javascript)
    - [🍂 What is a closure?](#-what-is-a-closure)
    - [🍂 What is NaN?](#-what-is-nan)
    - [🍂 What is anonymous function?](#-what-is-anonymous-function)
    - [🍂 What is \[\[\[\]\]\]?](#-what-is-)
    - [🍂 Why arrow function is needed over traditional function?](#-why-arrow-function-is-needed-over-traditional-function)
    - [🍂 Explain about this keyword.](#-explain-about-this-keyword)
    - [🍂 What is strict mode in JavaScript?](#-what-is-strict-mode-in-javascript)
    - [🍂 Is javascript a statically typed or dynamically typed?](#-is-javascript-a-statically-typed-or-dynamically-typed)
    - [🍂 What is DOM?](#-what-is-dom)
    - [🍂 What is BOM?](#-what-is-bom)
    - [🍂 What is scope in javascript?](#-what-is-scope-in-javascript)
    - [🍂 What is event bubbling and event capturing?](#-what-is-event-bubbling-and-event-capturing)
    - [🍂 What is callback and what is callback hell?](#-what-is-callback-and-what-is-callback-hell)
    - [🍂 What is a promise?](#-what-is-a-promise)
    - [🍂 What is async/await?](#-what-is-asyncawait)
    - [🍂 Explain the rest parameter.](#-explain-the-rest-parameter)
    - [🍂 Difference between Attributes and Property.](#-difference-between-attributes-and-property)

<br><br>

## 🚀 Topics covered from miscellaneous sources

### 🍂 What is javascript?
JavaScript is a high-level, interpreted programming language that conforms to the ECMAScript specification. JavaScript has curly-bracket syntax, dynamic typing, prototype-based object-orientation, and first-class functions. It is a **web scripting** language that allows us to create dynamically updating content, control multimedia, animate images, and much more.

**Interpreted**: JavaScript is an interpreted language, not a compiled language. It is executed line by line.

<br><br>

### 🍂 What is ECMAScript?
ECMAScript (European Computer Manufacturers Association Script) is a standard for scripting languages. It is a specification for a scripting language that is based on several technologies, including JavaScript. JavaScript is the most well-known implementation of ECMAScript.

<br><br>

### 🍂 Explain the key features in ES6.
- **Arrow Functions**: Arrow functions are more concise and easier to read. They are anonymous functions and do not have their own `this` context.
- **Classes**: ES6 classes are syntactic sugar over JavaScript's existing prototype-based inheritance. It is a new way to write reusable components.
- **Template Literals**: Template literals are string literals allowing embedded expressions. We can use multi-line strings and string interpolation features with them. Example: `let name = 'John'; console.log(`Hello ${name}`);`
- **Destructuring**: Destructuring allows binding using pattern matching with arrays and objects. Example: `let [a, b] = [1, 2];`
- **Default Parameters**: Default parameters allow parameters to be initialized with default values if no value or undefined is passed. Example: `function sum(a, b=1) { return a + b; }`
- **Promises**: Promises are used to handle asynchronous operations. They are a cleaner way to handle callbacks. Example: `new Promise((resolve, reject) => { resolve('Success'); });`

<br><br>

### 🍂 What is the difference between `null` and `undefined`?
- **`null`**: It is an assignment value. It can be assigned to a variable as a representation of no value. It is a primitive value. Example: `let a = null;`
- **`undefined`**: It means a variable has been declared but has not yet been assigned a value. It is a type itself. Example: `let a; console.log(a);`

<br><br>

### 🍂 What is the difference between `==` and `===`?
- **`==`**: It is used for comparison between two variables irrespective of the datatype of variable. Example: `if(2 == '2') { console.log('Equal'); }` will print 'Equal'.
- **`===`**: It is used for comparison between two variables but this will check strict type, which means it will check datatype and compare two values. Example: `if(2 === '2') { console.log('Equal'); }` will not print 'Equal'.

<br><br>

### 🍂 What is the difference between `let`, `const`, and `var`?
- **`var`**: It is function-scoped and can be redeclared and updated. It is hoisted to the top of the function. (function-scoped means it is available within the function where it is declared)

```javascript
function example() {
    var a = 10;
    if(true) {
        var a = 20; // This is the same variable
        console.log(a); // 20
    }
    console.log(a); // 20
}
```

<br><br>

- **`let`**: It is block-scoped and can be updated but not redeclared. It is not hoisted to the top of the block. (block-scoped means it is available within the block where it is declared). Inner block can have the same variable name as the outer block but it will be a different variable.

```javascript
function example() {
    let a = 10;
    if(true) {
        let a = 20; // This is a different variable
        console.log(a); // 20
    }
    console.log(a); // 10
    a = 30; // This will update the value of a to 30 in the same block
    console.log(a); // 30
}
```

<br><br>

- **`const`**: It is block-scoped and cannot be updated or redeclared. It is not hoisted to the top of the block. **Only `const` variables cannot be declared without initialization.**

```javascript
function example() {
    const a = 10;
    if(true) {
        const a = 20; // This is a different variable
        console.log(a); // 20
    }
    console.log(a); // 10
    a = 30; // This will throw an error
    const a = 30; // This will throw an error
}
```

<br><br>

### 🍂 What is hoisting in JavaScript?
Hoisting is a JavaScript mechanism where **variables and function declarations** are moved to the top of their containing scope before code execution. This means that no matter where functions and variables are declared, they are moved to the top of their scope regardless of whether their scope is global or local.

**variable hoisting:**
```javascript
console.log(a); // undefined. not ReferenceError
var a = 10;
```
it is interpreted as:
```javascript
var a;
console.log(a); // undefined
a = 10;
```

<br><br>

**function hoisting:**
```javascript
example(); // Hello
function example() {
    console.log('Hello');
}
```
it is interpreted as:
```javascript
function example() {
    console.log('Hello');
}
example(); // Hello
```

<br><br>

### 🍂 What is a closure?
A closure is a JavaScript function defined inside another function. The inner function has access to the outer function's variables and scope chain even after the outer function has finished executing. Closures are used to create private variables and to emulate the concept of classes and objects.

```javascript
function outer() {
    let a = 10;
    function inner() {
        console.log(a);
    }
    return inner;
}

let fn = outer();
fn(); // 10
```
here, the `inner` function has access to the `a` variable of the `outer` function even after the `outer` function has finished executing. The `inner` function forms a closure over the `a` variable.

<br><br>

### 🍂 What is NaN?
NaN stands for "Not-a-Number". It is a property of the global object and is returned when a mathematical operation is performed that is not a valid number. It is used to represent an error when a value is expected to be a number but is not.

```javascript
console.log(typeof NaN); // number

console.log(10 * 'a'); // NaN
console.log(Math.sqrt(-1)); // NaN
```

<br><br>

### 🍂 What is anonymous function?
An anonymous function is a function that is **defined without a name**. It is usually not accessible after its initial creation. Anonymous functions are often used as **arguments to other functions or to create closures**.

```javascript
let example = function() {
    console.log('Anonymous function');
};
example();
```

<br><br>

### 🍂 What is [[[]]]?
`[[[]]]` is a valid JavaScript syntax. It is an array containing an array containing an array. It is a nested array structure.

```javascript
let a = [[[]]];
console.log(a); // [[[]]]
```

<br><br>

### 🍂 Why arrow function is needed over traditional function?
- **Concise**: Arrow functions are more concise and easier to read.
- **No binding of `this`**: Arrow functions do not have their own `this` context. They are bound to the `this` of the enclosing scope.
- **No `arguments` object**: Arrow functions do not have an `arguments` object. The `arguments` object is not available inside arrow functions.

<br>

arguments object example:
```javascript
function example() {
    console.log(arguments);
}

example(1, 2, 3); // [1, 2, 3]

let example = () => {
    console.log(arguments); // ReferenceError: arguments is not defined
};

example(1, 2, 3);

let example = (...args) => {
    console.log(args); // [1, 2, 3]
};

example(1, 2, 3);
```

<br><br>

binding of `this` example:
```javascript
function example() {
    this.name = 'John';
    setTimeout(function() {
        console.log(this.name); // undefined (because this refers to the global object)
    }, 1000);
}
```
here, `this` in the traditional function refers to the global object. Because the traditional function has its own `this` context and that is why it is not able to access the `name` property of the `example` function (here `this` refers to the global object).

```javascript
function example() {
    this.name = 'John';
    setTimeout(() => {
        console.log(this.name); // John (because this refers to the parent function)
    }, 1000);
}
```
here, `this` in the arrow function refers to the `this` of the `example` function. Arrow functions do not have their own `this` context and that is why it is able to access the `name` property of the `example` function. (here `this` refers to the parent function).

<br><br>

### 🍂 Explain about this keyword.
The `this` keyword refers to the object it belongs to. (it refers to the immediate parent object).

It has different values depending on where it is used:
- In a method, `this` refers to the owner object.
- Alone, `this` refers to the global object.

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    fullName: function() {
        return this.firstName + ' ' + this.lastName;
    }
};
console.log(person.fullName()); // John Doe
```
here, `this` in the `fullName` method refers to the `person` object. (because the immediate parent of the `fullName` method is the `person` object and `this` refers to the immediate parent object)

```javascript
let person = {
    firstName: 'John',
    lastName: 'Doe',
    fullName: function() {
        return function() {
            return this.firstName + ' ' + this.lastName;
        };
    }
};
console.log(person.fullName()()); // undefined undefined
```
In the above example, `this` in the inner function refers to the global object. Because the inner function has its own `this` context and that is why it is not able to access the `firstName` and `lastName` properties of the `person` object. (as the immediate parent does not have `firstName` and `lastName` properties)

<br><br>

### 🍂 What is strict mode in JavaScript?
Strict mode is a way to opt into a restricted variant of JavaScript. It eliminates some JavaScript silent errors by changing them to throw errors. It fixes mistakes that make it difficult for JavaScript engines to perform optimizations. Strict mode applies to the entire script or to a function block. Strict mode helps in writing secure JavaScript code.

```javascript
function example() {
    x = 10; // This will not throw an error in normal mode.
    console.log(x); // 10
}
```

```javascript
function example() {
    'use strict';
    x = 10; // This will throw an error in strict mode.
    console.log(x); // ReferenceError: x is not defined
}
```

<br><br>

### 🍂 Is javascript a statically typed or dynamically typed?
JavaScript is a dynamically typed language. This means that the type of the variable is determined at runtime. It is not necessary to specify the type of the variable when declaring it.

```javascript
let a = 10; // Here, the type of a is number
a = 'Hello'; // Here, the type of a is string
```

<br><br>

### 🍂 What is DOM?
The Document Object Model (DOM) is a programming interface for web documents. It represents the structure of the document as a tree of nodes. The DOM is used to interact with the HTML document. It provides a structured representation of the document and defines methods that allow access to the document's content. The DOM is used to manipulate the document's structure, style, and content.

<br><br>

### 🍂 What is BOM?
The Browser Object Model (BOM) is a programming interface for web browsers. It provides objects and methods that allow JavaScript to interact with the browser. The BOM is not standardized and varies between browsers. It includes objects like `window`, `document`, `location`, `history`, `navigator`, `screen`, etc. The BOM is used to interact with the browser window and its components.

<br><br>

### 🍂 What is scope in javascript?
- **Global Scope**: Variables declared outside a function are in the global scope. They can be accessed from any function in the program.
- **Local Scope**: Variables declared inside a function are in the local scope. They can only be accessed from within the function.

<br>

global scope example:
```javascript
let a = 10; // a is global
function example() {
    console.log(a); // 10
}
console.log(a); // 10
```
here, `a` is global and is accessible throughout the program.

<br><br>

local scope example:
```javascript
function example() {
    let a = 10; // a is local to the example function
    console.log(a); // 10
}
console.log(a); // ReferenceError: a is not defined
```
here, `a` is local to the `example` function and is not accessible outside the function.

<br><br>

### 🍂 What is event bubbling and event capturing?
- **Event Bubbling**: In event bubbling, the event is first captured and handled by the innermost element and then propagated to the outer elements.

```html
<div onclick="console.log('div')">
    <button onclick="console.log('button')">Click me</button>
</div>
```
When the button is clicked, the event is first captured by the button and then propagated to the div.

<br><br>

- **Event Capturing**: In event capturing, the event is first captured and handled by the outermost element and then propagated to the inner elements.

```html
<div onclick="console.log('div')" capture>
    <button onclick="console.log('button')">Click me</button>
</div>
```
When the button is clicked, the event is first captured by the div and then propagated to the button. The `capture` attribute is used to enable event capturing.

<br><br>

### 🍂 What is callback and what is callback hell?
A callback is a function passed as an argument to another function. It is executed after the completion of a task. Callbacks are used to handle asynchronous operations in JavaScript.

```javascript
function example(callback) {
    setTimeout(() => {
        callback();
    }, 1000);
}

function callback() {
    console.log('Callback executed');
}

example(callback);
```
here, the `callback` function is passed as an argument to the `example` function and is executed after the completion of the task.

<br><br>

Callback hell is a situation where multiple nested callbacks are used in asynchronous operations. It makes the code difficult to read and maintain.

```javascript
function example(callback) {
    setTimeout(() => {
        callback(() => {
            setTimeout(() => {
                callback(() => {
                    setTimeout(() => {
                        callback();
                    }, 1000);
                });
            }, 1000);
        });
    }, 1000);
}
```

<br><br>

### 🍂 What is a promise?
A promise is an object that represents the eventual completion or failure of an asynchronous operation. It is used to handle asynchronous operations in JavaScript. Promises are cleaner and easier to read than callbacks.

```javascript
let promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Success'); // The operation is successful. .then method will be called.
    }, 1000);
});

// .then method is used to handle the success case
promise.then((result) => {
    console.log(result); // Success
});

// .catch method is used to handle the error case
promise.catch((error) => {
    console.log(error); // Error
});
```
here, the `promise` object represents the completion of an asynchronous operation. The `then` method is used to handle the success case.

it is equivalent to:
```javascript
// all together
new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Success');
    }, 1000);
}).then((result) => {
    console.log(result); // Success
}).catch((error) => {
    console.log(error); // Error
});
```

<br><br>

### 🍂 What is async/await?
Async/await is a modern way to handle asynchronous operations in JavaScript. It is built on top of promises and provides a cleaner and more readable syntax.

```javascript
async function example() {
    let result = await new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve('Success');
        }, 1000);
    });
    console.log(result); // Success
}

example();
```
here, the `await` keyword is used to wait for the promise to resolve (await ensures the promise is resolved before proceeding further. makes the code synchronous). The `async` keyword is used to define an asynchronous function. If we don't use `await`, the promise will be resolved in the background and the code will continue executing.

<br><br>

### 🍂 Explain the rest parameter.
The rest parameter allows a function to accept an indefinite number of arguments as an array. It is denoted by three dots `...` followed by the parameter name.

```javascript
function example(...args) {
    console.log(args);
}

example(1, 2, 3, 4, 5); // [1, 2, 3, 4, 5]

example('a', 'b', 'c'); // ['a', 'b', 'c']
```
here, the `args` parameter is a rest parameter that accepts an indefinite number of arguments as an array.

valid rest parameter syntax:
```javascript
function example(a, b, ...args) {
    console.log(a); // 1
    console.log(b); // 2
    console.log(args); // [3, 4, 5]
}

example(1, 2, 3, 4, 5);
```

invalid rest parameter syntax:
```javascript
// rest parameter should be the last parameter
function example(...args, a, b) {
    console.log(args);
    console.log(a);
    console.log(b);
}

example(1, 2, 3, 4, 5);
```

<br><br>

### 🍂 Difference between Attributes and Property.
- **Attributes**: Attributes are defined in the HTML code. They are used to initialize the DOM properties. They are defined in the start tag of an element. They are **case-insensitive**.

```html
<input id="123" type="text" value="Hello">
```
here, `id`, `type`, and `value` are attributes.

<br><br>

- **Properties**: Properties are defined in the DOM. They are used to access and manipulate the DOM elements. They are defined in the DOM object. They are **case-sensitive**.

```javascript
let input = document.getElementById('123');
console.log(input.value); // Hello
console.log(input.type); // text
```
here, `value` and `type` are properties. They are accessed using the DOM object.

<hr>