# Interview Preparation on Golang (Backend Development)

## Index
- [Interview Preparation on Golang (Backend Development)](#interview-preparation-on-golang-backend-development)
  - [Index](#index)
  - [🚀 Topics covered from w3schools](#-topics-covered-from-w3schools)
    - [🍂 what is go?](#-what-is-go)
    - [🍂 why go is used for?](#-why-go-is-used-for)
    - [🍂 Go syntax.](#-go-syntax)
    - [🍂 Go Variables types](#-go-variables-types)
    - [🍂 Declaring variables \& constants](#-declaring-variables--constants)
    - [🍂 Go Operators](#-go-operators)
    - [🍂 Go Arrays](#-go-arrays)
    - [🍂 Go Slices](#-go-slices)
    - [🍂 Go struct](#-go-struct)
    - [🍂 Go Maps](#-go-maps)
    - [🍂 Go Loops](#-go-loops)
    - [🍂 Go Functions](#-go-functions)
  - [🚀 Topics covered from other sources](#-topics-covered-from-other-sources)
    - [🍂 Why choose go over node.js for backend?](#-why-choose-go-over-nodejs-for-backend)
    - [🍂 Go Concurrency](#-go-concurrency)
    - [🍂 Go Error Handling](#-go-error-handling)
    - [🍂 Go Defer](#-go-defer)
    - [🍂 Go Panic and Recover](#-go-panic-and-recover)
    - [🍂 Go Interfaces](#-go-interfaces)
    - [🍂 Go routing](#-go-routing)
    - [🍂 Go middleware](#-go-middleware)

<br><br>

## 🚀 Topics covered from w3schools

### 🍂 what is go?
- Go is an open-source programming language that makes it easy to build simple, reliable, and efficient software.
- Go is a cross-platform language that can be used to build applications for Linux, Windows, and macOS.
- Go is syntactically similar to C, but with memory safety, garbage collection, structural typing, and CSP-style concurrency.
- Go was developed by Google in 2007.

<br><br>

### 🍂 why go is used for?
- Go is used for building web applications, command-line tools, network servers, and more.
- Go is cross-platform, which means we can write a Go program on a Windows computer and run it on a Linux server.

<br><br>

### 🍂 Go syntax.
- Package Declaration
- Import Packages
- Functions
- Statements & Comments

<br><br>

### 🍂 Go Variables types
- int
- float64, float32
- bool
- string

```go
package main

import "fmt"

func main() {
    var age int = 25
    var weight float64 = 65.5
    var isMale bool = true
    var name string = "John"
    inferredType := 25 // type inference (int)

    fmt.Println(age)
    fmt.Println(weight)
    fmt.Println(isMale)
    fmt.Println(name)
    fmt.Println(inferredType) // 25
}
```
inferred type is used when we don't specify the type of the variable. Go automatically assigns the type based on the value assigned to the variable. it can be used only inside functions.


<br><br>

### 🍂 Declaring variables & constants
- **var** keyword is used to declare variables in Go.
- **const** keyword is used to declare constants in Go.

```go
package main

import "fmt"

func main() {
    var name string = "John" // variable declaration
    fmt.Println(name)

    const age int = 25 // constant declaration
    fmt.Println(age)
}
```

<br><br>

### 🍂 Go Operators
- Arithmetic Operators (+, -, *, /, %)
- Comparison Operators (==, !=, <, >, <=, >=)
- Logical Operators (&&, ||, !)
- Bitwise Operators (&, |, ^, <<, >>)
- Assignment Operators (=, +=, -=, *=, /=, %=, <<=, >>=, &=, |=, ^=)
- Misc Operators (&, *, etc.)

<br><br>

### 🍂 Go Arrays
- An array is a collection of elements that are stored in contiguous memory locations.
- The size of an array is fixed and cannot be changed once it is declared.
- The elements of an array are accessed using an index.

```go
func main() {
    array := [5]int{10, 20, 30, 40, 50} // array declaration and initialization
    array1 := [...]int{10, 20} // array declaration without specifying the size
    var numbers [5]int // array declaration
    numbers[0] = 10
    numbers[1] = 20
    numbers[2] = 30
    numbers[3] = 40
    numbers[4] = 50

    fmt.Println(array) // [10 20 30 40 50]
    fmt.Println(array1) // [10 20]
    fmt.Println(numbers) // [10 20 30 40 50]
}
```

<br><br>

### 🍂 Go Slices
- A slice is a lightweight data structure that wraps an array and provides a more powerful interface to the elements of the array.
- The size of a slice is not fixed and can grow or shrink dynamically.
- Slices are used to represent variable-length sequences of elements.

```go
func main() {
    // slice_name := make([]type, length, capacity)
    // length: the number of elements the slice can contain
    // capacity: the number of elements the underlying array can contain
    slice := []int{10, 20, 30, 40, 50} // slice declaration and initialization
    slice1 := make([]int, 5) // slice declaration using make function. capacity is equal to length
    slice2 := make([]int, 5, 10) // slice declaration using make function with capacity

    slice1[0] = 10

    fmt.Println(slice) // [10 20 30 40 50]
    fmt.Println(slice1) // [10 0 0 0 0]
    fmt.Println(slice2) // [0 0 0 0 0]
}
```

**length vs capacity:** The length of a slice is the number of elements it contains, while the capacity of a slice is the number of elements in the underlying array starting from the first element of the slice. (capacity >= length. length means how many elements are currently in the slice, and capacity means how many elements the slice can hold.)

To understand the difference between length and capacity, consider the following example:

```go
slice := make([]int, 0, 3)
for i := 0; i < 5; i++ {
    slice = append(slice, i)
    fmt.Printf("Length: %d, Capacity: %d\n", len(slice), cap(slice))
}
```
The output of the program will be:
```go
Length: 1, Capacity: 3
Length: 2, Capacity: 3
Length: 3, Capacity: 3
Length: 4, Capacity: 6 // capacity is doubled when the length exceeds the capacity
Length: 5, Capacity: 6
```

<br><br>

### 🍂 Go struct
- A struct is a user-defined data type that groups together zero or more named values of different types.
- The fields of a struct are accessed using the dot operator.

```go
package main

import "fmt"

type Person struct {
    name string
    age int
    isMale bool
}

func main() {
    person := Person{name: "John", age: 25, isMale: true} // struct initialization
    fmt.Println(person) // {John 25 true}
    fmt.Println(person.name) // John
    fmt.Println(person.age) // 25
    fmt.Println(person.isMale) // true

    var person1 Person // struct declaration
    person1.name = "Alice"
    person1.age = 30
    person1.isMale = false
    fmt.Println(person1) // {Alice 30 false}
}
```

<br><br>

### 🍂 Go Maps
- A map is a collection of key-value pairs where each key is unique.
- Maps are used to represent unordered collections of elements.

```go
package main

import "fmt"

func main() {
    // map_name := make(map[key_type]value_type)
    // map_name := map[key_type]value_type{}
    // map_name := map[key_type]value_type{key1: value1, key2: value2, ...}
    person := map[string]int{"John": 25, "Alice": 30, "Bob": 35} // map declaration and initialization
    person1 := make(map[string]int) // map declaration using make function

    fmt.Println(person) // map[Alice:30 Bob:35 John:25]
    fmt.Println(person1) // map[]

    fmt.Println(person["John"]) // 25
    fmt.Println(person["Alice"]) // 30
    fmt.Println(person["Bob"]) // 35

    person["John"] = 40 // update value
    fmt.Println(person) // map[Alice:30 Bob:35 John:40]

    delete(person, "John") // delete key-value pair
    fmt.Println(person) // map[Alice:30 Bob:35]
}
```

<br><br>

### 🍂 Go Loops
- Go supports three types of loops: for loop, while loop, and do-while loop.

```go
package main

import "fmt"

func main() {
    // for loop
    for i := 0; i < 5; i++ {
        fmt.Println(i)
    }

    // while loop
    j := 0
    for j < 5 {
        fmt.Println(j)
        j++
    }

    // do-while loop
    k := 0
    for {
        fmt.Println(k)
        k++
        if k == 5 {
            break
        }
    }
}
```

<br><br>

### 🍂 Go Functions
- A function is a block of code that performs a specific task.
- Functions are used to break down a program into smaller, manageable pieces.
- Functions can take zero or more input parameters and return zero or more output parameters.

```go
package main

import "fmt"

func add(a int, b int) int {
    return a + b
}

func main() {
    sum := add(10, 20)
    fmt.Println(sum) // 30
}
```

<br><br>

<hr>

## 🚀 Topics covered from other sources

### 🍂 Why choose go over node.js for backend?
| Go | Node.js |
| --- | --- |
| Go is a statically typed language. | Node.js is a dynamically typed language. |
| Go is a compiled language. | Node.js is an interpreted language. |
| Go has a built-in garbage collector. | Node.js does not have a built-in garbage collector. |
| Go has a simpler syntax compared to Node.js. | Node.js has a more complex syntax. |
| Go has better performance compared to Node.js. | Node.js has lower performance compared to Go. |
| Go has better support for concurrency. | Node.js has limited support for concurrency. |
| Go is more suitable for building large-scale applications. | Node.js is more suitable for building small-scale applications. |
| Go has better error handling compared to Node.js. | Node.js has limited error handling capabilities. |
| Go is multi-threaded. | Node.js is single-threaded. |

**Static vs Dynamic Typing:** Go is a statically typed language, which means that the type of a variable is known at compile time. Node.js, on the other hand, is a dynamically typed language, which means that the type of a variable is determined at runtime.

**Compiled vs Interpreted Language:** Go is a compiled language, which means that the source code is translated into machine code before it is executed. Node.js is an interpreted language, which means that the source code is executed line by line by an interpreter.

<br><br>

### 🍂 Go Concurrency
- Go has built-in support for concurrency using **goroutines and channels**. (multi-threading)
- A goroutine is a lightweight thread of execution that runs concurrently with other goroutines.
- Channels are used to communicate between goroutines.

```go
package main

import (
    "fmt"
    "time"
)

func printNumbers() {
    for i := 1; i <= 5; i++ {
        fmt.Println(i)
        time.Sleep(1 * time.Second)
    }
}

func main() {
    go printNumbers()
    time.Sleep(6 * time.Second)
}
```
here, the `printNumbers` function is executed as a goroutine using the `go` keyword. The `main` function sleeps for 6 seconds to allow the `printNumbers` goroutine to complete its execution.

<br><br>

### 🍂 Go Error Handling
- Go uses the `error` type to represent errors.
- Functions can return an error as a second return value.
- Errors can be checked using the `if err != nil` statement.

```go
package main

import (
    "errors"
    "fmt"
)

func divide(a, b int) (int, error) {
    if b == 0 {
        return 0, errors.New("division by zero")
    }
    return a / b, nil
}

func main() {
    result, err := divide(10, 0)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Result:", result)
    }
}
```

<br><br>

### 🍂 Go Defer
- The `defer` statement is used to delay the execution of a function until the surrounding function returns.
- Deferred functions are executed in LIFO (Last In First Out) order.

```go
package main

import "fmt"

func main() {
    defer fmt.Println("World")
    fmt.Println("Hello")
}
```
here, the `World` statement is deferred until the `main` function returns. The output of the program will be:
```go
Hello
World
```

<br><br>

### 🍂 Go Panic and Recover
- The `panic` function is used to terminate the program immediately.
- The `recover` function is used to recover from a panic and resume normal execution.

```go
package main

import "fmt"

func main() {
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("Recovered:", r)
        }
    }()

    panic("Panic!")
}
```

<br><br>

### 🍂 Go Interfaces
- An interface is a collection of method signatures that a type can implement.
- Interfaces are used to define the behavior of an object.
- A type implements an interface if it provides definitions for all the methods in the interface.

```go
package main

import "fmt"

type Shape interface {
    area() float64
}

type Circle struct {
    radius float64
}

func (c Circle) area() float64 {
    return 3.14 * c.radius * c.radius
}

func printArea(s Shape) {
    fmt.Println("Area:", s.area())
}

func main() {
    circle := Circle{radius: 5}
    printArea(circle)
}
```

<br><br>

### 🍂 Go routing
- Routing is the process of determining how an application responds to a client request.
- Go provides a built-in `net/http` package for building web servers and routing HTTP requests.

```go
package main

import (
    "fmt"
    "net/http"
)

func homePage(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Welcome to the Home Page!")
}

func aboutPage(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Welcome to the About Page!")
}

func main() {
    http.HandleFunc("/", homePage)
    http.HandleFunc("/about", aboutPage)
    http.ListenAndServe(":8080", nil)
}
```

<br><br>

### 🍂 Go middleware
- Middleware is a piece of code that is executed before or after the main handler.
- Middleware is used to perform common tasks such as logging, authentication, and error handling.

```go
package main

import (
    "fmt"
    "net/http"
)

func logger(next http.Handler) http.Handler {
    return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
        fmt.Println("Logging...")
        next.ServeHTTP(w, r)
    })
}

func homePage(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Welcome to the Home Page!")
}

func main() {
    http.Handle("/", logger(http.HandlerFunc(homePage)))
    http.ListenAndServe(":8080", nil) // nil is used to use the default ServeMux
}
```

<hr>