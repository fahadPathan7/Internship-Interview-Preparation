# Interview Preparation on Design Patterns

## Index

## 🚀 Topics covered from javatpoint

### 🍂 SOLID principles
- [Single Responsibility Principle (SRP)](#single-responsibility-principle-srp)
- [Open/Closed Principle (OCP)](#openclosed-principle-ocp)
- [Liskov Substitution Principle (LSP)](#liskov-substitution-principle-lsp)
- [Interface Segregation Principle (ISP)](#interface-segregation-principle-isp)
- [Dependency Inversion Principle (DIP)](#dependency-inversion-principle-dip)

<br><br>

- **Single Responsibility Principle (SRP)**: A class should have one, and only one, reason to change. (only one responsibility)

```java
class Employee {
    public void save() {
        // save employee
    }
    public void update() {
        // update employee
    }
    public void delete() {
        // delete employee
    }
}
```
here, the Employee class has multiple responsibilities like save, update, and delete. So, we can create separate classes for each responsibility.

```java
class Save {
    public void save() {
        // save employee
    }
}

class Update {
    public void update() {
        // update employee
    }
}

class Delete {
    public void delete() {
        // delete employee
    }
}
```

<br><br>

- **Open/Closed Principle (OCP)**: Software entities should be open for extension, but closed for modification.

```java
class Circle {
    public void draw() {
        // draw circle
    }
}

class Square {
    public void draw() {
        // draw square
    }
}
```
here, if we want to add a new shape like a rectangle, then we have to modify the existing classes. So, we can create an interface Shape and implement it in the classes.

```java
interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        // draw circle
    }
}

class Square implements Shape {
    public void draw() {
        // draw square
    }
}
```

<br><br>

- **Liskov Substitution Principle (LSP)**: Objects of a superclass shall be replaceable with objects of its subclasses without affecting the functionality of the program.

```java
class Bird {
    public void fly() {
        // fly
    }
}

class Ostrich extends Bird {
    public void fly() {
        throw new UnsupportedOperationException("Ostrich can't fly");
    }
}
```
here, the Ostrich class is a subclass of the Bird class. But, the Ostrich class can't fly. So, it violates the Liskov Substitution Principle. So, we can create a separate class for the Ostrich.

```java
class Bird {
    public void fly() {
        // fly
    }
}

class Ostrich {
    public void run() {
        // run
    }
}
```

<br><br>

- **Interface Segregation Principle (ISP)**: A client should never be forced to implement an interface that it doesn't use or clients shouldn't be forced to depend on methods they do not use.

```java
interface Worker {
    void work();
    void eat();
}

class WorkerImpl implements Worker {
    public void work() {
        // work
    }
    public void eat() {
        // WorkerImpl doesn't need this method
    }
}
```
here, the Worker interface has two methods work() and eat(). But, the WorkerImpl class doesn't need the eat() method. So, we can create separate interfaces for work and eat.

```java
interface Workable {
    void work();
}

interface Eatable {
    void eat();
}

class WorkerImpl implements Workable {
    public void work() {
        // work
    }
}
```

<br><br>

- **Dependency Inversion Principle (DIP)**: High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details. Details should depend on abstractions.

```java
class LightBulb {
    public void turnOn() {
        // turn on light
    }
    public void turnOff() {
        // turn off light
    }
}

class Switch {
    private LightBulb lightBulb = new LightBulb();
    public void switchOn() {
        lightBulb.turnOn();
    }
    public void switchOff() {
        lightBulb.turnOff();
    }
}
```
here, the Switch class is directly dependent on the LightBulb class. So, we can create an interface Switchable and implement it in the LightBulb class.

```java
interface Switchable {
    void turnOn();
    void turnOff();
}

class LightBulb implements Switchable {
    public void turnOn() {
        // turn on light
    }
    public void turnOff() {
        // turn off light
    }
}

class Switch {
    private Switchable switchable;
    public Switch(Switchable switchable) {
        this.switchable = switchable;
    }
    public void switchOn() {
        switchable.turnOn();
    }
    public void switchOff() {
        switchable.turnOff();
    }
}

class Main {
    public static void main(String[] args) {
        Switchable switchable = new LightBulb();
        Switch switch = new Switch(switchable);
        switch.switchOn();
        switch.switchOff();
    }
}
```

<br><br>

### 🍂 Types of Design Patterns.
- [Creational Design Patterns](#creational-design-patterns)
   - [Singleton Pattern](#singleton-pattern)
   - [Factory Method Pattern](#factory-method-pattern)
   - [Abstract Factory Pattern](#abstract-factory-pattern)
   - [Builder Pattern](#builder-pattern)
   - [Prototype Pattern](#prototype-pattern)
 - [Structural Design Patterns](#structural-design-patterns)
   - [Adapter Pattern](#adapter-pattern)
   - [Bridge Pattern](#bridge-pattern)
   - [Composite Pattern](#composite-pattern)
   - [Decorator Pattern](#decorator-pattern)
   - [Facade Pattern](#facade-pattern)
   - [Flyweight Pattern](#flyweight-pattern)
   - [Proxy Pattern](#proxy-pattern)
 - [Behavioral Design Patterns](#behavioral-design-patterns)
   - [Chain of Responsibility Pattern](#chain-of-responsibility-pattern)
   - [Command Pattern](#command-pattern)
   - [Interpreter Pattern](#interpreter-pattern)
   - [Iterator Pattern](#iterator-pattern)
   - [Mediator Pattern](#mediator-pattern)
   - [Memento Pattern](#memento-pattern)
   - [Observer Pattern](#observer-pattern)
   - [State Pattern](#state-pattern)
   - [Strategy Pattern](#strategy-pattern)
   - [Template Pattern](#template-pattern)
   - [Visitor Pattern](#visitor-pattern)

<br><br>

### 🍂 Creational Design Patterns

- **Singleton Pattern**: A Singleton Pattern ensures a **class has only one instance** and provides a global point of access to it.

```java
class Singleton {
    private static Singleton instance; // private static variable of the same class
    private Singleton() {} // private constructor
    public static Singleton getInstance() {
        // ensures only one instance is created
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}

class Main {
    public static void main(String[] args) {
        Singleton singleton1 = Singleton.getInstance();
        Singleton singleton2 = Singleton.getInstance();
        System.out.println(singleton1 == singleton2); // true
    }
}
```

<br><br>

- **Factory Method Pattern**: A Factory Method Pattern defines an interface for creating an object, but lets subclasses decide which class to instantiate. (creates objects without specifying the exact class to create)

```java
interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        System.out.println("Circle is drawn");
    }
}

class Square implements Shape {
    public void draw() {
        System.out.println("Square is drawn");
    }
}

class ShapeFactory {
    public Shape getShape(String shapeType) {
        if (shapeType == null) {
            return null;
        }
        if (shapeType.equalsIgnoreCase("CIRCLE")) {
            return new Circle();
        } else if (shapeType.equalsIgnoreCase("SQUARE")) {
            return new Square();
        }
        return null;
    }
}

class Main {
    public static void main(String[] args) {
        ShapeFactory shapeFactory = new ShapeFactory();
        Shape shape1 = shapeFactory.getShape("CIRCLE"); // subclass decides which class to instantiate
        shape1.draw();
        Shape shape2 = shapeFactory.getShape("SQUARE");
        shape2.draw();
    }
}
```

<br><br>

- **Abstract Factory Pattern**: An Abstract Factory Pattern provides an interface for creating **families** of related or dependent objects without specifying their concrete classes. (Abstract Factory returns the factory of classes)

```java
interface Shape {
    void draw();
}

class Circle implements Shape {
    public void draw() {
        System.out.println("Circle is drawn");
    }
}

class Square implements Shape {
    public void draw() {
        System.out.println("Square is drawn");
    }
}

interface Color {
    void fill();
}

class Red implements Color {
    public void fill() {
        System.out.println("Red color is filled");
    }
}

class Green implements Color {
    public void fill() {
        System.out.println("Green color is filled");
    }
}

// Abstract Factory returns the factory of classes
abstract class AbstractFactory {
    abstract Shape getShape(String shapeType);
    abstract Color getColor(String colorType);
}

class ShapeFactory extends AbstractFactory {
    public Shape getShape(String shapeType) {
        if (shapeType == null) {
            return null;
        }
        if (shapeType.equalsIgnoreCase("CIRCLE")) {
            return new Circle();
        } else if (shapeType.equalsIgnoreCase("SQUARE")) {
            return new Square();
        }
        return null;
    }
    public Color getColor(String colorType) {
        return null;
    }
}

class ColorFactory extends AbstractFactory {
    public Shape getShape(String shapeType) {
        return null;
    }
    public Color getColor(String colorType) {
        if (colorType == null) {
            return null;
        }
        if (colorType.equalsIgnoreCase("RED")) {
            return new Red();
        } else if (colorType.equalsIgnoreCase("GREEN")) {
            return new Green();
        }
        return null;
    }
}

class FactoryProducer {
    public static AbstractFactory getFactory(String choice) {
        if (choice.equalsIgnoreCase("SHAPE")) {
            return new ShapeFactory();
        } else if (choice.equalsIgnoreCase("COLOR")) {
            return new ColorFactory();
        }
        return null;
    }
}

class Main {
    public static void main(String[] args) {
        AbstractFactory shapeFactory = FactoryProducer.getFactory("SHAPE");
        Shape shape1 = shapeFactory.getShape("CIRCLE");
        shape1.draw();
        Shape shape2 = shapeFactory.getShape("SQUARE");
        shape2.draw();

        AbstractFactory colorFactory = FactoryProducer.getFactory("COLOR");
        Color color1 = colorFactory.getColor("RED");
        color1.fill();
        Color color2 = colorFactory.getColor("GREEN");
        color2.fill();
    }
}
```

<br><br>

- **Builder Pattern**: A Builder Pattern constructs a complex object step by step. It provides a way to construct the object such that the same construction process can create different representations.

```java
class User {
    private String firstName;
    private String lastName;
    private int age;
    private String phone;
    private String address;

    private User(UserBuilder builder) {
        this.firstName = builder.firstName;
        this.lastName = builder.lastName;
        this.age = builder.age;
        this.phone = builder.phone;
        this.address = builder.address;
    }

    static class UserBuilder {
        private String firstName;
        private String lastName;
        private int age;
        private String phone;
        private String address;

        public UserBuilder(String firstName, String lastName) {
            this.firstName = firstName;
            this.lastName = lastName;
        }

        public UserBuilder age(int age) {
            this.age = age;
            return this;
        }

        public UserBuilder phone(String phone) {
            this.phone = phone;
            return this;
        }

        public UserBuilder address(String address) {
            this.address = address;
            return this;
        }

        public User build() {
            return new User(this);
        }
    }
}

class Main {
    public static void main(String[] args) {
        User user = new User.UserBuilder("John", "Doe")
            .age(30)
            .phone("1234567890")
            .address("123, Main Street, New York, USA")
            .build();
    }
}
```

<br><br>

- **Prototype Pattern**: A Prototype Pattern creates new objects by copying an existing object, known as a prototype.

```java
abstract class Shape implements Cloneable {
    private String id;
    protected String type;

    abstract void draw();

    public String getType() {
        return type;
    }

    public String getId() {
        return id;
    }

    public void setId(String id) {
        this.id = id;
    }

    public Object clone() {
        Object clone = null;
        try {
            clone = super.clone(); // clone the object
        } catch (CloneNotSupportedException e) {
            e.printStackTrace();
        }
        return clone;
    }
}

class Circle extends Shape {
    public Circle() {
        type = "Circle";
    }

    public void draw() {
        System.out.println("Inside Circle::draw() method.");
    }
}

class Square extends Shape {
    public Square() {
        type = "Square";
    }

    public void draw() {
        System.out.println("Inside Square::draw() method.");
    }
}

class ShapeCache {
    private static Map<String, Shape> shapeMap = new HashMap<>();

    public static Shape getShape(String shapeId) {
        Shape cachedShape = shapeMap.get(shapeId);
        return (Shape) cachedShape.clone();
    }

    public static void loadCache() {
        Circle circle = new Circle();
        circle.setId("1");
        shapeMap.put(circle.getId(), circle);

        Square square = new Square();
        square.setId("2");
        shapeMap.put(square.getId(), square);
    }
}

class Main {
    public static void main(String[] args) {
        ShapeCache.loadCache();

        Shape clonedShape1 = ShapeCache.getShape("1");
        System.out.println("Shape: " + clonedShape1.getType());

        Shape clonedShape2 = ShapeCache.getShape("2");
        System.out.println("Shape: " + clonedShape2.getType());
    }
}
```