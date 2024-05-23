# Interview Preparation on JavaScipt

## Index

## 🚀 Topics covered from miscellaneous sources

### 🍂 What is javascript?
JavaScript is a high-level, interpreted programming language that conforms to the ECMAScript specification. JavaScript has curly-bracket syntax, dynamic typing, prototype-based object-orientation, and first-class functions.

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

- **`const`**: It is block-scoped and cannot be updated or redeclared. It is not hoisted to the top of the block. <span style="color: orange;">**Only `const` variables cannot be declared without initialization.**</span>

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