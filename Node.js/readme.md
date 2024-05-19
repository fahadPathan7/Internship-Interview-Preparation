# Interview Preparation on Node.js (Express.js)

## Index
- [Interview Preparation on Node.js (Express.js)](#interview-preparation-on-nodejs-expressjs)
  - [Index](#index)
  - [🚀 Topics covered from miscellaneous sources (Node.js)](#-topics-covered-from-miscellaneous-sources-nodejs)
    - [🍂 what is Node.js?](#-what-is-nodejs)
    - [🍂 How does Node.js work?](#-how-does-nodejs-work)
    - [🍂 How do you manage packages in your node.js project?](#-how-do-you-manage-packages-in-your-nodejs-project)
    - [🍂 How node.js is better than other frameworks most popularly used?](#-how-nodejs-is-better-than-other-frameworks-most-popularly-used)
    - [🍂 What are the advantages of using promises insted of callbacks?](#-what-are-the-advantages-of-using-promises-insted-of-callbacks)
    - [🍂 Why is node.js single-threaded?](#-why-is-nodejs-single-threaded)
    - [🍂 How many types of API functions are there in node.js?](#-how-many-types-of-api-functions-are-there-in-nodejs)
    - [🍂 What is REPL?](#-what-is-repl)
    - [🍂 What is the purpose of module.exports?](#-what-is-the-purpose-of-moduleexports)
    - [🍂 What is the purpose of require() function?](#-what-is-the-purpose-of-require-function)
    - [🍂 How does node.js overcome the problem of blocking of I/O operations?](#-how-does-nodejs-overcome-the-problem-of-blocking-of-io-operations)
    - [🍂 What is middleware?](#-what-is-middleware)
    - [🍂 Why should we separate Express app and server?](#-why-should-we-separate-express-app-and-server)
    - [🍂 What is thread pool and which library handles it in node.js?](#-what-is-thread-pool-and-which-library-handles-it-in-nodejs)
  - [🚀 Topics covered from miscellaneous sources (Express.js)](#-topics-covered-from-miscellaneous-sources-expressjs)
    - [🍂 What is express.js?](#-what-is-expressjs)
    - [🍂 What are key features of express.js?](#-what-are-key-features-of-expressjs)
    - [🍂 What are the different types of middleware in express.js?](#-what-are-the-different-types-of-middleware-in-expressjs)
    - [🍂 What is the purpose next function in express.js middleware?](#-what-is-the-purpose-next-function-in-expressjs-middleware)
    - [🍂 What is the purpose of app.use() method in express.js?](#-what-is-the-purpose-of-appuse-method-in-expressjs)
    - [🍂 How do you handle file uploads in express.js?](#-how-do-you-handle-file-uploads-in-expressjs)
    - [🍂 How do you implement pagination in express.js?](#-how-do-you-implement-pagination-in-expressjs)
    - [🍂 How do you handle CORS in express.js?](#-how-do-you-handle-cors-in-expressjs)
    - [🍂 How do you handle WebSocket connections in express.js?](#-how-do-you-handle-websocket-connections-in-expressjs)
    - [🍂 How do you handle cookies in express.js?](#-how-do-you-handle-cookies-in-expressjs)
    - [🍂 How do you handle route-specific middleware in express.js?](#-how-do-you-handle-route-specific-middleware-in-expressjs)
    - [🍂 How do you handle server-side-rendering (SSR) in express.js?](#-how-do-you-handle-server-side-rendering-ssr-in-expressjs)
    - [🍂 Difference between node.js and express.js?](#-difference-between-nodejs-and-expressjs)
    - [🍂 What is runtime environment?](#-what-is-runtime-environment)
    - [🍂 Difference between library and framework?](#-difference-between-library-and-framework)
    - [🍂 What is JWT?](#-what-is-jwt)

<br><br>

## 🚀 Topics covered from miscellaneous sources (Node.js)

### 🍂 what is Node.js?
Node.js is a **runtime environment** for executing JavaScript code. It is built on the Chrome V8 JavaScript engine. It is used for building fast and scalable **network applications**. It is **open-source and cross-platform**.

<br><br>

### 🍂 How does Node.js work?
Node.js is a **single-threaded** but **highly scalable** system that utilizes JavaScript as its scripting language. It uses **non-blocking I/O** and **event-driven** model. It is a **lightweight** and **efficient** runtime environment.

<br><br>

### 🍂 How do you manage packages in your node.js project?
We can manage packages in our Node.js project using **npm** (Node Package Manager). It is the default package manager for Node.js. We can install, update, and remove packages using npm. To maintain a list of dependencies in our project, we can use a **package.json** file.

<br><br>

### 🍂 How node.js is better than other frameworks most popularly used?
Node.js is better than other frameworks because of its **non-blocking I/O** and **event-driven** model. It is **lightweight** and **efficient**. It is **single-threaded** but **highly scalable**. It is built on the Chrome V8 JavaScript engine (which is very fast). It is **open-source and cross-platform**.

<br><br>

### 🍂 What are the advantages of using promises insted of callbacks?
Promises are better than callbacks because they avoid **callback hell** (nested callbacks). They provide a **cleaner** and **more readable** code. They provide better **error handling**. They allow us to **chain** multiple asynchronous operations. They provide better **synchronization**.

**callback hell** is a situation where we have multiple nested callbacks which makes the code difficult to read and maintain.

<br><br>

### 🍂 Why is node.js single-threaded?
Node.js was created explicitly as an experiment in **asynchronous processing**. This was to try a new theory of doing async processing on a single thread over the existing thread-based implementation of scaling via differenct frameworks.

<br><br>

### 🍂 How many types of API functions are there in node.js?
There are two types of API functions in Node.js:
1. **Asynchronous, non-blocking functions**: These functions continue to run in the background and a callback function is called once the operation is completed.
2. **Synchronous, blocking functions**: These functions block the execution of the code until the operation is completed.

<br><br>

### 🍂 What is REPL?
REPL stands for **Read-Eval-Print-Loop**. It is a simple, interactive computer programming environment that takes single user inputs, evaluates them, and returns the result to the user. Node.js comes with a built-in REPL environment.

<br><br>

### 🍂 What is the purpose of module.exports?
This is used to expose functions, objects, or variables defined in a module to be accessed by other modules. It is used to **export** a module and make it available for other modules to **require** and use.

<br><br>

### 🍂 What is the purpose of require() function?
This function is used to **import** modules defined in other files. It is used to **include** functions, objects, or variables defined in a module to be accessed by other modules.

<br><br>

### 🍂 How does node.js overcome the problem of blocking of I/O operations?
Since the node has an **event loop** that can be used to handle all the I/O operations asynchronously, it can handle multiple requests at the same time. This is how it overcomes the problem of blocking of I/O operations.

<br><br>

### 🍂 What is middleware?
Middleware is a function that has access to the request and response objects. It can execute any code, make changes to the request and the response objects, end the request-response cycle, and call the next middleware function in the stack.

<br><br>

### 🍂 Why should we separate Express app and server?
Separating the Express app and server allows us to **test** the app without starting the server. It allows us to **export** the app and use it in other files. It allows us to **run** the app in different environments (e.g., development, production). Separation ensures business logic is **separated** from the server configuration which makes the code **cleaner** and **more maintainable**.

<br><br>

### 🍂 What is thread pool and which library handles it in node.js?
Thread pool is a pool of threads that are used to execute asynchronous tasks. In Node.js, the `libuv` library handles the thread pool. It is a multi-platform support library with a focus on asynchronous I/O.

<br><br>

<hr>

## 🚀 Topics covered from miscellaneous sources (Express.js)

### 🍂 What is express.js?
Express.js is a **web application framework** for Node.js. It provides a **robust set of features** for web and mobile applications. It is **minimal** and **flexible**. It provides a **thin layer** of fundamental web application features without obscuring Node.js features.

<br><br>

### 🍂 What are key features of express.js?
1. **Middleware**: It allows us to execute code during the request-response cycle.
2. **Routing**: It allows us to define routes to handle different HTTP requests.
3. **Templating**: It allows us to render dynamic content using templates. (e.g., EJS, Pug)
4. **Error Handling**: It provides a way to handle errors in the application.
5. **Modularity**: It allows us to break the application into smaller modules.
6. **Performance**: It is fast and efficient.

<br><br>

### 🍂 What are the different types of middleware in express.js?
There are different types of middleware in Express.js:
1. **Application-level middleware**: It is used to bind application-level middleware to an instance of the `app` object. such as logging, parsing, etc.
2. **Router-level middleware**: It is used to bind middleware to an instance of `express.Router()`. such as authentication, request processing, etc.
3. **Error-handling middleware**: It is used to define error-handling middleware functions. It takes four arguments `(err, req, res, next)`. It is used to handle errors in the application.
4. **Third-party middleware**: It is used to add functionality to the Express application. such as `body-parser`, `cookie-parser`, etc.

<br><br>

### 🍂 What is the purpose next function in express.js middleware?
The `next` function is used to pass control to the next middleware function in the stack. It is used to **execute** the next middleware function. If the current middleware function does not end the request-response cycle, it must call `next()` to pass control to the next middleware function.

<br><br>

### 🍂 What is the purpose of app.use() method in express.js?
The `app.use()` method is used to **mount** middleware functions in the application. It is used to **bind** the middleware function to the application. It is used to **execute** the middleware function for every request to the server.

<br><br>

### 🍂 How do you handle file uploads in express.js?
To handle file uploads in Express.js, we can use the `multer` middleware. It is a middleware for handling `multipart/form-data`. It allows us to **upload files** to the server. We can configure `multer` to specify the **destination** and **filename** for the uploaded files.

<br><br>

### 🍂 How do you implement pagination in express.js?
To implement pagination in Express.js, we can use **query parameters** to specify the **page** and **limit** of the results. We can use the `skip()` and `limit()` methods of Mongoose to **paginate** the results. We can calculate the **total number of pages** based on the total number of records and the limit per page.

<br><br>

### 🍂 How do you handle CORS in express.js?
To handle CORS (Cross-Origin Resource Sharing) in Express.js, we can use the `cors` middleware. It is a package that can be used to enable CORS with various options. We can configure `cors` to allow or restrict access to our server from different origins. We can use it to set the **Access-Control-Allow-Origin** header in the response.

<br><br>

### 🍂 How do you handle WebSocket connections in express.js?
To handle WebSocket connections in Express.js, we can use the `ws` package. It is a simple to use, blazing fast, and thoroughly tested WebSocket client and server implementation. We can create a WebSocket server using the `ws` package and handle WebSocket connections in our Express.js application.

<br><br>

### 🍂 How do you handle cookies in express.js?
To handle cookies in Express.js, we can use the `cookie-parser` middleware. It is a middleware that parses cookies attached to the client request object. We can use it to read and write cookies in our Express.js application. We can configure `cookie-parser` to set the **cookie secret** and other options.

<br><br>

### 🍂 How do you handle route-specific middleware in express.js?
To handle route-specific middleware in Express.js, we can use the `app.use()` method with a **path** parameter. We can specify the **path** for the middleware function to be executed only for requests that match the specified path. We can use this to define middleware functions that are specific to certain routes in our application.

<br><br>

### 🍂 How do you handle server-side-rendering (SSR) in express.js?
To handle server-side rendering (SSR) in Express.js, we can use a templating engine like **EJS** or **Pug**. We can render dynamic content on the server and send the HTML response to the client. We can use the `res.render()` method to render the template with data and send the HTML response to the client.

<br><br>

### 🍂 Difference between node.js and express.js?
Node.js is a **runtime environment** for executing JavaScript code, while Express.js is a **web application framework** for Node.js. Node.js provides the **core functionality** for running JavaScript code on the server, while Express.js provides a **set of features** for building web applications. Node.js is **low-level** and **general-purpose**, while Express.js is **high-level** and **specific to web applications**.

<br><br>

### 🍂 What is runtime environment?
A runtime environment is a software environment that provides the necessary **runtime support** for executing programs. It includes the **runtime libraries**, **runtime system**, and other **supporting programs** that are required to run the program. It provides an **execution environment** for the program to run.

<br><br>

### 🍂 Difference between library and framework?
A **library** is a collection of **functions** and **classes** that can be used to perform specific tasks. It provides **reusable code** that can be used in different applications. A **framework** is a **skeleton** of an application that provides a **structure** and **guidelines** for building the application. It provides **predefined patterns** and **components** that can be used to build the application.

<br><br>

### 🍂 What is JWT?
JWT stands for **JSON Web Token**. It is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA. JWTs consist of three parts separated by dots: a header, a payload, and a signature.

<hr>