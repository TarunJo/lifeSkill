# Object Oriented Programming (OOP)

## Introduction

Object-Oriented Programming (OOP) is like a popular way of building computer programs. It's all about making your code neat and easy to work with by using things called "objects".
This paper explains OOP in a way that's easy to understand, and it talks about the most important rules, ideas, and tricks in OOP. 
Whether you're just starting out or you're already a pro, this paper will help you make your software better.

## Core Principles of OOP

### Classes and Objects
- Classes are like templates for creating objects, which are the actual instances of those templates.
- Constructors build objects, and destructors clean them up.
- Encapsulation is like putting code in a safe box, with access rules to keep things secure.

### Interface
- It's a blueprint for classes, like a to-do list for actions they should perform.
- Interfaces only declare what methods should exist; they don't provide the details of how they work.
- Interfaces help achieve complete abstraction, making code less complicated.

### Inheritance
- Single inheritance means one class can inherit from another, while multiple inheritance allows inheriting from more than one.
- Method overriding is when a child class provides a new version of a method from the parent class.
- Superclasses are like parents, and subclasses are like their children in the code world.

### Abstraction
- Abstract classes and methods are like placeholders that must be filled in by the child classes.
- Interfaces set the rules, and classes implement the specific behaviors.
- Achieving data abstraction means hiding complex data details, focusing on what's important.

## Fundamental OOP Concepts

### Encapsulation
Encapsulation is like putting your computer code in a safe box. It means you hide some parts of your code so that others can't accidentally mess with them. 
This helps keep your code safe and working as it should. It's a bit like locking the important stuff in a secure box and only letting others access what they need.
<br>**Important Points**
- Data hiding
- Public and private access
- Benefits of encapsulation
  ```
  public class Student {
    private String name;

    public Student(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public static void main(String[] args) {
        Student student = new Student("Alice");
        System.out.println("Student Name: " + student.getName());
    }
  }

  ```

### Inheritance
Inheritance in programming is a bit like passing down traits from parents to children. 
You can create a new piece of code (a child) based on an existing piece of code (a parent) and add or change things as needed. 
It's like a way to reuse code and save time. For example, if you have a "vehicle" code, you can make a "car" code that inherits all the basic features of a vehicle but adds specific things that are unique to a car, like the number of doors. 
It's a way to build on what's already there.
<br>**Important Points**
- Code reuse
- Extending classes
- The 'is-a' relationship
  ```
  class Animal {
    public void speak() {
        // Common code for all animals.
    }
  }
  class Dog extends Animal {
    public void speak() {
        System.out.println("Woof!");
    }
  }
  class Cat extends Animal {
    public void speak() {
        System.out.println("Meow!");
    }
  ```

### Polymorphism
Polymorphism in programming is like having one word with different meanings depending on the context. 
In this context, it means that you can use the same function or method name, but it can do different things for different objects. 
It's a way to make your code flexible and adaptable. Imagine if you had a "draw" command for both a circle and a square. Even though it's the same command, it would make each shape look different. 
That's what polymorphism does in code – it allows you to use the same command in different ways depending on the situation.
<br>**Important Points**
- Flexibility in method invocation
- Method signature
- The 'has-a' relationship
  ```
  public static void animalSpeak(Animal animal) {
    animal.speak();
  }
  // Usage
  Animal dog = new Dog();
  Animal cat = new Cat();

  animalSpeak(dog);  // Outputs "Woof!"
  animalSpeak(cat);  // Outputs "Meow!"

  ```

### Abstraction
Abstraction in programming is like simplifying complex things to make them easier to work with. 
It's like using a TV remote without needing to know all the technical details of how it works inside. 
Abstraction helps you focus on the essential parts and hide the complicated stuff. 
For example, when you use a smartphone, you don't need to understand all the complex electronics inside; you can just interact with the touch screen. Abstraction is about using simple, understandable commands while hiding the inner complexities.
<br>**Important Points**
- Modeling real-world entities
- Reducing complexity
- Separation of concerns
  ```
  abstract class Shape {
    public abstract double area();
  }

  class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double area() {
        return 3.14 * radius * radius;
    }
  }

  // Usage
  Circle circle = new Circle(5);
  System.out.println("Circle area: " + circle.area());
  ```

## OOP Design Patterns

### Creational Patterns
- Singleton: It ensures that only one instance of a class is created and provides a way to access that instance.
- Factory Method: It's like a factory that creates objects without specifying their exact types, allowing flexibility in object creation.
- Abstract Factory: It's a super factory that creates other factories for creating families of related objects without specifying their classes.
- Builder: It's like an assembly line for creating complex objects, step by step, with various options.
- Prototype: It's like making copies of an existing object to create new ones, making it easy to produce similar objects.

### Structural Patterns
- Adapter: It's like a translator that allows two incompatible interfaces to work together by providing a middleman.
- Composite: It's like organizing objects into a tree structure to work with both individual objects and groups of objects seamlessly.
- Decorator: It's like adding features or behaviors to objects dynamically, without changing their core structure.
- Proxy: It's like using a stand-in or placeholder to control access to another object.
- Facade: It's like a simplified front door to a complex system, making it easier to use without dealing with its intricacies.

### Behavioral Patterns
- Observer: It's like subscribing to updates; when one thing changes, all the interested parties are automatically notified.
- Strategy: It's like having different strategies in your toolkit and choosing the right one for the job.
- Command: It's like encapsulating a request as an object, allowing you to parameterize and queue requests.
- Chain of Responsibility: It's like a relay race where different runners can handle a baton (request) until one successfully completes it.
- State: It's like changing the behavior of an object when its internal state changes, making it act differently in different situations.

## Conclusion

In simple terms, Object-Oriented Programming (OOP) is a vital part of making software today.
By grasping the main ideas, basic concepts, and smart ways of OOP, developers can create software that's easy to manage and grow. 
This paper is a helpful guide for developers who want to become OOP experts and use it well in their projects.

## References

- JavatPoint: https://www.javatpoint.com/java-oops-concepts
- Geeksforgeeks: https://www.geeksforgeeks.org/object-oriented-programming-in-cpp/
- Youtube: https://www.youtube.com/playlist?list=PL9gnSGHSqcno1G3XjUbwzXHL8_EttOuKk
- W3School: https://www.w3schools.com/java/default.asp
