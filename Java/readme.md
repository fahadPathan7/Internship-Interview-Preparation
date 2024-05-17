# Interview preparation on Java (OOP)

## Index
- [Interview preparation on Java (OOP)](#interview-preparation-on-java-oop)
  - [Index](#index)
  - [Topics covered from javatpoint](#topics-covered-from-javatpoint)
    - [🍂 what is java?](#-what-is-java)
    - [🍂 why java is OOP language?](#-why-java-is-oop-language)
    - [🍂 why java is a platform?](#-why-java-is-a-platform)
    - [🍂 what is package in java?](#-what-is-package-in-java)
    - [🍂 what is JVM?](#-what-is-jvm)
    - [🍂 what is JRE?](#-what-is-jre)
    - [🍂 what is JDK?](#-what-is-jdk)
    - [🍂 difference between object and class.](#-difference-between-object-and-class)
    - [🍂 difference between method overloading and overriding.](#-difference-between-method-overloading-and-overriding)
    - [🍂 types of variables.](#-types-of-variables)
    - [🍂 data types.](#-data-types)
    - [🍂 what is class?](#-what-is-class)
    - [🍂 what is inheritance?](#-what-is-inheritance)
    - [🍂 what is polymorphism?](#-what-is-polymorphism)
    - [🍂 what is abstraction?](#-what-is-abstraction)
    - [🍂 what is encapsulation?](#-what-is-encapsulation)
    - [🍂 what is a constructor?](#-what-is-a-constructor)
    - [🍂 what is private constructor?](#-what-is-private-constructor)
    - [🍂 why is java's main method static?](#-why-is-javas-main-method-static)
    - [🍂 what is this keyword?](#-what-is-this-keyword)
    - [🍂 what is super keyword?](#-what-is-super-keyword)
    - [🍂 what is final keyword?](#-what-is-final-keyword)
    - [🍂 what is static keyword?](#-what-is-static-keyword)
    - [🍂 what is strictft keyword?](#-what-is-strictft-keyword)
    - [🍂 why multiple inheritance is not supported in java?](#-why-multiple-inheritance-is-not-supported-in-java)
    - [🍂 why method overloading is not possible by changing the return type only?](#-why-method-overloading-is-not-possible-by-changing-the-return-type-only)
    - [🍂 can we overlaod java main() method?](#-can-we-overlaod-java-main-method)
    - [🍂 why can we not override static method?](#-why-can-we-not-override-static-method)
    - [🍂 what is instance initializer block?](#-what-is-instance-initializer-block)
    - [🍂 abstract classs in java.](#-abstract-classs-in-java)
    - [🍂 interface in java.](#-interface-in-java)
    - [🍂 difference between abstract class and interface.](#-difference-between-abstract-class-and-interface)
    - [🍂 access modifiers in java.](#-access-modifiers-in-java)
    - [🍂 java access modifiers with method overriding.](#-java-access-modifiers-with-method-overriding)
    - [🍂 object class in java.](#-object-class-in-java)
    - [🍂 object cloning in java.](#-object-cloning-in-java)
    - [🍂 wrapper class in java.](#-wrapper-class-in-java)
    - [🍂 call by value and call by reference.](#-call-by-value-and-call-by-reference)

## Topics covered from javatpoint

### 🍂 what is java?
Java is a high-level, platform-independent, object-oriented programming language. It was developed by **James Gosling** at **Sun Microsystems** in 1995. It is a general-purpose programming language that is used to develop desktop, web, and mobile applications. It is based on the **WORA (Write Once Run Anywhere)** principle. It is a **class-based** and **object-oriented** language.
<br><br>

### 🍂 why java is OOP language?
Java is an object-oriented programming language because it follows the **object-oriented programming paradigm**.

It is based on the following principles:
1. **Encapsulation**: wrapping the data (variables) and code (methods) together as a single unit.
2. **Inheritance**: acquiring the properties and behaviors of another class.
3. **Polymorphism**: performing one task by different ways.
4. **Abstraction**: hiding the implementation details and showing only the functionality to the user.
<br><br>

### 🍂 why java is a platform?
Java is a platform because it has two components:
1. **Runtime Environment:**
    - **JRE (Java Runtime Environment)**: provides the runtime environment in which Java bytecode can be executed.
    - **JVM (Java Virtual Machine)**: abstract machine that provides the runtime environment for Java bytecode.
    - **JDK (Java Development Kit)**: software development kit used to develop Java applications.
2. **API (Application Programming Interface):** provides a set of classes and interfaces that can be used to develop Java applications. e.g. `java.lang`, `java.io`, `java.util`, `java.net`.
<br><br>

### 🍂 what is package in java?
A package is a namespace that organizes a set of related classes and interfaces. It is used to prevent naming conflicts. It can be imported using the `import` keyword. It can be created using the `package` keyword. It can be accessed using the `.` operator.

example:
```java
package mypackage;
import java.util.Scanner;

class MyClass {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
    }
}
```
<br><br>

### 🍂 what is JVM?
**JVM (Java Virtual Machine)** is an abstract machine that provides the **runtime environment** in which **Java bytecode can be executed**. It enables Java programs to be run on any device or operating system that has a JVM installed. JVM is called a virtual machine because it doesn't physically exist. It is **not platform-independent**.

**Bytecode** is a highly optimized set of instructions that can be executed by the JVM. It is generated by the Java compiler and is platform-independent.
<br><br>

### 🍂 what is JRE?
JRE stands for **Java Runtime Environment**. It is the implementation of JVM. It **physically exists**. It contains a set of **libraries + other files** that JVM uses at runtime.

<img src='./images/jre.png' width=300px >
<br><br>

### 🍂 what is JDK?
JDK stands for **Java Development Kit**. It is a software development kit used to develop Java applications. It physically exists. It contains JRE + development tools.

<img src='./images/jdk.png' width=300px >
<br><br>

### 🍂 difference between object and class.
<img src='./images/obj-vs-class.png' width=700px >
<br><br>

### 🍂 difference between method overloading and overriding.
<img src='./images/overloading-vs-overriding.png' width=700px >
<br><br>

### 🍂 types of variables.
1. **Local variables**: declared inside the method.
2. **Instance variables**: declared inside the class but outside the method.
3. **Static variables**: declared with the static keyword.
<br><br>

### 🍂 data types.
1. **Primitive data types**: byte, short, int, long, float, double, char, boolean.
2. **Non-primitive data types**: String, Array, Class.

<img src='./images/datatypes.png' width=700px >
<br><br>

### 🍂 what is class?
A class is a blueprint for objects. It defines a data type that contains fields and methods. A class can be defined using the class keyword.

example:
```java
class MyClass {
    int x = 5;
    void myMethod() {
        System.out.println("Hello World");
    }
}
```
<br><br>

### 🍂 what is inheritance?
Inheritance is a mechanism in which one class acquires the properties and behaviors of another class. It represents the **IS-A relationship**.

example:
```java
class Animal {
    void eat() {
        System.out.println("eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("barking...");
    }
}
```
here, Dog is a subclass of Animal.
<br><br>

### 🍂 what is polymorphism?
Polymorphism is a mechanism in which one task is performed by different ways. It represents the **HAS-A relationship**.

1. **Compile-time polymorphism**: method overloading.
2. **Run-time polymorphism**: method overriding.

run-time polymorphism:
```java
class Animal {
    void sound() {
        System.out.println("Animal is making a sound");
    }
}

class Dog extends Animal {
    // overriding the sound method (run-time polymorphism)
    void sound() {
        System.out.println("Dog is barking");
    }
}
```

compile-time polymorphism:
```java
class Adder {
    static int add(int a, int b) {
        return a + b;
    }
    // method overloading (compile-time polymorphism)
    static double add(double a, double b) {
        return a + b;
    }
}
```
<br><br>

### 🍂 what is abstraction?
Abstraction is a process of hiding the implementation details and showing only the functionality to the user. It represents the **IS-A relationship**.

example:
```java
abstract class Animal {
    abstract void sound();
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog is barking");
    }
}
```
here, Dog is a subclass of Animal. Animal is an abstract class. Dog class must implement the sound method.
<br><br>

### 🍂 what is encapsulation?
Encapsulation is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. It represents the **HAS-A relationship**. It is achieved by declaring the class variables as private and providing public getter and setter methods to modify and view the variables.

example:
```java
class Student {
    private String name;
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
}
```
<br><br>

### 🍂 what is a constructor?
A constructor is a special type of method that is used to **initialize the object**. It is called when an **object is created**. It has the **same name** as the class and **doesn't have a return type**.

It can be of two types:
1. **Default constructor**: no-arg constructor.
2. **Parameterized constructor**: constructor with arguments.

example:
```java
class Student {
    int id;
    String name;

    // default constructor
    Student() {
        id = 1;
        name = "John";
    }

    // parameterized constructor
    Student(int i, String n) {
        id = i;
        name = n;
    }
}
```
<br><br>

### 🍂 what is private constructor?
A private constructor is a constructor that is declared with the private access modifier. It is used to **prevent the creation of objects** of the class. It is used in the **singleton design pattern**.

example:
```java
class Singleton {
    private static Singleton instance = new Singleton();
    private Singleton() {}
    public static Singleton getInstance() {
        return instance;
    }
}
```
<br><br>

### 🍂 why is java's main method static?
The main method is static because the JVM calls the main method without creating an object of the class. If it were not static, JVM would have to create an object of the class first and then call the main method which would lead to **unnecessary memory wastage**.
<br><br>

### 🍂 what is this keyword?
The this keyword is a reference variable that refers to the **current object**. It is used to refer to the current class instance variable. It is used to **differentiate between the instance variable and the local variable if they have the same name**.

example:
```java
class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
}
```
<br><br>

### 🍂 what is super keyword?
The super keyword is used to refer to the **immediate parent class object**. It is used to call the parent class method, constructor, and variable.

1. **To call the parent class method**: super.method_name().
2. **To refer to the parent class instance variable**: super.variable_name.
3. **To invoke the parent class constructor from the child class**: super().

example:
```java
class Animal {
    String color = "white";
}

class Dog extends Animal {
    String color = "black";

    void display() {
        System.out.println(color); // prints black
        System.out.println(super.color); // prints white
    }
}
```
<br><br>

### 🍂 what is final keyword?
The final keyword is used to restrict the user. It can be used with variables, methods, and classes.

1. **Final variable**: the value of the variable cannot be changed.
2. **Final method**: the method cannot be overridden.
3. **Final class**: the class cannot be inherited.

example:
```java
final class Animal {
    final int x = 10;
    final void display() {
        System.out.println("Hello");
    }
}
```
<br><br>

### 🍂 what is static keyword?
The static keyword is used to create a class-level variable or method. It can be used with variables, methods, blocks, and nested classes. With the static keyword, the variable or method belongs to the class rather than the object. It is shared among all objects of the class.

1. **Static variable**: the value of the variable is shared among all objects of the class.
2. **Static method**: the method belongs to the class rather than the object.
3. **Static block**: used to initialize the static variables.
4. **Static nested class**: a class can be made static **only if it is a nested class**.

example:
```java
class Student {
    static String college = "XYZ";

    static void change() {
        college = "ABC";
    }
}
```
<br><br>

### 🍂 what is strictft keyword?
The strictfp keyword is used to restrict the floating-point calculations to ensure portability. It can be applied to classes, interfaces, and methods. It is used to make the floating-point calculations consistent across different platforms.

example:
```java
strictfp class Test {
    strictfp void display() {
        // strictfp method
    }
}
```
<br><br>

### 🍂 why multiple inheritance is not supported in java?
Multiple inheritance is not supported in Java because it leads to the **diamond problem**. In the diamond problem, the compiler gets confused about which method to call from the parent classes. To avoid this problem, Java supports multiple inheritance through **interfaces**.
<br><br>

### 🍂 why method overloading is not possible by changing the return type only?
Method overloading is not possible by changing the return type only because the compiler cannot differentiate between the methods based on the return type. It can differentiate between the methods based on the number of arguments and the type of arguments.
<br><br>

### 🍂 can we overlaod java main() method?
Yes, we can overload the main method in Java. But the JVM calls the main method with a specific signature only: `public static void main(String[] args)`.
<br><br>

### 🍂 why can we not override static method?
We cannot override the static method because the static method belongs to the class rather than the object. It is shared among all objects of the class. **If we try to override the static method, the compiler will not give an error but it will call the method from the parent class only**.
<br><br>

### 🍂 what is instance initializer block?
The instance initializer block is used to initialize the instance data member. It is executed **before the constructor is invoked**. It is invoked **at the time of object creation each time**.

example:
```java
class A {
    int x;
    // instance initializer block
    {
        x = 10;
    }
}
```
<br><br>

### 🍂 abstract classs in java.
An abstract class is a class that is declared with the abstract keyword. It can have abstract methods and non-abstract methods. It cannot be instantiated **(cannot create objects of an abstract class)**. It can have constructors and static methods.

example:
```java
abstract class Animal {
    abstract void sound();
    void eat() {
        System.out.println("eating...");
    }
}
```
<br><br>

### 🍂 interface in java.
An interface is a reference type in Java. It is similar to a class. It is a collection of abstract methods **(100% abstract)**. A class implements an interface, thereby inheriting the abstract methods of the interface. All methods in an interface are **public and abstract** by default. It cannot have constructors and static methods. It is used to achieve multiple inheritance in Java. **All methods should be implemented in the class that implements the interface**.

example:
```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("barking...");
    }
}
```
<br><br>

### 🍂 difference between abstract class and interface.
<img src='./images/abstract-vs-interface.png' width=700px >
<br><br>

### 🍂 access modifiers in java.
There are four types of access modifiers in Java:
1. **Private**: accessible only within the class.
2. **Default**: accessible only within the package.
3. **Protected**: accessible within the package and outside the package through inheritance.
4. **Public**: accessible from anywhere.
<br><br>

### 🍂 java access modifiers with method overriding.
In method overriding, the access modifier of the overriding method **cannot be more restrictive** than the overridden method. It can be the same or less restrictive.

**restrictive order:** private > default > protected > public.

example:
```java
class Animal {
    protected void sound() {
        System.out.println("Animal is making a sound");
    }
}

class Dog extends Animal {
    // overriding the sound method
    public void sound() {
        System.out.println("Dog is barking");
    }
}
```
<br><br>

### 🍂 object class in java.
The Object class is the root class of Java. It is present in the `java.lang` package. It is the **superclass of all classes** in Java. It provides some methods that are common to all objects. Some of the methods are: `toString()`, `equals()`, `hashCode()`, `getClass()`, `clone()`, `finalize()`, `notify()`, `notifyAll()`, `wait()`.
<br><br>

### 🍂 object cloning in java.
Object cloning is a way to create an exact copy of an object. It is achieved by implementing the `Cloneable` interface and overriding the `clone()` method of the `Object` class. It is a shallow copy. To achieve a deep copy, we need to override the `clone()` method and copy the object's fields manually.

shallow copy:
```java
class Student implements Cloneable {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public Object clone() throws CloneNotSupportedException {
        return super.clone();
    }
}
```

deep copy:
```java
class Student implements Cloneable {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    @override
    public Object clone() throws CloneNotSupportedException {
        Student s = new Student(id, name);
        return s;
    }
}
```
<br><br>

### 🍂 wrapper class in java.
A wrapper class is a class that wraps the primitive data types. It provides a way to use primitive data types as objects.

example:
```java
int x = 10;
Integer y = new Integer(x); // wrapping
int z = y.intValue(); // unwrapping
```
<br><br>

### 🍂 call by value and call by reference.
In Java, arguments are passed by value. In call by value, a copy of the actual value is passed to the method. The changes made to the parameter inside the method have no effect on the actual argument. Java does not support call by reference.

call by value:
```java
class Test {
    int x = 10;

    void change(int x) {
        x = 20;
    }

    public static void main(String[] args) {
        Test t = new Test();
        t.change(t.x);
        System.out.println(t.x); // prints 10
    }
}
```
<br><br>