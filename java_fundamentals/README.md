# Fundamentals of Java

## Overview
Java is a high-level, robust, object-oriented, and secure programming language and platform. Originally called Oak, it was developed by James Gosling at Sun Microsystems in 1995. Today, it runs on billions of devices worldwide.

This repository covers the foundational concepts of Java programming, including syntax, data types, control flow, object-oriented principles, and arrays.

## Core Concepts

### 1. The Java Platform (JDK, JRE, JVM)
These three components form the core of the Java platform:
* **JDK (Java Development Kit):** Provides the tools necessary to write and compile Java programs.
* **JRE (Java Runtime Environment):** Provides the libraries and environment required to run Java applications.
* **JVM (Java Virtual Machine):** The engine that actually executes the compiled Java bytecode.

### 2. Java vs. C++
While both are powerful languages, they have distinct differences:
* **Platform Dependency:** C++ is platform-dependent, whereas Java is platform-independent.
* **Memory Management:** Java handles memory allocation automatically via a Garbage Collector, while C++ requires manual management (pointers, `malloc`, `new`, `delete`).
* **Features:** Java does not support multiple inheritance directly, nor does it support operator overloading or structures/unions.

### 3. Data Types
Java data types are divided into two main categories:
* **Primitive Data Types:** * *Numeric:* `byte`, `short`, `int`, `long`, `float`, `double`
    * *Non-Numeric:* `char`, `boolean`
* **Non-Primitive Data Types:** Classes, Strings, Arrays, Objects, and Interfaces.

### 4. Object-Oriented Programming (OOP)
Java organizes software as a combination of objects that incorporate both data and behavior.
* **Class:** A blueprint or template for creating objects.
* **Object:** An instance of a class, created using the `new` keyword.

### 5. Access Modifiers
Modifiers control the visibility and protection level of classes, methods, and variables:
* **`public`:** Accessible from everywhere (widest scope).
* **`protected`:** Accessible within the package and outside the package only through inheritance.
* **`default`:** Accessible only within the same package (applied when no modifier is specified).
* **`private`:** Accessible only within the class it is defined in.

### 6. Control Flow Statements
Java executes code from top to bottom, but control flow statements allow you to divert this execution:
* **Decision Making:** `if`, `if-else`, `if-else-if` ladder, `nested if`, and `switch` statements.
* **Loop Statements:** Execute instructions repeatedly based on a condition.
    * `for` loop: Used when the exact number of iterations is known.
    * `for-each` loop: Used to traverse data structures like arrays without needing to update a loop variable manually.
    * `while` loop: Used when the number of iterations is not known in advance.
    * `do-while` loop: Checks the condition at the end, ensuring the loop executes at least once.
* **Jump Statements:** Transfer execution control.
    * `break`: Exits the current loop or switch statement.
    * `continue`: Skips the rest of the current iteration and jumps to the next one.

### 7. Arrays
Arrays are objects that group multiple elements of the same data type in a single, contiguous memory block.
* **Single-Dimensional:** A linear collection of elements accessed via an index.
* **Multi-Dimensional:** An "array of arrays" used to store data in a table-like structure with rows and columns (e.g., matrices).

### 8. Types of Java Applications
Java can be used to build a variety of software:
* **Standalone Applications:** Traditional desktop software (e.g., Media players, Antivirus.
* **Web Applications:** Applications running on a server to create dynamic pages.
* **Enterprise Applications:** Distributed applications like banking systems with high security and load balancing.
* **Mobile Applications:** Apps created specifically for mobile devices.

---

## Included Code Examples

This repository includes several demonstration files to showcase the concepts mentioned above:

* **`Demojava.java`**: Demonstrates basic Java I/O using the `Scanner` class to take user input (strings and integers) and performs basic string operations (`toUpperCase`, `toLowerCase`, `length`).
* **`AccessM.java`**: Showcases Object-Oriented basics by creating a `Student` class and instantiating it. It demonstrates encapsulation using the four access modifiers (`private`, `default`, `protected`, `public`) and features a simple `for` loop.
* **`StudentManagementSystem.java`**: A comprehensive script that utilizes arrays, the `Scanner` class, an enhanced `for-each` loop, and `if-else-if` ladders to take student marks, calculate their grades, and determine the overall class average.
