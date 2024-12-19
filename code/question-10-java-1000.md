# Top 1000 Java Interview Question & Answers

## Java Basics

### 1. **Difference between JDK and JRE:**

- **JDK (Java Development Kit):**  
  The JDK is a complete development kit used to develop Java applications. It includes the **JRE** (Java Runtime Environment), which is necessary to run Java applications, along with additional tools and libraries for developing and debugging Java programs. Some key components of the JDK are:
  - Java compiler (`javac`)
  - Debugger
  - Javadoc
  - Other development utilities

- **JRE (Java Runtime Environment):**  
  The JRE is a subset of the JDK and is used to run Java applications. It provides the libraries and other resources needed for Java applications to execute but does **not** include development tools like the compiler. It consists of:
  - JVM (Java Virtual Machine)
  - Java class libraries
  - Java supporting files

In summary:
- JDK is for **developers** (it includes JRE and tools for development).
- JRE is for **running** Java programs (it includes JVM and class libraries).

### 2. **What is Java Virtual Machine (JVM)?**

The **Java Virtual Machine (JVM)** is a part of the Java Runtime Environment (JRE) that executes Java bytecode. It acts as an interpreter and provides an environment in which Java programs can be run. The JVM is platform-independent, meaning Java programs can run on any operating system or hardware architecture, provided the JVM is available for that platform.

JVM performs the following tasks:
- Loads the compiled Java bytecode (class files).
- Verifies bytecode for security and correctness.
- Executes the bytecode, converting it into machine code using Just-In-Time (JIT) compilation.
- Manages memory (via garbage collection).

### 3. **Different Types of Memory Areas Allocated by JVM:**

The JVM allocates several memory areas for managing the execution of Java programs. These include:

- **Method Area:**  
  Stores class structures (metadata), method data, and static variables shared among all instances of a class.

- **Heap:**  
  This is the runtime memory pool where Java objects are allocated. The heap is managed by the JVM's garbage collector, which automatically reclaims memory when objects are no longer in use.

- **Stack:**  
  Each thread in a Java program has its own stack. It stores local variables, method calls, and partial results of methods being executed. The stack follows a Last-In-First-Out (LIFO) structure.

- **PC Register (Program Counter):**  
  The program counter stores the address of the current executing instruction in the method being invoked.

- **Native Method Stack:**  
  This memory area is used for native methods (methods written in languages like C or C++) that the JVM can call from Java programs.

### 4. **What is JIT Compiler?**

**JIT (Just-In-Time) Compiler** is a component of the JVM that improves the performance of Java applications by compiling bytecode into native machine code **at runtime**, rather than interpreting it. 

- The JVM first loads the bytecode and interprets it. If certain code is executed frequently, the JIT compiler compiles that code into machine language and stores it for future use. This process speeds up the execution of the program.
  
- JIT compilation occurs only when the code is executed, meaning it optimizes the performance dynamically based on actual usage patterns.

### 5. **How Java Platform is Different from Other Platforms?**

Java is considered a **platform-independent** language, and its platform has several key differences from other programming platforms:

- **Write Once, Run Anywhere:**  
  Java code is compiled into bytecode, which can run on any platform that has a compatible JVM. This is in contrast to languages like C or C++, where code must be compiled specifically for each target platform.

- **Platform Independence:**  
  Java uses the JVM to abstract away platform-specific details, allowing the same Java program to run on different operating systems (Windows, Linux, macOS) without modification.

- **Automatic Memory Management (Garbage Collection):**  
  Java handles memory management through garbage collection, freeing developers from the complexities of manual memory allocation and deallocation, as seen in languages like C/C++.

- **Security Features:**  
  Java has built-in security mechanisms, such as bytecode verification and runtime security checks, making it less susceptible to certain types of vulnerabilities that are common in other languages.

- **Rich API (Application Programming Interface):**  
  Java provides a comprehensive set of libraries for various tasks (I/O, networking, GUI, etc.), which makes Java applications more versatile and easier to develop compared to other platforms.

  ### 6. **Why People Say That Java is 'Write Once and Run Anywhere' Language?**

  Java is often referred to as a **"write once, run anywhere"** language because of its platform-independent nature. This means that once a Java program is written and compiled, it can run on any device or operating system without modification. The key to this feature lies in Java's use of the **Java Virtual Machine (JVM)**. 
  
  - Java programs are compiled into **bytecode** (not native machine code).
  - This bytecode is executed by the JVM, which is available for various platforms like Windows, macOS, Linux, etc.
  - The JVM acts as an intermediary between the compiled Java code and the underlying hardware, ensuring that the program works the same way on any platform that has the appropriate JVM.
  
  So, as long as there is a JVM for a specific platform, a Java program can run on that platform, which is why it's called "write once, run anywhere."
  
  ### 7. **How Does ClassLoader Work in Java?**
  
  A **ClassLoader** in Java is responsible for dynamically loading Java classes into memory at runtime. It loads the `.class` files (compiled bytecode) from different sources (disk, network, etc.) and makes them available for use in the program.
  
  Java ClassLoader works as follows:
  
  1. **Bootstrap ClassLoader:**  
     This is the parent class loader, and it loads core Java classes from the JDK's libraries (like `java.lang.*`). It’s built into the JVM.
  
  2. **Extension ClassLoader:**  
     It loads classes from the extension libraries, typically found in the `lib/ext` directory of the JDK.
  
  3. **System/Application ClassLoader:**  
     This loader loads classes from the classpath, which is a list of locations (directories or JAR files) where Java classes are stored. This is the default loader used for user-defined classes.
  
  4. **Custom ClassLoader:**  
     Java allows creating custom class loaders by extending the `ClassLoader` class. These can be used to load classes from non-standard locations (e.g., databases, networks, etc.).
  
  The ClassLoader hierarchy is hierarchical in nature, meaning that each loader has a parent loader (except the Bootstrap ClassLoader). If a class is not found by the current loader, it delegates the request to the parent loader.
  
  ### 8. **Do You Think 'main' Used for Main Method is a Keyword in Java?**
  
  No, **`main`** is **not a keyword** in Java. It is simply an identifier used to define the entry point of a Java program. The signature of the `main` method is always:
  
  ```java
  public static void main(String[] args)
  ```
  
  - **`public`** is an access modifier, which means the method can be accessed from anywhere.
  - **`static`** means that the method can be called without creating an instance of the class.
  - **`void`** means the method doesn't return any value.
  - **`String[] args`** is the parameter for passing command-line arguments to the program.
  
  Since `main` is not a keyword, you could technically name another method as `main`, but it wouldn’t serve as the entry point for your application unless it's the method signature used as the starting point for Java programs.
  
  ### 9. **Can We Write Main Method as Public Void Static Instead of Public Static Void?**
  
  No, **`public static void main(String[] args)`** is the correct signature for the main method in Java, and the order of the keywords is important:
  
  - **`public`** must come before **`static`**, and **`static`** must come before **`void`**.
  - **`public static void`** is the proper order because:
    - **`public`**: It specifies the access level.
    - **`static`**: It allows the method to be called without creating an instance of the class.
    - **`void`**: It signifies the method does not return any value.
  
  The Java language follows specific syntax rules, and changing the order would lead to a compilation error.
  
  ### 10. **In Java, if We Do Not Specify Any Value for Local Variables, What Will Be the Default Value of the Local Variables?**
  
  In Java, **local variables** (variables declared within a method or block) **do not have default values**. If a local variable is not explicitly initialized before it is used, the Java compiler will throw a **compilation error**. This is done to avoid undefined behavior due to uninitialized variables.
  
  For example:
  
  ```java
  public void example() {
      int x;  // Local variable x is declared but not initialized
      System.out.println(x);  // Error: variable x might not have been initialized
  }
  ```
  
  In contrast, **instance variables** (fields) and **class variables** (static fields) are automatically initialized with default values:
  - **Numeric types** (`int`, `float`, `double`) are initialized to `0`.
  - **Boolean** is initialized to `false`.
  - **Reference types** (objects) are initialized to `null`.
  
### 11. **What Will Be the Value of the String Array of Arguments in Main Method If We Run a Java Class Without Passing Any Arguments?**

If you run a Java program without passing any command-line arguments, the **`String[] args`** parameter in the `main` method will be an empty array.

For example, consider the following code:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Number of arguments: " + args.length);
    }
}
```

If you run this program without passing any arguments, the output will be:

```
Number of arguments: 0
```

This is because the `args` array is empty (`args.length` will be `0`). The array is not `null`; it is an empty array with a length of 0. You can check if there are arguments by checking `args.length`.

### 12. **What is the Difference Between byte and char Data Types in Java?**

The **`byte`** and **`char`** data types in Java are both used to represent simple values, but they differ in their purpose, range, and usage:

#### 1. **Size and Range:**
- **`byte`:**
  - Size: 1 byte (8 bits).
  - Range: -128 to 127 (signed).
  - It is used to store small integer values and is particularly useful when working with raw binary data, such as in file I/O or networking.

- **`char`:**
  - Size: 2 bytes (16 bits).
  - Range: 0 to 65,535 (unsigned).
  - It is used to represent single Unicode characters. The `char` type in Java is designed to store characters in the Unicode character set, which supports a wide range of characters from different languages and symbols.

#### 2. **Usage:**
- **`byte`:**
  - Used to store small integers or raw binary data (e.g., when working with byte arrays).
  - Can be used in arithmetic calculations but is primarily intended for memory efficiency when you need to store small values.

- **`char`:**
  - Used specifically to represent a single character in text. For example, it could represent letters, digits, or special symbols.
  - It is often used in text processing, such as when manipulating individual characters in a string or working with character encoding.

#### 3. **Example:**
```java
public class DataTypesExample {
    public static void main(String[] args) {
        byte b = 100;  // valid byte value
        char c = 'A';  // valid char value, represents the character 'A'
        
        System.out.println("Byte value: " + b);  // Output: Byte value: 100
        System.out.println("Char value: " + c);  // Output: Char value: A
    }
}
```

- In this example, `b` stores a byte value, and `c` stores a character value. The `byte` type can hold a small integer, whereas the `char` type is used to represent a Unicode character.

#### 4. **Key Differences Summary:**

| Feature           | `byte`                         | `char`                        |
|-------------------|--------------------------------|-------------------------------|
| **Size**          | 1 byte (8 bits)                | 2 bytes (16 bits)             |
| **Range**         | -128 to 127 (signed)           | 0 to 65,535 (unsigned)        |
| **Use Case**      | Stores small integers or binary data | Stores single characters (Unicode) |
| **Default Value** | 0                              | '\u0000' (null character)     |

In conclusion:
- **`byte`** is used for small integer values (from -128 to 127), while **`char`** is used for representing characters (such as letters or symbols) using Unicode.

## OOPS in Java

### 13. **What Are the Main Principles of Object-Oriented Programming (OOP)?**

Object-Oriented Programming (OOP) is a programming paradigm that uses objects and classes to structure code. The main principles of OOP are:

1. **Encapsulation:**
   - The concept of hiding the internal details of an object and exposing only the necessary functionalities. It is achieved using **access modifiers** (like `private`, `protected`, and `public`).
   - For example, an object can have private fields, and you can access or modify those fields through public getter and setter methods.

2. **Abstraction:**
   - Abstraction involves hiding the complex implementation details and showing only the essential features of an object.
   - This allows programmers to focus on high-level functionality without worrying about the specifics. Abstract classes and interfaces in Java are used to implement abstraction.

3. **Inheritance:**
   - Inheritance allows a new class (subclass) to inherit properties and behaviors (methods) from an existing class (superclass). This helps to promote reusability and hierarchical relationships.
   - In Java, inheritance is implemented using the `extends` keyword.

4. **Polymorphism:**
   - Polymorphism allows objects to be treated as instances of their parent class, enabling one interface to be used for different data types. This is achieved through **method overriding** (runtime polymorphism) and **method overloading** (compile-time polymorphism).
   - For example, different objects can respond to the same method call in different ways, depending on their actual class.

### 14. **What is the Difference Between Object-Oriented Programming Language and Object-Based Programming Language?**

The main difference between **Object-Oriented Programming (OOP)** languages and **Object-Based Programming** languages lies in their features and capabilities:

- **Object-Oriented Programming Language:**
  - Fully supports all the principles of OOP: **Encapsulation, Abstraction, Inheritance, and Polymorphism**.
  - Java, C++, Python, and C# are examples of OOP languages. These languages allow creating objects, classes, inheritance, method overriding, and dynamic polymorphism.

- **Object-Based Programming Language:**
  - Supports some features of OOP, such as **encapsulation** and **abstraction**, but **does not fully support inheritance** and **polymorphism**.
  - Examples of object-based languages are JavaScript (in earlier versions) and VBScript. While they allow creating objects, they do not support inheritance in the traditional OOP sense.

In short, **Object-Oriented** languages fully embrace the four main principles of OOP, whereas **Object-Based** languages support only some of these principles, like encapsulation, but lack full inheritance and polymorphism features.

### 15. **In Java, What is the Default Value of an Object Reference Defined as an Instance Variable in an Object?**

In Java, the **default value** of an object reference (instance variable) is `null`. This means that if an object reference is not explicitly initialized, it will point to `null` until a new object is assigned to it.

For example:

```java
public class Person {
    String name; // default value is null
}

public class Test {
    public static void main(String[] args) {
        Person p = new Person();
        System.out.println(p.name); // Output will be null
    }
}
```

Here, `p.name` will be `null` because it was not explicitly initialized.

### 16. **Why Do We Need a Constructor in Java?**

A **constructor** in Java is a special method that is used to initialize objects when they are created. The constructor's primary purpose is to set initial values for the object’s fields or perform any setup necessary when an object is created.

Key reasons for needing a constructor:
1. **Initialization:** It allows initializing an object with specific values when it is created, ensuring the object is in a valid state right from the start.
2. **Object Creation:** It is invoked automatically when an object is created using the `new` keyword, so you don't have to manually assign values to each field after the object is created.
3. **Overloading:** Java supports constructor overloading, which allows creating objects with different initializations based on the number and types of arguments passed.

Example:
```java
public class Car {
    String model;
    int year;

    // Constructor
    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car("Toyota", 2020); // Constructor initializes the object
        System.out.println(car.model); // Output: Toyota
    }
}
```

### 17. **Why Do We Need a Default Constructor in Java Classes?**

A **default constructor** is a constructor provided by Java when no constructor is explicitly defined by the programmer. It has no parameters and initializes the object with default values (such as `0` for integers, `null` for object references, etc.).

The need for a default constructor arises from the following reasons:
1. **Automatic Initialization:** If no constructor is defined in a class, the Java compiler automatically provides a default constructor. This is useful when you want to create an object without passing any arguments.
2. **Flexibility in Object Creation:** The default constructor enables the creation of objects without needing to provide specific initialization values. For example, when objects are created in a collection or when deserialized from a file.
3. **Constructor Overloading:** Even if you define constructors with parameters, having a default constructor allows you to create objects without specifying any initial values.
4. **Superclass Constructor:** If a class extends another class, and the superclass has a default constructor, the subclass can call the superclass's default constructor automatically.

Example:
```java
public class Car {
    String model;
    int year;

    // Default constructor
    public Car() {
        model = "Unknown";
        year = 0;
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car(); // Default constructor initializes fields to default values
        System.out.println(car.model); // Output: Unknown
    }
}
```
### 18. **What is the Value Returned by Constructor in Java?**

In Java, a **constructor** does not return a value. Unlike methods, which return a specific type of value (such as `int`, `String`, or `void`), constructors are special methods used to initialize objects and **do not have a return type**. The constructor is implicitly called when an object is created using the `new` keyword and is used to set the initial state of the object.

For example:

```java
public class Person {
    String name;
    
    // Constructor
    public Person(String name) {
        this.name = name;
    }
    
    public static void main(String[] args) {
        Person p = new Person("Alice");  // Constructor is called, no return value
    }
}
```

In this example, the constructor **does not return anything**. It simply initializes the `name` field of the `Person` object. Therefore, constructors **cannot** have a return type, not even `void`.

### 19. **Can We Inherit a Constructor?**

No, **constructors cannot be inherited** in Java. Constructors are not inherited because they are used to initialize the object at the time of its creation, and each class has its own specific initialization requirements.

However, a subclass can call a constructor of its superclass using the **`super()`** keyword. This allows the subclass to invoke the parent class constructor and initialize the fields inherited from the parent class. The constructor itself, though, is not inherited.

For example:

```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();  // Calling the superclass constructor
        System.out.println("Dog Constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();  // Output: Animal Constructor
                              //         Dog Constructor
    }
}
```

In this example, the `Dog` class does **not inherit** the constructor of `Animal`, but it calls it using `super()`. The constructor of the subclass `Dog` must explicitly invoke the superclass constructor, either implicitly or using `super()`.

### 20. **Why Constructors Cannot Be `final`, `static`, or `abstract` in Java?**

In Java, constructors cannot be **`final`**, **`static`**, or **`abstract`** for the following reasons:

1. **`final` Constructor:**
   - A **`final`** method cannot be overridden by subclasses. However, constructors are not inherited, and they are specific to the class in which they are defined. Therefore, making a constructor `final` serves no purpose because constructors are never inherited, and there is no need to prevent them from being overridden.
   - Additionally, since constructors are already unique to their class and can’t be overridden (unlike methods), making them `final` is redundant.

2. **`static` Constructor:**
   - **`static`** methods belong to the class rather than to any particular instance. Constructors, on the other hand, are used to create and initialize objects, and they are inherently tied to an instance of the class.
   - Since constructors are meant to initialize an instance of the class, they cannot be **static**, because static methods are for class-level functionality and do not operate on individual instances of a class.

3. **`abstract` Constructor:**
   - **`abstract`** methods are meant to be overridden by subclasses, but constructors cannot be overridden by subclasses. A constructor is meant to initialize an object, and thus it always has to be called when creating an instance of a class. Making a constructor `abstract` would be illogical because there would be no implementation to invoke when the class is instantiated.
   - Therefore, **constructors cannot be abstract**, as they are not supposed to have an abstract method signature (i.e., no body for a constructor).

In summary:
- **`final`** constructors are unnecessary, as constructors are not inherited.
- **`static`** constructors would conflict with the instance-specific nature of constructors.
- **`abstract`** constructors don’t make sense because constructors are used to create objects, and abstract methods cannot be directly invoked.


## Inheritance

### 21. **What is the Purpose of the 'this' Keyword in Java?**

In Java, the **`this`** keyword is a reference to the current object instance of the class. It is commonly used to refer to instance variables and methods of the current object, especially when there is a conflict between instance variables and method parameters (having the same name). The `this` keyword helps distinguish between the two.

Here are the main uses of the `this` keyword in Java:

1. **Referring to instance variables:**
   - When the local variable or method parameter has the same name as an instance variable, `this` is used to refer to the instance variable.

   Example:
   ```java
   class Person {
       String name;
       
       // Constructor with parameter 'name'
       Person(String name) {
           this.name = name; // 'this.name' refers to the instance variable, 'name' refers to the parameter
       }
   }
   ```

2. **Calling instance methods:**
   - `this` can be used to call the current object's method. Though optional, it can help avoid ambiguity when method names are overloaded.

   Example:
   ```java
   class Example {
       void display() {
           System.out.println("Displaying...");
       }
       
       void callDisplay() {
           this.display(); // Explicitly using 'this' to call the method
       }
   }
   ```

3. **Passing the current object to another method:**
   - `this` can be used to pass the current instance of the class to another method.

   Example:
   ```java
   class Example {
       void show(Example obj) {
           System.out.println("Showing object");
       }

       void callShow() {
           this.show(this); // Passing the current object to the 'show' method
       }
   }
   ```

4. **Constructor chaining:**
   - In a constructor, `this()` can be used to call another constructor in the same class (constructor overloading).

   Example:
   ```java
   class Person {
       String name;
       int age;
       
       // Constructor with two parameters
       Person(String name, int age) {
           this.name = name;
           this.age = age;
       }
       
       // Constructor with one parameter
       Person(String name) {
           this(name, 0); // Calls the constructor with two parameters
       }
   }
   ```

### 22. **Explain the Concept of Inheritance?**

**Inheritance** is one of the core principles of **Object-Oriented Programming (OOP)**. It allows a class to inherit properties and methods from another class. The class that inherits the properties and behaviors is called the **subclass** or **child class**, and the class that is inherited from is called the **superclass** or **parent class**.

Key features of inheritance:
- **Reusability:** A subclass can reuse the code and functionality of the parent class without needing to rewrite it.
- **Extensibility:** A subclass can extend the behavior of the parent class by adding new methods or overriding existing ones.
- **Hierarchy:** Inheritance models a hierarchical relationship between classes.

**Example:**
```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Inherited method from Animal class
        dog.bark(); // Dog's own method
    }
}
```
Here, `Dog` inherits the `eat()` method from the `Animal` class, and it can also have its own methods like `bark()`.

### 23. **Which Class in Java is the Superclass of Every Other Class?**

The **`Object`** class is the **superclass** of every other class in Java. All classes in Java, either directly or indirectly, inherit from the `Object` class. This class provides several important methods that are inherited by all Java classes, including:
- `toString()`: Returns a string representation of the object.
- `equals()`: Compares the object with another object for equality.
- `hashCode()`: Returns a hash code value for the object.
- `clone()`: Creates and returns a copy of the object.

For example, even if a class doesn't explicitly extend `Object`, it still implicitly does:

```java
class MyClass {
    // This class implicitly extends Object
}
```

### 24. **Why Does Java Not Support Multiple Inheritance?**

Java does not support **multiple inheritance** (i.e., a class cannot inherit from more than one class) due to several reasons, primarily to avoid complexity and ambiguity. Here are the key reasons:

1. **Ambiguity in method inheritance:**
   - If a class inherits from two or more classes that have methods with the same name, it would create ambiguity about which method to inherit and call.
   - This is known as the **diamond problem**, which occurs when two parent classes have a method with the same signature, and the subclass inherits both.

2. **Simplifying the design:**
   - Multiple inheritance can lead to complex and error-prone code. By avoiding it, Java simplifies its object model and reduces potential issues related to inheritance.

3. **Alternative using interfaces:**
   - Java allows a class to implement multiple interfaces. This is a safer and cleaner way to achieve similar functionality as multiple inheritance, without the ambiguity problem.
   
   Example:
   ```java
   interface A {
       void methodA();
   }

   interface B {
       void methodB();
   }

   class C implements A, B {
       public void methodA() {
           System.out.println("Method A");
       }

       public void methodB() {
           System.out.println("Method B");
       }
   }
   ```

Here, class `C` can implement both interfaces `A` and `B`, allowing it to inherit multiple behaviors but without the complications of multiple inheritance.

### 25. **In OOPS, What is Meant by Composition?**

**Composition** is a design principle in Object-Oriented Programming where one class contains an instance of another class, implying a "has-a" relationship between the two classes. It is a type of **association** where the composed class (also called the container class) includes references to objects of other classes as part of its state.

The key feature of composition is that the contained object (the component) is typically created and destroyed along with the container object. Composition is preferred over inheritance when the relationship between classes is not hierarchical, but rather a "part-of" or "has-a" relationship.

### Example of Composition:
```java
class Engine {
    void start() {
        System.out.println("Engine started");
    }
}

class Car {
    Engine engine; // Composition: Car has an Engine
    
    Car() {
        engine = new Engine(); // Car creates its own Engine
    }

    void startCar() {
        engine.start(); // Car uses Engine's functionality
        System.out.println("Car is running");
    }
}

public class Main {
    public static void main(String[] args) {
        Car car = new Car();
        car.startCar(); // Engine started \n Car is running
    }
}
```

In this example, a `Car` "has-a" `Engine`. The `Engine` is created inside the `Car` class constructor and is part of the `Car`'s state. When the `Car` is destroyed, the `Engine` is also destroyed, as it is tightly bound to the `Car`.

### 26. **How Aggregation and Composition Are Different Concepts?**

**Aggregation** and **Composition** are both types of associations in Object-Oriented Programming (OOP) that describe relationships between objects. However, they differ in terms of strength and dependency between the objects.

1. **Aggregation (Has-A relationship):**
   - Aggregation represents a **"whole-part"** relationship where the "whole" object can exist independently of its "part".
   - In aggregation, the **lifetime** of the contained object (part) is not dependent on the containing object (whole). That is, the part can exist even if the whole object is destroyed.
   - It is a **looser** relationship, and the objects can exist separately.
   
   Example:
   ```java
   class Department {
       String name;
   }

   class Employee {
       Department department;  // Aggregation: Employee "has" a Department
   }
   ```
   In this example, an `Employee` has a `Department`, but the `Department` can exist without the `Employee`.

2. **Composition (Strong Has-A relationship):**
   - Composition is a **stronger** form of aggregation. It also represents a "whole-part" relationship, but in this case, the "part" cannot exist without the "whole".
   - If the **whole** object is destroyed, the **part** object will also be destroyed.
   - It is a **tighter** relationship than aggregation.

   Example:
   ```java
   class Engine {
       void start() {
           System.out.println("Engine started");
       }
   }

   class Car {
       Engine engine;  // Composition: Car "has" an Engine
       
       Car() {
           engine = new Engine(); // Engine is part of Car
       }
   }
   ```
   Here, a `Car` "has" an `Engine`. If the `Car` is destroyed, the `Engine` is also destroyed.

### 27. **Why Are There No Pointers in Java?**

Java does not support **pointers** for several reasons, primarily focused on simplifying memory management, improving security, and enhancing code stability:

1. **Memory Safety:** Pointers can cause **undefined behavior**, such as accessing memory locations that are not valid or modifying memory incorrectly. This can lead to **segmentation faults** or **memory corruption**. By removing pointers, Java avoids these risks.
   
2. **Automatic Garbage Collection:** Java uses **automatic memory management** via **garbage collection**, which means the system automatically frees memory when objects are no longer in use. This eliminates the need for developers to manually manage memory using pointers, reducing the risk of memory leaks and dangling references.
   
3. **Security:** Pointers can be a source of **security vulnerabilities**, allowing direct access to memory locations. Without pointers, Java code is **more secure** and less prone to exploits that may arise from direct memory manipulation.
   
4. **Simplicity:** Pointers can make code complex and hard to maintain. Java avoids pointers to make the language easier to understand and work with, especially for beginner programmers.

### 28. **If There Are No Pointers in Java, Then Why Do We Get NullPointerException?**

In Java, there are no **explicit pointers**, but there are **references** to objects. When you create an object, you are working with **references** to memory locations, not direct pointers. A **NullPointerException (NPE)** occurs when you try to use a reference that is **null**, which means it does not point to any valid object in memory.

Even though Java doesn't expose pointers to the programmer, the internal workings of the JVM still involve pointers for memory management. However, Java abstracts this mechanism and prevents direct access to memory through pointers. A **NullPointerException** occurs when:

1. You attempt to call a method on a **null reference**.
2. You try to access or modify a field of a **null reference**.
3. You try to use an array or collection that has not been initialized.

Example:
```java
String str = null;
str.length(); // Throws NullPointerException
```

Here, `str` is a reference variable, but it doesn't point to any actual object, and hence calling `str.length()` results in a `NullPointerException`.

### 29. **What is the Purpose of the 'super' Keyword in Java?**

The **`super`** keyword in Java is used to refer to the **superclass** (parent class) of the current object. It is primarily used in the following scenarios:

1. **Accessing superclass methods:**
   - You can use `super` to call a method in the superclass, especially if the method is overridden in the subclass.
   
   Example:
   ```java
   class Animal {
       void sound() {
           System.out.println("Animal sound");
       }
   }
   
   class Dog extends Animal {
       void sound() {
           super.sound();  // Calls the superclass method
           System.out.println("Bark");
       }
   }
   ```

2. **Accessing superclass constructors:**
   - You can use `super()` to call a constructor of the superclass.
   
   Example:
   ```java
   class Animal {
       Animal(String name) {
           System.out.println("Animal name: " + name);
       }
   }
   
   class Dog extends Animal {
       Dog() {
           super("Dog");  // Calls the superclass constructor
       }
   }
   ```

3. **Accessing superclass fields:**
   - If a subclass has a field with the same name as a field in the superclass, you can use `super` to differentiate between the two.
   
   Example:
   ```java
   class Animal {
       String name = "Animal";
   }
   
   class Dog extends Animal {
       String name = "Dog";
       
       void display() {
           System.out.println(super.name); // Accesses 'name' from Animal class
       }
   }
   ```

### 30. **Is it Possible to Use `this()` and `super()` Both in the Same Constructor?**

No, it is **not possible** to use both **`this()`** and **`super()`** in the **same constructor**. The reason is that `this()` and `super()` are used to invoke constructors, and a constructor can only call **one** other constructor (either from the same class or from the superclass), not both.

- `this()` is used to call another constructor within the **same class**.
- `super()` is used to call a constructor from the **superclass**.

A constructor can either call another constructor in the same class using `this()` or call a constructor from the superclass using `super()`, but it cannot do both in a single constructor.

Example:
```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super();  // Calls the constructor of the superclass (Animal)
        System.out.println("Dog Constructor");
    }
}
```
In this example, `Dog` can use `super()` to call the constructor of `Animal`, but it cannot also use `this()` to call another constructor in `Dog`.

### 31. **What is the Meaning of Object Cloning in Java?**

**Object cloning** in Java refers to creating an exact copy of an object. This is done using the `clone()` method, which is defined in the `Object` class. By calling `clone()`, a new object is created with the same field values as the original object. It is commonly used to create a duplicate of an object, preserving its state.

To allow cloning, a class must implement the **`Cloneable`** interface. If a class does not implement this interface, calling `clone()` will result in a **`CloneNotSupportedException`**.

Key points about cloning:
- **Shallow cloning:** The clone method performs a **shallow copy**, meaning it copies the object's fields but does not clone objects that are referenced by the fields (i.e., references are copied).
- **Deep cloning:** A deep copy duplicates the entire object graph, including all objects that are referenced by the original object.

Example:
```java
class Person implements Cloneable {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone();
    }
}

public class Main {
    public static void main(String[] args) throws CloneNotSupportedException {
        Person p1 = new Person("Alice", 30);
        Person p2 = (Person) p1.clone();  // Cloning the object

        System.out.println(p1.name);  // Output: Alice
        System.out.println(p2.name);  // Output: Alice
    }
}
```

## Static

### 32. **In Java, Why Do We Use Static Variables?**

In Java, **static variables** are used when we want to store data that is common to all instances of a class. These variables are shared across all objects of the class, rather than having a separate copy for each instance. The value of a static variable is the same for every instance, and it can be accessed without creating an object of the class.

Key points about static variables:
1. **Shared Across All Instances:** A static variable is shared among all instances of a class. If one instance changes the value of a static variable, the change will be reflected in all other instances.
2. **Class-level Variable:** Static variables belong to the class rather than to any specific object. You can access them using the class name or through an instance, though accessing via the class name is preferred.

Example:
```java
class Counter {
    static int count = 0;  // Static variable

    Counter() {
        count++;  // Increment the count for every new object
    }

    void displayCount() {
        System.out.println("Count: " + count);
    }
}

public class Main {
    public static void main(String[] args) {
        Counter c1 = new Counter();
        Counter c2 = new Counter();
        c1.displayCount();  // Output: Count: 2
        c2.displayCount();  // Output: Count: 2
    }
}
```
In this example, the `count` variable is shared among all `Counter` objects, so both `c1` and `c2` show the same value of `count` (2).

### 33. **Why It Is Not a Good Practice to Create Static Variables in Java?**

While static variables have their uses, they should be used with caution for the following reasons:

1. **Global State Management:**
   - Static variables are shared across all instances of a class, which means their values are effectively **global**. This can lead to unexpected behavior and make it difficult to track changes in the state of an object, especially in large applications with multiple classes interacting.

2. **Testing and Maintainability:**
   - Static variables can make unit testing more difficult because they introduce a shared state across tests. This can lead to test failures if the static variables are not properly reset between tests.
   - Static variables can make code less modular and harder to maintain, as changes to a static variable may have wide-reaching effects across the application.

3. **Concurrency Issues:**
   - Static variables can cause concurrency problems in multi-threaded environments. Since they are shared among all threads, multiple threads accessing and modifying a static variable simultaneously can lead to **data inconsistencies** unless proper synchronization is used.

4. **Memory Management:**
   - Static variables are tied to the class itself, not instances. As a result, they remain in memory for the entire lifecycle of the application. This can lead to **memory leaks** if they hold references to large objects or resources that are no longer needed.

### 34. **What Is the Purpose of Static Method in Java?**

**Static methods** are used when we want to perform an operation that is related to the class itself rather than to specific instances of the class. They are part of the class itself, so they can be called without creating an object of the class.

Key points:
1. **No Object Required:** Static methods can be called using the class name, and you don't need to instantiate the class to use them.
2. **Cannot Access Instance Members:** Static methods cannot access non-static instance variables or instance methods. They can only directly access other static variables and methods.
3. **Common Utility Methods:** Static methods are often used for utility functions that don't depend on the state of individual objects, such as math calculations or factory methods.

Example:
```java
class MathUtils {
    static int add(int a, int b) {
        return a + b;
    }

    static int multiply(int a, int b) {
        return a * b;
    }
}

public class Main {
    public static void main(String[] args) {
        int sum = MathUtils.add(5, 3);   // Calling static method
        int product = MathUtils.multiply(4, 6); // Calling static method
        System.out.println("Sum: " + sum);    // Output: Sum: 8
        System.out.println("Product: " + product); // Output: Product: 24
    }
}
```
In this example, `add` and `multiply` are static methods, so they are called directly on the class `MathUtils` without needing to create an instance.

### 35. **Why Do We Mark the Main Method as Static in Java?**

The **`main`** method in Java is marked as static so that it can be called by the Java Virtual Machine (JVM) without creating an instance of the class. When the program starts, the JVM needs to know where to begin executing the code. The static `main` method serves as the entry point for the program.

Key reasons:
1. **No Object Required:** The `main` method is static so that it can be called without creating an instance of the class. The JVM calls `main` directly when the program starts.
2. **Consistency:** The `main` method serves as the standard starting point for every Java application. Since the JVM does not create objects until the program starts running, it cannot invoke non-static methods without an object.
3. **Execution Context:** By making `main` static, the JVM ensures that the method can be invoked with no need for instance variables or constructors. The static context allows the program to start immediately.

Example:
```java
public class MyClass {
    public static void main(String[] args) {
        System.out.println("Hello, world!");  // Entry point for the program
    }
}
```
In this example, `main` is static, so the JVM can call it directly to start the execution of the program.

### 36. **In What Scenario Do We Use a Static Block?**

A **static block** (also known as a static initializer) is used for **initializing static variables** or performing **one-time setup** when the class is loaded by the JVM. It is executed once, when the class is loaded into memory, before any object is created or static methods are called.

Common use cases for static blocks:
1. **Initialization of Static Variables:** Static blocks are often used to initialize static variables with complex logic or values that cannot be initialized directly.
2. **Logging or Configuration Setup:** Static blocks can be used for one-time setup, such as configuring logging or setting up connections to external resources like databases.
3. **Handling Exceptions in Static Initialization:** You can use a static block to perform setup that might throw exceptions. This allows you to handle exceptions in the initialization process.

Example:
```java
class MyClass {
    static int num;
    
    // Static block to initialize static variable
    static {
        num = 10;
        System.out.println("Static block executed: num = " + num);
    }
    
    public static void main(String[] args) {
        System.out.println("Main method executed: num = " + num);
    }
}
```
Output:
```
Static block executed: num = 10
Main method executed: num = 10
```
In this example, the static block is executed before the `main` method, and it initializes the static variable `num`. This block runs only once when the class is loaded into memory.

### Summary:
- **Static Variables:** Shared across all instances, used for class-level data.
- **Static Methods:** Used for class-related operations that don't require object state.
- **Static Block:** Used for one-time initialization when the class is loaded.
- **Main Method:** Static, as it needs to be called by the JVM to start the program without requiring an instance of the class.

### 37. **Is it Possible to Execute a Program Without Defining a `main()` Method?**

In Java, the **`main()`** method is the entry point for a standalone application. However, there are certain scenarios where a Java program can be executed without explicitly defining a `main()` method:

1. **Using a Java Application Server (e.g., in Web or Enterprise Applications):**
   - In web applications (like those developed using servlets) or enterprise applications (like those developed with EJBs or Spring frameworks), the `main()` method is not required because the server itself takes care of the program's startup and execution flow. These programs are typically started by the application server, which invokes the necessary class and methods.
   
   Example: In a servlet-based web application, the container (like Tomcat) manages the application's lifecycle, and no `main()` method is needed in the `Servlet` class.

2. **Using a Framework with Dependency Injection (e.g., Spring):**
   - In modern frameworks like **Spring**, the framework's runtime environment can take control of starting the program. The `main()` method might still be present in the main application class to bootstrap the Spring container, but the real logic is typically handled by the framework using annotations and configuration files.

3. **JAR Files with Web Start or Applets (Deprecated in Some Cases):**
   - Java Applets and Web Start applications used to have different entry points (not `main()`), but this approach has been deprecated and is no longer recommended for modern Java development.

In most cases, however, for simple Java applications or when running code directly via the command line, the `main()` method is required.

### 38. **What Happens When Static Modifier Is Not Mentioned in the Signature of the `main()` Method?**

If the **`static`** modifier is omitted from the signature of the `main()` method, the program will not run correctly. The Java Virtual Machine (JVM) specifically looks for a **static** `main()` method to start the execution of a Java program. Without the static modifier, the JVM will not be able to call the method without creating an instance of the class, which is not possible at the program's entry point.

For example:
```java
class HelloWorld {
    public void main(String[] args) {  // No static modifier
        System.out.println("Hello, World!");
    }
}

public class Main {
    public static void main(String[] args) {
        HelloWorld hw = new HelloWorld();
        hw.main(args);  // You would need to manually create an instance and call main()
    }
}
```
In this case, the program would fail to start automatically because the JVM would not recognize the `main()` method as the entry point. You would have to manually create an instance and call the method.

**Error Example:**
```
Exception in thread "main" java.lang.NoSuchMethodError: main
```

### 39. **What Is the Difference Between Static Method and Instance Method in Java?**

**Static Methods** and **Instance Methods** differ in several ways related to how they are invoked and how they interact with class and instance data.

1. **Static Method:**
   - **Belongs to the class**: A static method is associated with the class itself, rather than with any specific instance of the class.
   - **No access to instance members**: Static methods cannot directly access instance variables or instance methods (non-static members) of the class. They can only access other static members.
   - **Can be called without an object**: Static methods can be called directly using the class name or through an object, but calling them via the class name is the recommended way.
   - **Common use cases**: They are often used for utility functions, operations that don’t require any instance-specific data, or class-level behavior.

   Example:
   ```java
   class MathUtils {
       static int add(int a, int b) {  // Static method
           return a + b;
       }
   }

   public class Main {
       public static void main(String[] args) {
           int result = MathUtils.add(5, 3);  // Calling static method without creating an object
           System.out.println(result);  // Output: 8
       }
   }
   ```

2. **Instance Method:**
   - **Belongs to an instance of the class**: An instance method is associated with a specific object (instance) of the class.
   - **Access to both static and instance members**: Instance methods can access both static and non-static (instance) variables and methods.
   - **Requires an object to be invoked**: Instance methods must be called on an object (an instance of the class). They cannot be invoked without creating an instance of the class.
   - **Common use cases**: Instance methods are used when the method needs to operate on instance variables or when the behavior of the method depends on the specific state of an object.

   Example:
   ```java
   class Calculator {
       int a, b;

       Calculator(int a, int b) {
           this.a = a;
           this.b = b;
       }

       int add() {  // Instance method
           return a + b;
       }
   }

   public class Main {
       public static void main(String[] args) {
           Calculator calc = new Calculator(5, 3);  // Create an object
           int result = calc.add();  // Calling instance method on the object
           System.out.println(result);  // Output: 8
       }
   }
   ```

### Key Differences:

| Feature                     | Static Method                              | Instance Method                            |
|-----------------------------|--------------------------------------------|--------------------------------------------|
| **Binding**                  | Bound to the class                        | Bound to the instance (object)             |
| **Access to Instance Variables** | Cannot access instance variables or methods | Can access instance variables and methods  |
| **Invocation**               | Can be called using the class name         | Must be called on an instance of the class |
| **Memory**                   | Shared by all instances                   | Each instance has its own copy of the method |
| **Use Case**                 | Typically used for utility methods, class-level operations | Used for operations that depend on the instance state |

## Method Overloading and Overriding

### 40. **What Is the Other Name of Method Overloading?**

**Method Overloading** is also commonly referred to as **"compile-time polymorphism"** or **"static polymorphism."**

This is because the decision regarding which method to call is made during **compile-time** based on the method signature (the number and type of parameters). The method name remains the same, but different parameter lists allow for multiple versions of the method.

### 41. **How Will You Implement Method Overloading in Java?**

**Method overloading** in Java is implemented by defining multiple methods with the **same name** but **different method signatures** within the same class. The method signature includes the method name and the number, type, or order of parameters. Overloading is not based on the return type of the method.

Example of method overloading:

```java
class Calculator {

    // Method to add two integers
    int add(int a, int b) {
        return a + b;
    }

    // Method to add three integers
    int add(int a, int b, int c) {
        return a + b + c;
    }

    // Method to add two doubles
    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();

        System.out.println(calc.add(5, 3));            // Calls add(int, int)
        System.out.println(calc.add(5, 3, 2));         // Calls add(int, int, int)
        System.out.println(calc.add(5.5, 3.2));        // Calls add(double, double)
    }
}
```

In this example, the method `add()` is overloaded with different parameter lists. The correct version of the method is called based on the number and type of arguments passed.

### 42. **What Kinds of Argument Variations Are Allowed in Method Overloading?**

In **method overloading**, the variations allowed are based on the method's **parameter list**, which can differ in:

1. **Number of Parameters**: You can overload methods by changing the number of parameters.
   
   Example:
   ```java
   void display(int a) { }
   void display(int a, int b) { }
   ```

2. **Type of Parameters**: You can overload methods by changing the type of one or more parameters.

   Example:
   ```java
   void show(int a) { }
   void show(double a) { }
   ```

3. **Order of Parameters**: You can overload methods by changing the order of parameters, even if the types are the same.

   Example:
   ```java
   void print(int a, double b) { }
   void print(double b, int a) { }
   ```

4. **Varargs (Variable Number of Arguments)**: Java allows you to pass a variable number of arguments using varargs (`...`), which can also be a form of overloading.

   Example:
   ```java
   void print(int... numbers) { }
   void print(String... strings) { }
   ```

However, **method overloading is determined by the method signature**, not by the return type, which leads to the next question.

### 43. **Why It Is Not Possible to Do Method Overloading by Changing the Return Type of Method in Java?**

In Java, **method overloading cannot be achieved by changing only the return type** because the method signature must be unique and distinguishable. The method signature consists of the **method name** and the **parameter list**, but **not the return type**. Therefore, if two methods have the same name and parameter list but different return types, the Java compiler cannot distinguish between them when called, leading to ambiguity.

For example, this would **not compile**:

```java
class Example {
    int add(int a, int b) { return a + b; }
    double add(int a, int b) { return a + b; }  // Error: Return type alone cannot differentiate methods
}
```

In this case, the two methods have the same name and parameters, so Java cannot decide which one to call based solely on the return type.

### 44. **Is It Allowed to Overload `main()` Method in Java?**

Yes, it is allowed to **overload the `main()` method** in Java. The `main()` method is just like any other method in a class, so you can define multiple versions of it with different parameter lists. 

However, the **entry point for the Java program** is the **`public static void main(String[] args)`** method, which is called by the JVM when the program starts. If you create overloaded versions of the `main()` method, they will not be called by the JVM. You would need to call them explicitly from within your `main()` method or another method.

Example of overloading `main()`:

```java
class Main {

    public static void main(String[] args) {
        System.out.println("Standard main method.");
        main(5);  // Calling overloaded main
    }

    // Overloaded main method with an integer argument
    public static void main(int a) {
        System.out.println("Overloaded main method: " + a);
    }
}
```

Output:
```
Standard main method.
Overloaded main method: 5
```

In this case, the JVM invokes the `main(String[] args)` method, but the overloaded `main(int a)` method can be called explicitly inside the program.

### 45. **How Do We Implement Method Overriding in Java?**

**Method overriding** in Java is a concept where a subclass provides a **specific implementation** for a method that is already defined in its superclass. The method in the subclass must have the **same signature** (same name, same parameter list) as the method in the superclass. The `@Override` annotation is commonly used for clarity and to help the compiler catch errors.

To implement method overriding:
1. The method in the **superclass** should be **non-static** and typically **public or protected** (so it can be overridden).
2. The subclass should provide its own implementation of the method with the same method signature.

Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {  // Overriding the sound method in the Dog subclass
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Animal();
        animal.sound();  // Calls Animal's sound()

        Dog dog = new Dog();
        dog.sound();  // Calls Dog's overridden sound()
    }
}
```

Output:
```
Animal makes a sound
Dog barks
```

In this example:
- The `sound()` method in the `Dog` class **overrides** the `sound()` method in the `Animal` class.
- When the method is called on an object of type `Dog`, the overridden version in the `Dog` class is executed.
- The `@Override` annotation is used to indicate that the method is intentionally overriding a superclass method.

### Key Points of Method Overriding:
- The method in the subclass must have the same method signature as the one in the superclass.
- Overriding allows the subclass to provide its own specific behavior.
- The method in the superclass should not be `private`, `final`, or `static` (because such methods cannot be overridden).
- The return type of the overridden method should be the same or a **subtype** (covariant return type) of the return type in the superclass method.

### 46. **Are We Allowed to Override a Static Method in Java?**

No, we **cannot override** a static method in Java. Static methods are associated with the class rather than with instances of the class. Therefore, static methods are resolved at compile time based on the class type, not the object type. This makes static methods **not subject to method overriding**.

However, we can **hide** a static method in a subclass by defining a static method with the same signature in the subclass. This is known as **method hiding**, not overriding.

### 47. **Why Java Does Not Allow Overriding a Static Method?**

Java does not allow overriding static methods because static methods are resolved **at compile-time** based on the class type, not the object type. Since static methods are tied to the class itself (not instances), they are not part of the object's dynamic dispatch mechanism that is needed for method overriding.

In other words:
- Static methods are called directly on the class (e.g., `ClassName.method()`).
- Method overriding involves dynamic polymorphism, where the method that gets called is determined at **runtime** based on the object’s type. Since static methods don’t participate in the runtime polymorphism, they cannot be overridden.

If a subclass defines a static method with the same name and signature as a static method in the parent class, it **hides** the parent class method, but this is not considered overriding.

### 48. **Is It Allowed to Override an Overloaded Method?**

Yes, **overloaded methods** can be overridden in Java. Overloading and overriding are two different concepts:
- **Overloading** occurs when methods have the same name but different parameter lists in the same class.
- **Overriding** occurs when a subclass provides a specific implementation for a method already defined in its superclass.

An **overloaded method** can be overridden if it is inherited by a subclass. The overriding method in the subclass must have the same method signature (name and parameters) as the method in the superclass.

Example:

```java
class Parent {
    void display(int a) {
        System.out.println("Parent display with int: " + a);
    }
}

class Child extends Parent {
    @Override
    void display(int a) {
        System.out.println("Child display with int: " + a);
    }
}

public class Main {
    public static void main(String[] args) {
        Parent p = new Child();
        p.display(10);  // Calls overridden method in Child
    }
}
```

In this example, the `display(int)` method is overridden by the `Child` class.

### 49. **What Is the Difference Between Method Overloading and Method Overriding in Java?**

| Feature                     | **Method Overloading**                                  | **Method Overriding**                                  |
|-----------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **Definition**               | Defining multiple methods with the same name but different parameter lists within the same class. | Providing a specific implementation of a method in a subclass that already exists in the superclass. |
| **Binding Time**             | Compile-time (resolved at compile time).               | Runtime (resolved dynamically at runtime).              |
| **Return Type**              | The return type can be different, as long as the parameter list differs. | The return type must be the same or covariant (a subclass type of the return type in the superclass). |
| **Method Signature**         | The method name and parameter list must differ.         | The method name and parameter list must be the same.     |
| **Inheritance Requirement**  | No inheritance required; overloading happens within the same class. | Inheritance required (subclass inherits the method).     |
| **Polymorphism**             | Not related to polymorphism.                          | Associated with polymorphism (dynamic method dispatch). |

Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    // Method Overriding
    @Override
    void sound() {
        System.out.println("Dog barks");
    }

    // Method Overloading
    void sound(int times) {
        for (int i = 0; i < times; i++) {
            System.out.println("Dog barks");
        }
    }
}
```

### 50. **Does Java Allow Virtual Functions?**

Yes, **Java supports virtual functions**. In fact, **all non-static, non-private methods in Java are virtual** by default. When you call a method on an object, Java determines at **runtime** which method to invoke, based on the actual object type (not the reference type). This is known as **dynamic method dispatch**, and it allows method overriding to work.

For example, if you have a superclass and subclass with an overridden method, Java will call the subclass method even if the reference variable is of the superclass type. This dynamic resolution of the method is referred to as **virtual method invocation** or **runtime polymorphism**.

Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();  // Animal reference, but Dog object
        animal.sound();  // Calls Dog's sound() method, not Animal's
    }
}
```

In this example, even though the reference type is `Animal`, the **virtual method** `sound()` is resolved at runtime to the `Dog` class version.

### 51. **What Is Meant by Covariant Return Type in Java?**

A **covariant return type** allows a method in a subclass to return a type that is a subclass of the return type declared in the superclass method. This concept is allowed in method overriding, meaning the return type in the overridden method can be more specific (or a subclass) than the return type in the parent class.

Example:

```java
class Animal {
    Animal getAnimal() {
        return new Animal();
    }
}

class Dog extends Animal {
    @Override
    Dog getAnimal() {  // Covariant return type (Dog is a subclass of Animal)
        return new Dog();
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        Animal animal = dog.getAnimal();  // Returns a Dog, but the reference is of type Animal
    }
}
```

## OOPS

### 00. **OOP Concepts with Example: Abstraction, Polymorphism, Inheritance, and Encapsulation**

**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of "objects," which are instances of classes. The four major principles of OOP are:

1. **Abstraction**: Hiding the implementation details and showing only the essential features of an object.
   - Example: You use a **smartphone** without needing to understand its internal workings. The complex functionalities (e.g., networking, hardware operations) are abstracted from the user.

   ```java
   abstract class Animal {
       abstract void sound();  // Abstract method - no implementation
   }

   class Dog extends Animal {
       void sound() {
           System.out.println("Dog barks");
       }
   }

   class Main {
       public static void main(String[] args) {
           Animal animal = new Dog();  // Polymorphism
           animal.sound();  // Dog barks
       }
   }
   ```

2. **Polymorphism**: The ability of a single function or method to behave differently based on the object it is acting upon. This can be achieved through **method overriding** (runtime polymorphism) and **method overloading** (compile-time polymorphism).
   
   ```java
   class Animal {
       void sound() {
           System.out.println("Animal makes a sound");
       }
   }

   class Dog extends Animal {
       @Override
       void sound() {
           System.out.println("Dog barks");
       }
   }

   class Main {
       public static void main(String[] args) {
           Animal animal = new Dog();  // Runtime Polymorphism
           animal.sound();  // Dog barks
       }
   }
   ```

3. **Inheritance**: A mechanism where one class acquires the properties and behaviors (methods) of another class. Inheritance promotes code reusability.
   
   ```java
   class Animal {
       void sound() {
           System.out.println("Animal makes a sound");
       }
   }

   class Dog extends Animal {
       void sound() {
           System.out.println("Dog barks");
       }
   }
   ```

4. **Encapsulation**: The concept of wrapping data (variables) and methods (functions) together as a single unit and restricting access to some of the object's components. It is achieved using **private** variables and **public** getter and setter methods.
   
   ```java
   class Person {
       private String name;  // private variable

       // Getter and Setter methods
       public String getName() {
           return name;
       }

       public void setName(String name) {
           this.name = name;
       }
   }

   class Main {
       public static void main(String[] args) {
           Person person = new Person();
           person.setName("John");
           System.out.println(person.getName());
       }
   }
   ```

### 52. **What Is Runtime Polymorphism?**

**Runtime Polymorphism**, also known as **dynamic method dispatch**, refers to the ability of Java to resolve method calls at runtime, based on the object type rather than the reference type. This allows one method to be used in different contexts, depending on the object that invokes it.

In Java, runtime polymorphism is typically achieved through **method overriding** (when a subclass overrides a method of its superclass).

Example:

```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();  // Reference of Animal, object of Dog
        animal.sound();  // Dog barks (resolved at runtime)
    }
}
```

In the above example, the method `sound()` is invoked on an `Animal` reference, but at runtime, it calls the `sound()` method of the `Dog` class because the actual object is of type `Dog`.

### 53. **Is It Possible to Achieve Runtime Polymorphism by Data Members?**

No, **runtime polymorphism** in Java cannot be achieved by **data members**. Polymorphism in Java is **only applicable to methods**, not fields or variables. Method overriding is the mechanism through which runtime polymorphism is achieved.

Data members (fields) are resolved at compile time based on the reference type. If two classes have the same field name, the field in the class being referenced is used, not the one in the actual object.

Example:

```java
class Animal {
    String type = "Animal";
}

class Dog extends Animal {
    String type = "Dog";
}

class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        System.out.println(animal.type);  // Outputs: Animal (resolved at compile time, not runtime)
    }
}
```

In this case, the field `type` in the `Animal` class is accessed, not the one in the `Dog` class, because field resolution is done at compile time, not at runtime.

### 54. **Explain the Difference Between Static and Dynamic Binding?**

**Binding** refers to the linking of a method call to the method body. There are two types of binding in Java: **static binding** (early binding) and **dynamic binding** (late binding).

- **Static Binding** (Early Binding):
  - It occurs at **compile time**.
  - It is used for method calls to **static**, **private**, and **final** methods, as well as **variables**.
  - In static binding, the method to be invoked or the variable to be accessed is determined at compile time based on the reference type.

  Example of static binding:

  ```java
  class Animal {
      static void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      static void sound() {
          System.out.println("Dog barks");
      }
  }

  class Main {
      public static void main(String[] args) {
          Animal animal = new Dog();
          animal.sound();  // Static binding, calls Animal's sound() method
      }
  }
  ```

- **Dynamic Binding** (Late Binding):
  - It occurs at **runtime**.
  - It is used for **method overriding**, where the method to be invoked is determined based on the actual object type at runtime.
  - It allows Java to choose the correct method when a method is called on a reference variable, based on the object type assigned to that reference.

  Example of dynamic binding:

  ```java
  class Animal {
      void sound() {
          System.out.println("Animal makes a sound");
      }
  }

  class Dog extends Animal {
      @Override
      void sound() {
          System.out.println("Dog barks");
      }
  }

  class Main {
      public static void main(String[] args) {
          Animal animal = new Dog();
          animal.sound();  // Dynamic binding, calls Dog's sound() method at runtime
      }
  }
  ```

### Key Differences:
- **Static Binding**:
  - Occurs at **compile time**.
  - Used for static, private, and final methods and fields.
  - Resolved based on the reference type.
- **Dynamic Binding**:
  - Occurs at **runtime**.
  - Used for method overriding (polymorphism).
  - Resolved based on the actual object type at runtime.

### 55. **What is Abstraction in Object-Oriented Programming?**

**Abstraction** is one of the fundamental principles of Object-Oriented Programming (OOP). It refers to the concept of **hiding the implementation details** and showing only the essential features of an object or system. In other words, abstraction allows us to define "what" an object does but not "how" it does it. This helps in reducing complexity and focusing on high-level functionalities.

In Java, abstraction can be achieved using:
1. **Abstract Classes**: Classes that cannot be instantiated directly and can have abstract methods (methods without body).
2. **Interfaces**: A contract that defines a set of methods that must be implemented by the class that implements the interface.

Example of Abstraction:

```java
abstract class Animal {
    abstract void sound();  // Abstract method (no implementation)
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();  // Animal reference, Dog object
        animal.sound();  // Dog barks
    }
}
```

In this example, the `sound()` method is abstract in the `Animal` class, so subclasses like `Dog` provide the implementation. The user of the class doesn't need to know how `sound()` is implemented but only that it will make a sound.

### 56. **How is Abstraction Different from Encapsulation?**

While both **abstraction** and **encapsulation** deal with hiding details, they focus on different aspects:

- **Abstraction** focuses on **hiding the complexity** and showing only the relevant functionality. It defines **what** an object should do but not **how** it should do it. 
  - Example: A **remote control** abstracts away the complexities of the television's internal working and provides only the essential functionality like power on/off, volume control, etc.

- **Encapsulation** focuses on **hiding the internal state** of an object and restricting access to it. It allows control over data by using **getter** and **setter** methods. It defines **how** an object’s data can be accessed or modified.
  - Example: A **bank account** class encapsulates the balance and allows access through methods like `deposit()` or `withdraw()`, hiding the internal balance state.

**Key Difference**:
- Abstraction hides complexity by exposing only necessary information (what an object does).
- Encapsulation hides data and allows controlled access to it (how an object stores and manipulates data).

Example:
```java
class BankAccount {
    private double balance;  // Encapsulation: balance is hidden

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;  // Deposit money into account
        }
    }

    public double getBalance() {
        return balance;  // Access the balance safely
    }
}

abstract class Shape {
    abstract void draw();  // Abstraction: defining a common method, but the implementation is hidden
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a Circle");
    }
}
```

### 57. **What is an Abstract Class in Java?**

An **abstract class** in Java is a class that **cannot be instantiated directly**. It is used as a base for other classes to inherit from. An abstract class can contain both abstract methods (methods without a body) and concrete methods (methods with implementation). 

**Key Points about Abstract Class**:
- It may contain abstract methods (methods without implementation).
- It may contain concrete methods (methods with implementation).
- It can have constructors, fields, and other members.
- A subclass that inherits an abstract class **must implement all of its abstract methods** unless the subclass is also abstract.

Example of Abstract Class:

```java
abstract class Animal {
    abstract void sound();  // Abstract method (no implementation)

    void eat() {  // Concrete method
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal dog = new Dog();
        dog.sound();  // Dog barks
        dog.eat();    // Animal is eating
    }
}
```

### 58. **Is It Allowed to Mark a Method Abstract Without Marking the Class Abstract?**

No, **you cannot mark a method as abstract** without marking the class as abstract. In Java, an abstract method must be defined in an abstract class. This is because abstract methods do not have an implementation, and the responsibility of providing an implementation for that method lies with subclasses. If a class contains an abstract method, it must be declared as abstract.

Example of Invalid Code:

```java
class Animal {
    abstract void sound();  // Error: Cannot have an abstract method in a non-abstract class
}
```

To correct this, you must mark the class as abstract:

```java
abstract class Animal {
    abstract void sound();  // This is correct now
}
```

### 59. **Is It Allowed to Mark a Method Abstract as Well as Final?**

No, you **cannot mark a method as both `abstract` and `final`**. The `abstract` modifier indicates that the method must be overridden by subclasses, while the `final` modifier indicates that the method cannot be overridden. These two behaviors are contradictory.

- **`abstract`** methods must be overridden in a subclass.
- **`final`** methods cannot be overridden in any subclass.

Therefore, it is not possible to have a method that is both abstract and final.

Example of Invalid Code:

```java
abstract class Animal {
    final abstract void sound();  // Error: Cannot be both final and abstract
}
```

To resolve this, you should choose one of the modifiers based on your intention:
- If the method should be overridden, use `abstract`.
- If the method should not be overridden, use `final`.

### 60. **Can We Instantiate an Abstract Class in Java?**

No, you **cannot instantiate an abstract class** in Java directly. An **abstract class** is designed to be a base class and can have abstract methods (methods without implementation), so it cannot be instantiated. However, you can create an instance of a subclass that extends the abstract class and provides implementations for the abstract methods.

Example:

```java
abstract class Animal {
    abstract void sound();
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal animal = new Animal();  // Error: Cannot instantiate an abstract class
        Animal animal = new Dog();  // Valid, creates an instance of Dog
        animal.sound();  // Dog barks
    }
}
```

### 61. **What is an Interface in Java?**

An **interface** in Java is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors. A class implements an interface by providing implementations for all of its methods. It defines a **contract** or a set of rules that the implementing class must follow.

Key points about interfaces:
- An interface defines **what a class should do**, but not **how it should do it**.
- A class that implements an interface **must provide an implementation** for all the methods declared by the interface, unless the class is abstract.
- An interface can be used to achieve **multiple inheritance** in Java.

Example:

```java
interface Animal {
    void sound();  // Method signature (no body)
}

class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.sound();  // Dog barks
    }
}
```

### 62. **Is It Allowed to Mark an Interface Method as Static?**

Yes, **it is allowed** to mark a method as **static** in an interface, starting from Java 8. A **static method** in an interface can have a body, and it can be invoked directly using the interface name. However, **static methods cannot be overridden** by implementing classes. They are not part of the contract that implementing classes have to follow.

Example of a static method in an interface:

```java
interface Animal {
    static void greet() {
        System.out.println("Hello from Animal");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal.greet();  // Directly call the static method on the interface
    }
}
```

### 63. **Why Can an Interface Not Be Marked as Final in Java?**

An interface **cannot be marked as `final`** because the purpose of an interface is to provide a **contract** that other classes can **implement**. If an interface were marked as `final`, no class would be able to implement it, making it pointless. A final class cannot be subclassed, and similarly, marking an interface as final would prevent any class from implementing it.

Example:

```java
// Invalid: Interfaces cannot be final
// final interface Animal { 
//     void sound();
// }
```

### 64. **What is a Marker Interface?**

A **marker interface** is an interface that has no methods or fields. It is used to signal a special behavior or property for the classes that implement it. A class implements a marker interface to indicate that it possesses certain characteristics, and the behavior is typically checked at runtime by other components.

The marker interface itself does not enforce any behavior, but its presence tells the program that the class should be treated in a special way.

**Common examples** of marker interfaces in Java include:
- `Serializable`: Marks a class whose objects can be serialized.
- `Cloneable`: Marks a class whose objects can be cloned.

Example of a Marker Interface:

```java
interface Serializable {
    // No methods or fields
}

class Person implements Serializable {
    String name;
    int age;

    // Person class can now be serialized
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        // If we try to serialize a Person object, it must implement Serializable
    }
}
```

### 65. **What Can We Use Instead of Marker Interface?**

Instead of using a marker interface, we can use the following alternatives in Java:

1. **Annotations**:
   - Annotations can provide metadata about the class or methods, similar to marker interfaces, but with more flexibility. Annotations can be processed at compile time or runtime to perform specific actions based on the presence of the annotation.
   
2. **Custom Logic or Flags**:
   - We can use custom logic within the class, such as setting a flag (boolean or other values) to indicate a special behavior. This can provide more control compared to marker interfaces, as it allows more information to be conveyed.

3. **Reflection**:
   - Using Java reflection, we can inspect class types and determine whether a class has a specific behavior or characteristic, without needing a marker interface.

**Example with Annotations**:
```java
@interface Serializable {
}

@Serializable
class Person {
    String name;
    int age;
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        // Check if the class has the Serializable annotation
        if (person.getClass().isAnnotationPresent(Serializable.class)) {
            System.out.println("Person class is serializable");
        }
    }
}
```

### 66. **How Are Annotations Better Than Marker Interfaces?**

Annotations are considered better than marker interfaces in many situations due to the following reasons:

1. **Flexibility**:
   - Annotations can carry **additional metadata**. While a marker interface only indicates that a class has a specific property, an annotation can carry more detailed information (e.g., a version number, author, or description).

2. **More Powerful and Extensible**:
   - Annotations are more **powerful and flexible** as they can be processed at compile-time (using annotation processors) or runtime (using reflection). You can also apply them to methods, fields, parameters, etc.
   
3. **Avoids Inheritance Issues**:
   - Marker interfaces force a class to inherit from an interface, which may not always be desirable. Using annotations, we avoid unwanted inheritance relationships. Classes don't have to implement an interface just for marking purposes.
   
4. **Cleaner Code**:
   - Using annotations eliminates the need for unnecessary interface implementation, which may lead to cleaner and more maintainable code.

**Example**:
```java
@interface Marker {
    String value() default "Default Marker";
}

@Marker(value = "Special Class")
class MyClass {
    // Additional logic
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        if (obj.getClass().isAnnotationPresent(Marker.class)) {
            System.out.println("This class has Marker annotation.");
        }
    }
}
```

### 67. **What is the Difference Between Abstract Class and Interface in Java?**

**Abstract Class** and **Interface** in Java are both used to represent abstract concepts, but they have several key differences:

| Feature                 | **Abstract Class**                                    | **Interface**                                      |
|-------------------------|--------------------------------------------------------|----------------------------------------------------|
| **Methods**             | Can have both abstract (without implementation) and concrete (with implementation) methods. | Can only have abstract methods (until Java 8) or default/static methods (from Java 8). |
| **Multiple Inheritance**| Supports single inheritance (a class can extend only one abstract class). | Supports multiple inheritance (a class can implement multiple interfaces). |
| **Constructors**        | Can have constructors.                                | Cannot have constructors.                         |
| **Fields**              | Can have instance variables (fields), both static and non-static. | Can only have static final variables (constants). |
| **Access Modifiers**    | Can have any access modifiers for methods and fields (e.g., public, private). | Methods in an interface are implicitly `public`, and fields are `public static final`. |
| **Purpose**             | Used when classes share common behavior and attributes, but they may have different implementations for some methods. | Used to define a contract that can be implemented by any class. |
| **Inheritance**         | A class can extend only one abstract class. | A class can implement multiple interfaces. |
  
**Example**:

```java
abstract class Animal {
    abstract void sound();  // Abstract method
    void eat() {            // Concrete method
        System.out.println("Animal is eating");
    }
}

interface Mammal {
    void giveBirth();  // Abstract method in interface
}
```

### 68. **Does Java Allow Us to Use Private and Protected Modifiers for Variables in Interfaces?**

In Java, the following rules apply to variables in interfaces:

- **Variables in interfaces** are implicitly **`public static final`**.
  - **`public`**: The variable is accessible by any class.
  - **`static`**: The variable belongs to the interface itself, not instances of the interface.
  - **`final`**: The variable cannot be modified once it is assigned.

As a result, **private** or **protected** modifiers are not allowed for variables in an interface because the primary goal of an interface is to provide a public contract that all implementing classes can access.

**Example of Valid Interface Variables**:

```java
interface Animal {
    // Implicitly public, static, and final
    int age = 10;  // Default access modifier is public static final

    void sound();  // Abstract method
}
```

You cannot use the `private` or `protected` modifiers for variables in an interface, and they will result in a compile-time error.

### 69. **How Can We Cast an Object Reference to an Interface Reference?**

In Java, you can cast an object reference to an interface reference if the object's class implements the interface. The cast is typically done when you want to treat the object as an instance of the interface, allowing you to call the methods defined by the interface.

Example:

```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();  // Implicit casting to Animal reference
        animal.sound();  // Dog barks

        // Explicit casting to the Animal interface reference
        Dog dog = (Dog) animal;  // Cast to the Dog class
        dog.sound();  // Dog barks
    }
}
```

In this example:
- The `Dog` object is cast to the `Animal` interface reference. Since `Dog` implements `Animal`, this cast is valid.
- You can also cast the object back to the original type (`Dog`), allowing you to access methods specific to `Dog`.

## Final

### 70. **How Can You Change the Value of a Final Variable in Java?**

In Java, a `final` variable **cannot be reassigned** once it has been initialized, meaning you cannot change its value after it has been assigned. However, there are some exceptions where the value of a `final` variable can appear to change:

1. **For Final Instance Variables**: 
   - If the `final` variable is an object reference, you cannot change the reference to point to another object, but you can modify the state of the object the reference points to (if the object's class allows that).
   
2. **For Final Local Variables**: 
   - Once a local `final` variable is assigned a value, it cannot be reassigned within the method.

3. **For Final Static Variables**:
   - Static `final` variables must be assigned exactly once, and this assignment typically happens during class initialization. You can assign them in a static block, but they cannot be reassigned after that.

**Examples:**

```java
class MyClass {
    final int x = 10;  // This final variable cannot be changed

    final int[] arr = {1, 2, 3}; // You can't reassign arr, but you can modify its elements

    public void changeValue() {
        // x = 20;  // Error: Cannot assign a value to final variable 'x'

        arr[0] = 100;  // Valid: Modifying an element of the final array
    }
}
```

### 71. **Can a Class Be Marked Final in Java?**

Yes, a **class can be marked as `final`** in Java. When a class is marked as `final`, it **cannot be subclassed**. This is useful when you want to ensure that the class’s behavior is not altered through inheritance, providing security or stability.

For example:
```java
final class MyClass {
    void display() {
        System.out.println("This is a final class.");
    }
}

// The following code will result in an error:
// class SubClass extends MyClass { }  // Error: Cannot subclass a final class
```

### 72. **How Can We Create a Final Method in Java?**

A **final method** in Java is a method that **cannot be overridden** by subclasses. It is marked with the `final` keyword to prevent any subclass from providing its own implementation of the method.

To declare a method as `final`:

```java
class MyClass {
    public final void display() {
        System.out.println("This method cannot be overridden.");
    }
}

class SubClass extends MyClass {
    // The following will result in an error:
    // public void display() { }  // Error: Cannot override the final method from MyClass
}
```

In this example, the `display()` method in `MyClass` is marked as `final`, so any subclass attempting to override it will result in a compile-time error.

### 73. **How Can We Prohibit Inheritance in Java?**

To **prohibit inheritance** in Java, you can **mark the class as `final`**. This prevents any subclass from inheriting from that class. When a class is marked as `final`, it cannot be extended.

```java
final class MyClass {
    void display() {
        System.out.println("This class cannot be inherited.");
    }
}

// The following will result in an error:
// class SubClass extends MyClass { }  // Error: Cannot subclass a final class
```

Alternatively, you can prevent inheritance of **specific methods** by marking them as `final`, as discussed above. This would allow you to prevent method overriding but still allow subclassing.

**To summarize**:
- To prohibit inheritance of a class, mark the class as `final`.
- To prevent method overriding, mark the method as `final`.

### 74. **Why is the Integer Class Final in Java?**

The **Integer class** in Java is marked as **final** to prevent subclassing. There are several reasons for this:

1. **Immutable Design**: 
   - The `Integer` class is immutable, meaning its state (the value it holds) cannot be changed after it is created. Allowing subclassing could compromise the immutability of the class, as a subclass could introduce methods that modify the state of the `Integer` object.

2. **Performance**: 
   - The `Integer` class is widely used in Java, and subclassing it might introduce performance overhead or unexpected behaviors that could interfere with its optimized implementation.

3. **Security**: 
   - Marking the `Integer` class as final prevents it from being extended, ensuring its behavior remains consistent and predictable across different uses.

By making it final, Java guarantees that the class’s behavior remains unaltered, improving reliability and reducing potential bugs.

### 75. **What is a Blank Final Variable in Java?**

A **blank final variable** is a `final` variable that is declared but **not initialized** at the time of declaration. It is **required to be initialized later**, either in the constructor or through an initializer block.

A blank final variable can be:
- **Instance variable**: A `final` variable that is not initialized in the constructor but needs to be assigned a value within the constructor.
- **Static final variable**: A static `final` variable that is not initialized at the point of declaration but needs to be initialized in a static block.

**Example:**

```java
class MyClass {
    final int x;  // Blank final instance variable

    MyClass(int value) {
        x = value;  // Blank final variable is initialized in constructor
    }
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass(100);
        System.out.println(obj.x);  // Output: 100
    }
}
```

### 76. **How Can We Initialize a Blank Final Variable?**

A **blank final variable** must be initialized in the constructor or a static block, depending on whether it is an instance or static variable. 

1. **Instance Blank Final Variable**:
   - It must be assigned a value in the constructor of the class before it is accessed.

```java
class MyClass {
    final int x;  // Blank final variable

    MyClass(int value) {
        x = value;  // Initialization of blank final variable
    }
}
```

2. **Static Blank Final Variable**:
   - A static blank final variable must be initialized in a static block, and it can only be assigned once.

```java
class MyClass {
    static final int x;  // Blank final static variable

    static {
        x = 100;  // Initialization of static final variable
    }
}
```

If you fail to initialize a blank final variable, the Java compiler will throw an error.

### 77. **Is it Allowed to Declare the Main Method as Final?**

Yes, it is **allowed to declare the `main` method as `final`** in Java. The `main` method is typically declared as `public static void main(String[] args)` because it is the entry point for any Java application, but you can also mark it as `final` if you wish.

**Example:**

```java
class MyClass {
    public final static void main(String[] args) {
        System.out.println("This is the main method.");
    }
}
```

In this case, declaring the `main` method as `final` would prevent any subclass from overriding it. However, in most cases, overriding the `main` method is not necessary or recommended, so declaring it as `final` simply provides the benefit of ensuring that it cannot be modified in subclasses.

- **Note**: The `main` method is typically **not overridden** in Java applications, as it is a static method designed to start the execution of the program. However, marking it as `final` doesn't have much practical effect other than ensuring no subclass can override it.

## Package

### 78. **What is the Purpose of Package in Java?**

In Java, a **package** serves several purposes:

1. **Namespace Management**: 
   - Packages help in organizing classes and interfaces in a hierarchical manner, preventing naming conflicts. For example, two classes with the same name can exist in different packages without causing ambiguity.

2. **Access Control**: 
   - Packages provide a way to control access to classes and methods. By using different access modifiers (`public`, `protected`, `private`), you can restrict access to certain classes or methods within a package or across different packages.

3. **Reusability and Maintainability**: 
   - By grouping related classes and interfaces together in a package, Java promotes code reusability and easier maintenance. A well-organized package structure makes it easier to maintain and extend the code.

4. **Avoiding Name Conflicts**: 
   - Packages help avoid conflicts between classes with the same name, as the package name differentiates them. For example, both `com.example.util.Date` and `com.example.app.Date` can coexist because they are in different packages.

**Example of Package**:
```java
package com.myapp.utilities;

public class MyClass {
    // Class implementation
}
```

### 79. **What is the `java.lang` Package?**

The **`java.lang`** package is one of the most fundamental and essential packages in Java. It is automatically imported into every Java program, meaning you don't have to explicitly import it. It contains fundamental classes that are necessary for Java programming, including:

1. **Primitive Wrapper Classes**:
   - Classes like `Integer`, `Character`, `Double`, etc., that wrap the primitive data types (`int`, `char`, `double`, etc.) into objects.

2. **String Class**:
   - The `String` class, which represents sequences of characters, is part of this package.

3. **Math Class**:
   - The `Math` class provides methods for mathematical operations such as `sqrt()`, `sin()`, and `pow()`.

4. **Thread and Exception Handling**:
   - Classes like `Thread`, `Runnable`, and `Throwable` (the superclass of all errors and exceptions) are part of this package.

5. **Object Class**:
   - The `Object` class, which is the root class of all classes in Java, is in the `java.lang` package. Every class in Java inherits from `Object`.

Other important classes in `java.lang` include `System`, `Runtime`, `Class`, `StringBuilder`, and `Integer`.

### 80. **Which is the Most Important Class in Java?**

The **`Object`** class is arguably the most important class in Java. It is the **root class** from which every other class in Java inherits, either directly or indirectly. The `Object` class provides several essential methods that every Java class inherits:

1. **`toString()`**: 
   - Returns a string representation of the object.
   
2. **`equals()`**: 
   - Compares two objects for equality.
   
3. **`hashCode()`**: 
   - Provides a hash code for the object, used in hashing-based collections like `HashMap`.
   
4. **`clone()`**: 
   - Creates a copy of the object.
   
5. **`getClass()`**: 
   - Returns the runtime class of the object.

**Example**:
```java
class MyClass {
    public String toString() {
        return "This is MyClass object";
    }
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        System.out.println(obj.toString());  // Output: This is MyClass object
    }
}
```

Since every class in Java inherits from `Object`, it provides a universal set of methods that can be used across all Java objects.

### 81. **Is it Mandatory to Import the `java.lang` Package Every Time?**

No, it is **not mandatory** to import the **`java.lang`** package explicitly because it is **automatically imported by the Java compiler** in every Java program. This package contains fundamental classes like `String`, `Object`, `Math`, and others that are essential for nearly all Java applications.

For example, you don't need to import the `String` class or `Math` class explicitly because they are part of `java.lang` and are always available:

**Example**:
```java
public class Main {
    public static void main(String[] args) {
        String message = "Hello, World!";
        double result = Math.pow(2, 3);
        System.out.println(message);  // Output: Hello, World!
        System.out.println(result);   // Output: 8.0
    }
}
```

In the above example, even though we use the `String` and `Math` classes, there is no need to import them explicitly because they are part of the `java.lang` package, which is implicitly imported.

### 82. **Can You Import the Same Package or Class Twice in Your Class?**

In Java, **you can import the same class or package multiple times**, but it is **redundant**. The Java compiler ignores repeated import statements for the same class or package, so there is no harm in importing them more than once. However, it's considered unnecessary and inefficient practice to do so.

For example:
```java
import java.util.List;
import java.util.List;  // This import is redundant

public class Main {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();
        list.add("Hello");
    }
}
```

In the above example, the second `import java.util.List` is redundant, and Java will ignore it. The same applies to importing packages. If you import `java.util.*` twice, only one of those imports will be effective.

### 83. **What is a Static Import in Java?**

A **static import** allows you to access the **static members (fields and methods)** of a class directly, without having to prefix them with the class name. This can make your code more concise and readable, especially when you are using many static members from a class.

**Syntax**:
```java
import static <package_name>.<class_name>.<static_member>;
```

You can import a static method or static variable from a class, and then you can use that method or variable directly in your code without needing to refer to the class explicitly.

**Example**:
```java
import static java.lang.Math.PI;
import static java.lang.Math.sqrt;

public class Main {
    public static void main(String[] args) {
        System.out.println(PI);   // Directly using PI without Math. prefix
        System.out.println(sqrt(16));  // Directly using sqrt() without Math. prefix
    }
}
```

In this example, we use `PI` and `sqrt()` directly without the `Math` class prefix, thanks to static imports.

### 84. **What is the Difference Between `import static com.test.FooClass` and `import com.test.FooClass`?**

The difference between `import static com.test.FooClass` and `import com.test.FooClass` lies in how the class or members are accessed:

1. **`import com.test.FooClass`**:
   - This is a **regular import** statement that imports the **entire class** (`FooClass`) from the `com.test` package.
   - After this import, you need to refer to any **non-static members** (fields or methods) of `FooClass` using the class name (e.g., `FooClass.method()`).
   
   **Example**:
   ```java
   import com.test.FooClass;

   public class Main {
       public static void main(String[] args) {
           FooClass obj = new FooClass();
           obj.someMethod();  // Accessing a method from FooClass
       }
   }
   ```

2. **`import static com.test.FooClass`**:
   - This is a **static import** that imports all the **static members** (fields or methods) from the `FooClass`.
   - After this import, you can **directly use static methods or fields** of `FooClass` without needing to refer to the class explicitly.
   
   **Example**:
   ```java
   import static com.test.FooClass.someStaticMethod;
   import static com.test.FooClass.someStaticVariable;

   public class Main {
       public static void main(String[] args) {
           someStaticMethod();  // Directly calling the static method
           System.out.println(someStaticVariable);  // Directly accessing the static variable
       }
   }
   ```

### Summary of the Difference:

- **`import com.test.FooClass`**: Imports the **entire class** (both static and non-static members), and you must use the class name to access any members.
- **`import static com.test.FooClass`**: Imports **only the static members** of the `FooClass`, allowing you to use those static members directly without the class name.

### Additional Notes:
- **Static import** is useful when you want to use several static members from a class without repeatedly typing the class name (e.g., `Math.PI`, `Math.sqrt()`, etc.).
- **Regular import** is used when you need to use the class itself or its non-static members.

## Internationalization

### 85. **What is Locale in Java?**

In Java, **Locale** is a class that represents a specific geographical, political, or cultural region. It is used to tailor programs to specific regions or countries by modifying the behavior of classes that perform locale-sensitive operations, such as date formatting, number formatting, and string comparison.

A `Locale` object is used to define the region, language, and sometimes the variant that affects how the program behaves, especially in terms of internationalization (i18n) and localization (l10n).

For example:
- **Language**: "en" for English, "fr" for French.
- **Country**: "US" for the United States, "IN" for India.
- **Variant**: Specific regional variations, such as "zh_CN" for Chinese in China and "zh_TW" for Chinese in Taiwan.

The **Locale** class allows Java applications to adapt based on the region or cultural preferences of users, which includes formatting dates, times, numbers, and other locale-specific content.

### 86. **How Will You Use a Specific Locale in Java?**

To use a specific `Locale` in Java, you create an instance of the `Locale` class by passing the desired language, country, and variant. Once the `Locale` is created, you can use it with various classes like `DateFormat`, `NumberFormat`, and `ResourceBundle` to tailor your program to the particular locale.

Here's how you can create and use a specific `Locale` in Java:

#### Example 1: Using `Locale` for Date Formatting

```java
import java.text.DateFormat;
import java.util.Date;
import java.util.Locale;

public class LocaleExample {
    public static void main(String[] args) {
        // Creating a specific Locale (e.g., French in France)
        Locale frenchLocale = new Locale("fr", "FR");

        // Creating DateFormat object for the French Locale
        DateFormat dateFormat = DateFormat.getDateInstance(DateFormat.FULL, frenchLocale);

        // Formatting the current date using the French locale
        Date date = new Date();
        System.out.println("Date in French Locale: " + dateFormat.format(date));
    }
}
```

In this example:
- The `Locale("fr", "FR")` specifies French as the language and France as the country.
- `DateFormat.getDateInstance()` is used with the locale to format the date in the appropriate way for that locale.

#### Example 2: Using `Locale` for Currency Formatting

```java
import java.text.NumberFormat;
import java.util.Locale;

public class LocaleCurrencyExample {
    public static void main(String[] args) {
        // Creating a Locale for US (English, United States)
        Locale usLocale = new Locale("en", "US");

        // Creating NumberFormat object for currency formatting
        NumberFormat currencyFormat = NumberFormat.getCurrencyInstance(usLocale);

        // Formatting a number as currency
        double amount = 1234567.89;
        System.out.println("Currency in US Locale: " + currencyFormat.format(amount));
    }
}
```

Here:
- `Locale("en", "US")` is used to specify the United States (English).
- `NumberFormat.getCurrencyInstance()` formats the number according to US currency conventions.

#### Example 3: Using `Locale` with `ResourceBundle` for Localization

```java
import java.util.Locale;
import java.util.ResourceBundle;

public class ResourceBundleExample {
    public static void main(String[] args) {
        // Creating a specific Locale (German in Germany)
        Locale germanLocale = new Locale("de", "DE");

        // Loading a resource bundle based on the German locale
        ResourceBundle messages = ResourceBundle.getBundle("MessagesBundle", germanLocale);

        // Retrieving and displaying a localized message
        System.out.println(messages.getString("greeting"));
    }
}
```

In this case:
- A `ResourceBundle` is loaded for the German locale (`de_DE`).
- The program retrieves a localized string from the `MessagesBundle` resource file, which contains key-value pairs like `"greeting" = "Hallo"`.

#### Common `Locale` Constructors:
- `Locale(String language)` — Creates a locale for the given language (e.g., `"en"` for English).
- `Locale(String language, String country)` — Creates a locale for the given language and country (e.g., `"en", "US"` for English in the United States).
- `Locale(String language, String country, String variant)` — Creates a locale for the given language, country, and variant (e.g., `"en", "US", "NY"` for English in the US, with a New York variant).

### Summary:
- A `Locale` is used in Java to tailor an application for specific regions, languages, or cultural preferences.
- You can create a `Locale` and pass it to classes like `DateFormat`, `NumberFormat`, and `ResourceBundle` to format or retrieve data in a way that is appropriate for the target locale.
- The `Locale` class plays an essential role in internationalization (i18n) and localization (l10n) of Java applications.

## Serialization

87. What is the serialization?
88. What is the purpose of serialization?
89. What is Deserialization?
90. What is Serialization and Deserialization conceptually?
91. Why do we mark a data member transient?
92. Is it allowed to mark a method as transient?
93. How does marking a field as transient makes it possible to serialize an object?
94. What is Externalizable interface in Java?
95. What is the difference between Serializable and Externalizable interface?

## Reflection

96. What is Reflection in Java?
97. What are the uses of Reflection in Java?
98. How can we access private method of a class from outside the class?
99. How can we create an Object dynamically at Runtime in Java?

## Garbage Collection

100.What is Garbage Collection in Java?
101.Why Java provides Garbage Collector?
102.What is the purpose of gc() in Java?
103.How does Garbage Collection work in Java?
104.When does an object become eligible for Garbage Collection in Java?
105.Why do we use finalize() method in Java?
106.What are the different types of References in Java?
107.How can we reference an unreferenced object again?
108.What kind of process is the Garbage collector thread?
109.What is the purpose of the Runtime class?
110.How can we invoke an external process in Java?
111.What are the uses of Runtime class?

## Inner Classes

112.What is a Nested class?
113.How many types of Nested classes are in Java?
114.Why do we use Nested Classes?
115.What is the difference between a Nested class and an Inner class in Java?
116.What is a Nested interface?
117.How can we access the non-final local variable, inside a Local Inner class?
118.Can an Interface be defined in a Class?
119.Do we have to explicitly mark a Nested Interface public static?
120.Why do we use Static Nested interface in Java?

## String

121.What is the meaning of Immutable in the context of String class in Java?
122.Why a String object is considered immutable in java?
123.How many objects does following code create?
124.How many ways are there in Java to create a String object?
125.How many objects does followingcode create?
126.What is String interning?
127.Why Java uses String literal concept?
128.What is the basic difference between a String and StringBuffe object?
129.How will you create an immutable class in Java?
130.What is the use of toString() method in java?
131.Arrange the three classes String, StringBuffer and StringBuilder in the order of efficiency for String processing operations?

## Exception Handling
132.What is Exception Handling in Java?
133.In Java, what are the differences between a Checked and Unchecked?
134.What is the base class for Error and Exception classes in Java?
135.What is a finally block in Java?
136.What is the use of finally block in Java?
137.Can we create a finally block without creating a catch block?
138.Do we have to always put a catch block after a try block?
139.In what scenarios, a finally block will not be executed?
140.Can we re-throw an Exception in Java?
141.What is the difference between throw and throws in Java?
142.What is the concept of Exception Propagation?
143.When we override a method in a Child class, can we throw an
additional Exception that is not thrown by the Parent class method?

## Multi-threading
144.How Multi-threading works in Java?
145.What are the advantages of Multithreading?
146.What are the disadvantages of Multithreading?
147.What is a Thread in Java?
148.What is a Thread’s priority and how it is used in scheduling?
149.What are the differences between Pre-emptive Scheduling Scheduler and Time Slicing Scheduler?
150.Is it possible to call run() method instead of start() on a thread in Java?
151.How will you make a user thread into daemon thread if it has already started?
152.Can we start a thread two times in Java?
153.In what scenarios can we interrupt a thread?
154.In Java, is it possible to lock an object for exclusive use by a thread?
155.How notify() method is different from notifyAll() method?

## Collections
156.What are the differences between the two data structures: a Vector and an ArrayList?
157.What are the differences between Collection and Collections in Java?
158.In which scenario, LinkedList is better than ArrayList in Java?
159.What are the differences between a List and Set collection in Java?
160.What are the differences between a HashSet and TreeSet collection in Java?
161.In Java, how will you decide when to use a List, Set or a Map collection?
162.What are the differences between a HashMap and a Hashtable in Java?
163.What are the differences between a HashMap and a TreeMap?
164.What are the differences between Comparable and Comparator?
165.In Java, what is the purpose of Properties file?
166.What is the reason for overriding equals() method?
167.How does hashCode() method work in Java?
168.Is it a good idea to use Generics in collections?

## Mixed Questions

169.What are Wrapper classes in Java?
170.What is the purpose of native method in Java?
171.What is System class?
172.What is System, out and println in System.out.println method call?
173.What is the other name of Shallow Copy in Java?
174.What is the difference between Shallow Copy and Deep Copy in Java?
175.What is a Singleton class?
176.What is the difference between Singleton class and Static class?

## Java Collection

177.What is the difference between Collection and Collections Framework in Java?
178.What are the main benefits of Collections Framework in Java?
179.What is the root interface of Collection hierarchy in Java?
180.What are the main differences between Collection and Collections?
181.What are the Thread-safe classes in Java Collections framework?
182.How will you efficiently remove elements while iterating a Collection?
183.How will you convert a List into an array of integers like- int[]?
184.How will you convert an array of primitive integers int[] to a List collection?
185.How will you run a filter on a Collection?
186.How will you convert a List to a Set?
187.How will you remove duplicate elements from an ArrayList?
188.How can you maintain a Collection with elements in Sorted order?
189.What is the difference between Collections.emptyList() and creating new instance of Collection?
190.How will you copy elements from a Source List to another list?
191.What are the Java Collection classes that implement List interface?
192.What are the Java Collection classes that implement Set interface?
193.What is the difference between an Iterator and ListIterator in Java?
194.What is the difference between Iterator and Enumeration?
195.What is the difference between an ArrayList and a LinkedList data structure?
196.What is the difference between a Set and a Map in Java?
197.What is the use of a Dictionary class?
198.What is the default size of load factor in a HashMap collection in Java?
199.What is the significance of load factor in a HashMap in Java?
200.What are the major differences between a HashSet and a HashMap?
201.What are the similarities between a HashSet and a HashMap in Java?
202.What is the reason for overriding equals() method?
203.How can we synchronize the elements of a List, a Set or a Map?
204.What is Hash Collision? How Java handles hash-collision in HashMap?
205.What are the Hash Collision resolution techniques?
206.What is the difference between Queue and Stack data structures?
207.What is an Iterator in Java?
208.What is the difference between Iterator and Enumeration in Java?
209.What is the design pattern used in the implementation of Enumeration in Java?
210.Which methods do we need to override to use an object as key in a HashMap?
211.How will you reverse a List in Java?
212.How will you convert an array of String objects into a List?
213.What is the difference between peek(), poll() and remove() methods of Queue interface in java?
214.What is the difference between Array and ArrayList in Java?
215.How will you insert, delete and retrieve elements from a HashMap collection in Java?
216.What are the main differences between HashMap and ConcurrentHashMap in Java?
217.What is the increasing order of performance for following collection classes in Java?
218.Why does Map interface not extend Collection interface in Java?
219.What are the different ways to iterate elements of a list in Java?
220.What is CopyOnWriteArrayList? How it is different from ArrayList in Java?
221.How remove() method is implemented in a HashMap?
222.What is BlockingQueue in Java Collections?
223.How is TreeMap class implemented in Java?
224.What is the difference between Fail-fast and Fail-safe iterator in Java?
225.How does ConcurrentHashMap work in Java?
226.What is the importance of hashCode() and equals() methods?
227.What is the contract of hashCode() and equals() methods in Java?
228.What is an EnumSet in Java?
229.What are the main Concurrent Collection classes in Java?
230.How will you convert a Collection to SynchronizedCollection in Java?
231.How IdentityHashMap is different from a regular Map in Java?
232.What is the main use of IdentityHashMap?
233.How can we improve the performance of IdentityHashMap?
234.Is IdentityHashMap thread-safe?
235.What is a WeakHashMap in Java?
236.How can you make a Collection class read Only in Java?
237.When is UnsupportedOperationException thrown in Java?
238.Let say there is a Customer class. We add objects of Customer class to an ArrayList. How can we sort the Customer objects in ArrayList by
using customer firstName attribute of Customer class?
239.What is the difference between Synchronized Collection and Concurrent Collection?
240.What is the scenario to use ConcurrentHashMap in Java?
241.How will you create an empty Map in Java?
242.What is the difference between remove() method of Collection and remove() method of Iterator?
243.Between an Array and ArrayList, which one is the preferred collection for storing objects?
244.Is it possible to replace Hashtable with ConcurrentHashMap in Java?
245.How CopyOnWriteArrayList class is different from ArrayList and Vector classes?
246.Why ListIterator has add() method but Iterator does not have?
247.Why do we sometime get ConcurrentModificationException during iteration?
248.How will you convert a Map to a List in Java?
249.How can we create a Map with reverse view and lookup in Java?
250.How will you create a shallow copy of a Map?
251.Why we cannot create a generic array in Java?
252.What is a PriorityQueue in Java?
253.What are the important points to remember while using Java Collections Framework?
254.How can we pass a Collection as an argument to a method and ensure that method will not be able to modify it?
255.Can you explain how HashMap works in Java?
256.Can you explain how HashSet is implemented in Java?
257.What is a NavigableMap in Java?
258.What is the difference between descendingKeySet() and descendingMap() methods of NavigableMap?
259.What is the advantage of NavigableMap over Map?
260.What is the difference between headMap(), tailMap() and subMap() methods of NavigableMap?
261.How will you sort objects by Natural order in a Java List?
262.How can we get a Stream from a List in Java?
263.Can we get a Map from a Stream in Java?
264.What are the popular implementations of Deque in Java? Advanced Multi-threading
265.What is a Thread in Java?
266.What is the priority of a Thread and how it is used in scheduling?
267.What is the default priority of a thread in Java?
268.What are the three different priorities that can be set on a Thread in Java?
269.What is the purpose of join() method in Thread class?
270.What is the fundamental difference between wait() and sleep() methods?
271.Is it possible to call run() method instead of start() on a thread in Java?
272.What is a daemon thread in Java?
273.How can we make a regular thread Daemon thread in Java?
274.How will you make a user thread into daemon thread if it has already started?
275.Can we start a thread two times in Java?
276.What is a Shutdown hook in Java?
277.What is synchronization in Java?
278.What is the purpose of Synchronized block in Java?
279.What is static synchronization?
280.What is a Deadlock situation?
281.What is the meaning of concurrency?
282.What is the main difference between process and thread?
283.What is a process and thread in the context of Java?
284.What is a Scheduler?
285.What is the minimum number of Threads in a Java program?
286.What are the properties of a Java thread?
287.What are the different states of a Thread in Java?
288.How will you set the priority of a thread in Java?
289.What is the purpose of Thread Groups in Java?
290.Why we should not stop a thread by calling its stop() method?
291.How will you create a Thread in Java?
292.How can we stop a thread in the middle of execution in Java?
293.How do you access the current thread in a Java program?
294.What is Busy waiting in Multi-threading?
295.How can we prevent busy waiting in Java?
296.Can we use Thread.sleep() method for real-time processing in Java?
297.Can we wake up a thread that has been put to sleep by using Thread.sleep() method?
298.What are the two ways to check if a Thread has been interrupted?
299.How can we make sure that Parent thread waits for termination of Child thread?
300.How will you handle InterruptedException in Java?
301.Which intrinsic lock is acquired by a synchronized method in Java?
302.Can we mark a constructor as synchronized in Java?
303.Can we use primitive values for intrinsic locks?
304.Do we have re-entrant property in intrinsic locks?
305.What is an atomic operation?
306.Can we consider the statement i++ as an atomic operation in Java?
307.What are the Atomic operations in Java?
308.Can you check if following code is thread-safe?
309.What are the minimum requirements for a Deadlock situation in a program?
310.How can we prevent a Deadlock?
311.How can we detect a Deadlock situation?
312.What is a Livelock?
313.What is Thread starvation?
314.How can a synchronized block cause Thread starvation in Java?
315.What is a Race condition?
316.What is a Fair lock in multi-threading?
317.Which two methods of Object class can be used to implement a Producer Consumer scenario?
318.How JVM determines which thread should wake up on notify()?
319.Check if following code is thread-safe for retrieving an integer value from a Queue?
320.How can we check if a thread has a monitor lock on a given object?
321.What is the use of yield() method in Thread class?
322.What is an important point to consider while passing an object from one thread to another thread?
323.What are the rules for creating Immutable Objects?
324.What is the use of ThreadLocal class?
325.What are the scenarios suitable for using ThreadLocal class?
326.How will you improve the performance of an application by multi-threading?
327.What is scalability in a Software program?
328.How will you calculate the maximum speed up of an application byusi ng multiple processors?
329.What is Lock contention in multi-threading?
330.What are the techniques to reduce Lock contention?
331.What technique can be used in following code to reduce Lock contention?
332.What is Lock splitting technique?
333.Which technique is used in ReadWriteLock class for reducing Lock contention?
334.What is Lock striping?
335.What is a CAS operation?
336.Which Java classes use CAS operation?
337.Is it always possible to improve performance by object pooling in a multi-threading application?
338.How can techniques used for performance improvement in a single thread application may degrade the performance in a multi-threading
application?
339.What is the relation between Executor and ExecutorService interface?
340.What will happen on calling submit() method of an ExecutorService instance whose queue is already full?
341.What is a ScheduledExecutorService?
342.How will you create a Thread pool in Java?
343.What is the main difference between Runnable and Callable interface?
344.What are the uses of Future interface in Java?
345.What is the difference in concurrency in HashMap and in Hashtable?
346.How will you create synchronized instance of List or Map Collection?
347.What is a Semaphore in Java?
348.What is a CountDownLatch in Java?
349.What is the difference between CountDownLatch and CyclicBarrier?
350.What are the scenarios suitable for using Fork/Join framework?
351.What is the difference between RecursiveTask and RecursiveAction class?
352.In Java 8, can we process stream operations with a Thread pool?
353.What are the scenarios to use parallel stream in Java 8?
354.How Stack and Heap work in Java multi-threading environment?
355.How can we take Thread dump in Java?
356.Which parameter can be used to control stack size of a thread in Java?
357.There are two threads T1 and T2? How will you ensure that these threads run in sequence T1, T2 in Java?

## Java 8

358.What are the new features released in Java 8?
359.What are the main benefits of new features introduced in Java 8?
360.What is a Lambda expression in Java 8?
361.What are the three main parts of a Lambda expression in Java?
362.What is the data type of a Lambda expression?
363.What is the meaning of following lambda expression?
364.Why did Oracle release a new version of Java like Java 8?
365.What are the advantages of a lambda expression?
366.What is a Functional interface in Java 8?
367.What is a Single Abstract Method (SAM) interface in Java 8?
368.How can we define a Functional interface in Java 8?
369.Why do we need Functional interface in Java?
370.Is it mandatory to use @FunctionalInterface annotation to define a Functional interface in Java 8?
371.What are the differences between Collection and Stream API in Java8?
372.What are the main uses of Stream API in Java 8?
373.What are the differences between Intermediate and Terminal Operations in Java 8 Streams?
374.What is a Spliterator in Java 8?
375.What are the differences between Iterator and Spliterator in Java 8?
376.What is Type Inference in Java 8?
377.Does Java 7 support Type Inference?
378.How does Internal Iteration work in Java 8?
379.What are the main differences between Internal and External Iterator?
380.What are the main advantages of Internal Iterator over External Iterator in Java 8?
381.What are the applications in which we should use Internal Iteration?
382.What is the main disadvantage of Internal Iteration over External Iteration?
383.Can we provide implementation of a method in a Java Interface?
384.What is a Default Method in an Interface?
385.Why do we need Default method in a Java 8 Interface?
386.What is the purpose of a Static method in an Interface in Java 8?
387.What are the core ideas behind the Date/Time API of Java 8?
388.What are the advantages of new Date and Time API in Java 8 over old Date API?
389.What are the main differences between legacy Date/Time API in Java and Date/Time API of Java 8?
390.How can we get duration between two dates or time in Java 8?
391.What is the new method family introduced in Java 8 for processing of Arrays on multi core machines?
392.How does Java 8 solve Diamond problem of Multiple Inheritance?
393.What are the differences between Predicate, Supplier and Consumer in Java 8?
394.Is it possible to have default method definition in an interface without marking it with default keyword?
395.Can we create a class that implements two Interfaces with default methods of same name and signature?
396.How Java 8 supports Multiple Inheritance?
397.In case we create a class that extends a base class and implements an interface. If both base class and interface have a default method with
same name and arguments, then which definition will be picked by JVM?
398.If we create same method and define it in a class , in its parent class and in an interface implemented by the class, then definition will be
invoked if we access it using the reference of Interface and the object of class?
399.Can we access a static method of an interface by using reference of the interface?
400.How can you get the name of Parameter in Java by using reflection?
401.What is Optional in Java 8?
402.What are the uses of Optional?
403.Which method in Optional provides the fallback mechanism in case of null value?
404.How can we get current time by using Date/Time API of Java 8?
405.Is it possible to define a static method in an Interface?
406.How can we analyze the dependencies in Java classes and packages?
407.What are the new JVM arguments introduced by Java 8?
408.What are the popular annotations introduced in Java 8?
409.What is a StringJoiner in Java 8?
410.What is the type of a Lambda expression in Java 8?
411.What is the target type of a lambda expression?
412.What are the main differences between an interface with default
method and an abstract class in Java 8?

## Java Tricky Questions

413.Is there any difference between a = a + b and a += b expressions?
414.What does the expression 1.0 / 0.0 return? Will there be any compilation error? 
415.Can we use multiple main methods in multiple classes?
416.Does Java allow you to override a private or static method?
417.What happens when you put a key object in a HashMap that isalready present?
418.How can you make sure that N threads can access N resources without deadlock?
419.How can you determine if JVM is 32-bit or 64-bit from Java Program? 
420.What is the right data type to represent Money (like Dollar/Pound) in Java?
421.How can you do multiple inheritances in Java?
422.Is ++ operation thread-safe in Java?
423.How can you access a non-static variable from the static context?
424.Let say there is a method that throws NullPointerException in the superclass. Can we override it with a method that throws
RuntimeException?
425.How can you mark an array volatile in Java?
426.What is a thread local variable in Java?
427.What is the difference between sleep() and wait() methods in Java?
428.Can you create an Immutable object that contains a mutable object?
429.How can you convert an Array of bytes to String?
430.What is difference between CyclicBarrier and CountDownLatch class?
431.What is the difference between StringBuffer and StringBuilder?
432.Which class contains clone method? Cloneable or Object class?
433.How will you take thread dump in Java?
434.Can you cast an int variable into a byte variable? What happens if the value of int is larger than byte?
435.In Java, can we store a double value in a long variable without explicit casting?
436.What will this return 5*0.1 == 0.5? true or false?
437.Out of an int and Integer, which one takes more memory?
438.Can we use String in the switch case statement in Java?
439.Can we use multiple main methods in same class?
440.When creating an abstract class, is it a good idea to call abstract methods inside its constructor?
441.How can you do constructor chaining in Java?
442.How can we find the memory usage of JVM from Java code?
443.What is the difference between x == y and x.equals(y) expressions in Java?
444. How can you guarantee that the garbage collection takes place?
445.What is the relation between x.hashCode() method and x.equals(y) method of Object class?
446.What is a compile time constant in Java?
447.Explain the difference between fail-fast and fail-safe iterators?
448. You have a character array and a String. Which one is more secure to store sensitive data (like password, date of birth, etc.)?
449.Why do you use volatile keyword in Java?
450.What is the difference between poll() and remove() methods of Queue in Java?
451.Can you catch an exception thrown by another thread in Java?
452.How do you decide which type of Inner Class – Static or Non-Static to use in Java?
453.What are the different types of Classloaders in Java?
454.What are the situations in which you choose HashSet or TreeSet?
455.What is the use of method references in Java?
456.Do you think Java Enums are more powerful than integer constants?
457.Why do we use static initializers in Java?
458.Your client is complaining that your code is throwing NoClassDefFoundError or NoSuchMethodError, even though you are ableto compile your code without error and method exists in your code. What
could be the reason behind this?
459.How can you check if a String is a number by using regular expression?
460.What is the difference between the expressions String s = "Temporary" and String s = new String("Temporary ")? Which one is
better and more efficient?
461.In Java, can two equal objects have the different hash code?
462.How can we print an Array in Java?
463.Is it ok to use random numbers in the implementation of hashcode() method in Java?
464.Between two types of dependency injections, constructor injection and setter dependency injection, which one is better?
465.What is the difference between DOM and SAX parser in Java?
466.Between Enumeration and Iterator, which one has better performance in Java?
467.What is the difference between pass by reference and pass by value?
468.What are the different ways to sort a collection in Java?
469.Why Collection interface doesn’t extend Cloneable and Serializable interfaces?
470.What is the difference between a process and a thread in Java?
471.What are the benefits of using an unordered array over an ordered array?
472.Between HashSet and TreeSet collections in Java, which one is better?
473.When does JVM call the finalize() method?
474.When would you use Serial Garabage collector or Throughput Garbage collector in Java?
475.In Java, if you set an object reference to null, will the Garbage Collector immediately free the memory held by that object?
476.How can you make an Object eligible for Garbage collection in Java?
477.When do you use Exception or Error in Java? What is the difference between these two?
478.What is the advantage of PreparedStatement over Statement class in Java?
479.In Java, what is the difference between throw and throws keywords? 
480.What happens to the Exception object after the exception handling is done?
481.How do you find which client machine is sending request to your servlet in Java? 
482.What is the difference between a Cookie and a Session object in Java?
483.Which protocol does Browser and Servlet use to communicate with each other?
484. What is HTTP Tunneling?
485.Why do we use JSP instead of Servlet in Java?
486.Is empty ‘.java’ file name a valid source file name in Java?
487.How do you implement Servlet Chaining in Java?
488.Can you instantiate this class?
489.Why Java does not support operator overloading?
490.Why String class is Immutable or Final in Java?
491.What is the difference between sendRedirect and forward methods?
492.How do you fix your Serializable class, if it contains a member that is not serializable?
493.What is the use of run time polymorphism in Java?
494.What are the rules of method overloading and method overriding in Java?
495.What is the difference between a class and an object in Java?
496.Can we create an abstract class that extends another abstract class?
497.Why do you use Upcasting or Downcasting in Java?
498.What is the reason to organize classes and interfaces in a package in Java?
499.What is information hiding in Java?
500.Why does Java provide default constructor?
501.What is the difference between super and this keywords in Java?
502.What is the advantage of using Unicode characters in Java?
503.Can you override an overloaded method in Java?
504.How can we change the heap size of a JVM?
505.Why should you define a default constructor in Java?
506.How will you make an Object Immutable in Java?
507.How can you prevent SQL Injection in Java Code?
508.Which two methods should be always implemented by HashMap key Object?
509.Why an Object used as Key in HashMap should be Immutable?
510.How can we share an object between multiple threads?
511.How can you determine if your program has a deadlock?

## JSP(Jakarta Server Pages)

512.What are the implicit objects in JSP?
513.How will you extend JSP code?
514.How will you handle runtime exceptions in JSP?
515.How will you prevent multiple submits of a page that come by clicking refresh button multiple times?
516.How will you implement a thread safe JSP page?
517.How will you include a static file in a JSP page?
518.What are the lifecycle methods of a JSP?
519.What are the advantages of using JSP in web architecture?
520.What is the advantage of JSP over Javascript?
521.What is the Lifecycle of JSP?
522.What is a JSP expression?
523.What are the different types of directive tags in JSP?
524.What is session attribute in JSP?
525.What are the different scopes of a JSP object?
526.What is pageContext in JSP?
527.What is the use of jsp:useBean in JSP?
528.What is difference between include Directive and include Action of JSP?
529.How will you use other Java files of your application in JSP code?
530.How will you use an existing class and extend it to use in the JSP?
531.Why _jspService method starts with _ symbol in JSP?
532.Why do we use tag library in JSP?
533.What is the different type of tag library groups in JSTL?
534.How will you pass information from one JSP to another JSP?
535.How will you call a stored procedure from JSP?
536.Can we override _jspService() method in JSP?
537.What is a directive in JSP?
538.How will you implement Session tracking in JSP?
539.How do you debug code in JSP?
540.How will you implement error page in JSP?
541.How will you send XML data from a JSP?
542.What happens when we request for a JSP page from web browser?
543.How will you implement Auto Refresh of page in JSP?
544.What are the important status codes in HTTP?
545.What is the meaning of Accept attribute in HTTP header?
546.What is the difference between Expression and Scriptlet in JSP?
547.How will you delete a Cookie in JSP?
548.How will you use a Cookie in JSP?
549.What is the main difference between a Session and Cookie in JSP?
550.How will you prevent creation of session in JSP?
551.What is an output comment in JSP?
552.How will you prevent caching of HTML output by web browser in JSP?
553.How will you redirect request to another page in browser in JSP code?
554.What is the difference between sendRedirect and forward in a JSP?
555.What is the use of config implicit object in JSP?
556.What is the difference between init-param and context-param?
557.What is the purpose of RequestDispatcher?
558.How can be read data from a Form in a JSP?
559.What is a filter in JSP?
560.How can you upload a large file in JSP?
561.In which scenario, Container initializes multiple JSP/Servlet objects? 

## Java Design Patterns

562.When will you use Strategy Design Pattern in Java?
563.What is Observer design pattern?
564.What are the examples of Observer design pattern in JDK?
565.How Strategy design pattern is different from State design pattern in Java?
566.Can you explain Decorator design pattern with an example in Java?
567.What is a good scenario for using Composite design Pattern in Java?
568.Have you used Singleton design pattern in your Java project?
569.What are the main uses of Singleton design pattern in Java project?
570.Why java.lang.Runtime is a Singleton in Java?
571.What is the way to implement a thread-safe Singleton design pattern in Java?
572.What are the examples of Singleton design pattern in JDK?
573.What is Template Method design pattern in Java?
574.What are the examples of Template method design pattern in JDK?
575.Can you tell some examples of Factory Method design pattern implementation in Java?
576.What is the benefit we get by using static factory method to create object?
577.What are the examples of Builder design pattern in JDK?
578.What are the examples of Abstract Factory design pattern in JDK?
579.What are the examples of Decorator design pattern in JDK?
580.What are the examples of Proxy design pattern in JDK?
581.What are the examples of Chain of Responsibility design pattern in JDK?
582.What are the main uses of Command design pattern?
583.What are the examples of Command design pattern in JDK?
584.What are the examples of Interpreter design pattern in JDK?
585.What are the examples of Mediator design pattern in JDK?
586.What are the examples of Strategy design pattern in JDK?
587.What are the examples of Visitor design pattern in JDK?
588.How Decorator design pattern is different from Proxy pattern?
589.What are the different scenarios to use Setter and Constructor based injection in Dependency Injection (DI) design pattern?
590.What are the different scenarios for using Proxy design pattern?
591.What is the main difference between Adapter and Proxy design pattern?
592.When will you use Adapter design pattern in Java?
593.What are the examples of Adapter design pattern in JDK?
594.What is the difference between Factory and Abstract Factory design pattern?
595.What is Open/closed design principle in Software engineering?
596.What is SOLID design principle?
597.What is Builder design pattern?
598.What are the different categories of Design Patterns used in Object Oriented Design?
599.What is the design pattern suitable to access elements of a Collection?
600.How can we implement Producer Consumer design pattern in Java?
601.What design pattern is suitable to add new features to an existing object?
602.Which design pattern can be used when to decouple abstraction from the implementation?
603.Which is the design pattern used in Android applications?
604.How can we prevent users from creating more than one instance of singleton object by using clone() method?
605.What is the use of Interceptor design pattern?
606.What are the Architectural patterns that you have used?
607.What are the popular uses of Façade design pattern?
608.What is the difference between Builder design pattern and Factory design pattern?
609.What is Memento design pattern?
610.What is an AntiPattern?
611.What is a Data Access Object (DAO) design pattern?

## Spring Questions

612.What is Spring framework?
613.What are the benefits of Spring framework in software development?
614.What are the modules in Core Container of Spring framework?
615.What are the modules in Data Access/Integration layer of Spring framework?
616.What are the modules in Web layer of Spring framework?
617.What is the main use of Core Container module in Spring framework?
618.What kind of testing can be done in Spring Test Module?
619.What is the use of BeanFactory in Spring framework?
620.Which is the most popular implementation of BeanFactory in Spring?
621.What is XMLBeanFactory in Spring framework?
622.What are the uses of AOP module in Spring framework?
623.What are the benefits of JDBC abstraction layer module in Spring framework?
624.How does Spring support Object Relational Mapping (ORM) integration?
625.How does Web module work in Spring framework?
626.What are the main uses of Spring MVC module?
627.What is the purpose of Spring configuration file?
628.What is the purpose of Spring IoC container?
629.What is the main benefit of Inversion of Control (IOC) principle?
630.Does IOC containers support Eager Instantiation or Lazy loading of beans?
631.What are the benefits of ApplicationContext in Spring?
632.How will you implement ApplicationContext in Spring framework?
633.Explain the difference between ApplicationContext and BeanFactory in Spring?
634.Between ApplicationContext and BeanFactory which one is preferable to use in Spring?
635.What are the main components of a typical Spring based application?
636.Explain Dependency Injection (DI) concept in Spring framework?
637.What are the different roles in Dependency Injection (DI)?
638.Spring framework provides what kinds of Dependency Injection mechanism?
639.In Spring framework, which Dependency Injection is better? Constructor-based DI or Setter-based DI?
640.What are the advantages of Dependency Injection (DI)?
641.What are the disadvantages of Dependency Injection (DI)?
642.What is a Spring Bean?
643.What does the definition of a Spring Bean contain?
644.What are the different ways to provide configuration metadata to a Spring Container?
645.What are the different scopes of a Bean supported by Spring?
646.How will you define the scope of a bean in Spring?
647.Is it safe to assume that a Singleton bean is thread safe in Spring Framework?
648.What are the design-patterns used in Spring framework?
649.What is the lifecycle of a Bean in Spring framework?
650.What are the two main groups of methods in a Bean’s lifecycle?
651.Can we override main lifecycle methods of a Bean in Spring?
652.What are Inner beans in Spring?
653.How can we inject a Java Collection in Spring framework?
654.What is Bean wiring in Spring?
655.What is Autowiring in Spring?
656.What are the different modes of Autowiring supported by Spring?
657.What are the cases in which Autowiring may not work in Spring framework?
658.Is it allowed to inject null or empty String values in Spring?
659.What is a Java-based Configuration in Spring?
660.What is the purpose of @Configuration annotation?
661.What is the difference between Full @Configuration and 'lite' @Beans mode?
662.In Spring framework, what is Annotation-based container configuration?
663.How will you switch on Annotation based wiring in Spring?
664.What is @Autowired annotation?
665.What is @Required annotation?
666.What are the two ways to enable RequiredAnnotationBeanPostProcessor in Spring?
667.What is @Qualifier annotation in Spring?
668.How Spring framework makes JDBC coding easier for developers?
669.What is the purpose of JdbcTemplate?
670.What are the benefits of using Spring DAO?
671.What are the different ways to use Hibernate in Spring?
672.What types of Object Relational Mapping (ORM) are supported by Spring?
673.How will you integrate Spring and Hibernate by using HibernateDaoSupport?
674.What are the different types of the Transaction Management supported by Spring framework?
675.What are the benefits provided by Spring Framework’s Transaction Management?
676.Given a choice between declarative and programmatic Transaction Management, which method will you choose?
677.What is Aspect Oriented Programming (AOP)
678.What is an Aspect in Spring?
679.In Spring AOP, what is the main difference between a Concern and a Cross cutting concern?
680.What is a Joinpoint in Spring AOP?
681.What is an Advice in Spring AOP?
682.What are the different types of Advice in Spring AOP?
683.What is a Pointcut in Spring AOP?
684.What is an Introduction in Spring AOP?
685.What is a Target object in Spring AOP?
686.What is a Proxy in Spring AOP?
687.What are the different types of AutoProxy creators in Spring?
688.What is Weaving in Spring AOP?
689.In Spring AOP, Weaving is done at compile time or run time?
690.What is XML Schema-based Aspect implementation?
691.What is Annotation-based aspect implementation in Spring AOP?
692.How does Spring MVC framework work?
693.What is DispatcherServlet?
694.Can we have more than one DispatcherServlet in Spring MVC?
695.What is WebApplicationContext in Spring MVC?
696.What is Controller in Spring MVC framework?
697.What is @RequestMapping annotation in Spring?
698.What are the main features of Spring MVC?
699.What is the difference between a Singleton and Prototype bean in Spring?
700.How will you decide which scope- Prototype or Singleton to use for a bean in Spring?
701.What is the difference between Setter and Constructor based Dependency Injection (DI) in Spring framework?
702.What are the drawbacks of Setter based Dependency Injection (DI) in Spring?
703.What are the differences between Dependency Injection (DI) and Factory Pattern?
704.In Spring framework, what is the difference between FileSystemResource and ClassPathResource?
705.Name some popular Spring framework annotations that you use in your project?
706.How can you upload a file in Spring MVC Application?
707.What are the different types of events provided by Spring framework?
708.What is the difference between DispatcherServlet and ContextLoaderListener in Spring?
709.How will you handle exceptions in Spring MVC Framework?
710.What are the best practices of Spring Framework?
711.What is Spring Boot?

## Hibernate

712.What is Hibernate framework?
713.What is an Object Relational Mapping (ORM)?
714.What is the purpose of Configuration Interface in Hibernate?
715.What is Object Relational Impedance Mismatch?
716.What are the main problems of Object Relational Impedance Mismatch?
717.What are the key characteristics of Hibernate?
718.Can you tell us about the core interfaces of Hibernate framework?
719.How will you map the columns of a DB table to the properties of a Java class in Hibernate?
720.Does Hibernate make it mandatory for a mapping file to have .hbm.xml extension?
721.What are the steps for creating a SessionFactory in Hibernate?
722.Why do we use POJO in Hibernate?
723.What is Hibernate Query Language (HQL)?
724.How will you call a stored procedure in Hibernate?
725.What is Criteria API in Hibernate?
726.Why do we use HibernateTemplate?
727.How can you see SQL code generated by Hibernate on console?
728.What are the different types of collections supported by Hibernate?
729.What is the difference between session.save() and session.saveOrUpdate() methods in Hibernate?
730.What are the advantages of Hibernate framework over JDBC?
731.How can we get statistics of a SessionFactory in Hibernate?
732.What is the Transient state of an object in Hibernate?
733.What is the Detached state of an object in Hibernate?
734.What is the use of Dirty Checking in Hibernate?
735.What is the purpose of Callback interface in Hibernate?
736.What are the different ORM levels in Hibernate?
737.What are the different ways to configure a Hibernate application?
738.What is Query Cache in Hibernate?
739.What are the different types of Association mappings supported by Hibernate?
740.What are the different types of Unidirectional Association mappings in Hibernate?
741.What is Unit of Work design pattern?
742.In Hibernate, how can an object go in Detached state?
743.How will you order the results returned by a Criteria in Hibernate?
744.How does Example criterion work in Hibernate?
745.How does Transaction management work in Hibernate?
746.How can we mark an entity/collection as immutable in Hibernate?
747.What are the different options to retrieve an object from database in Hibernate?
748.How can we auto-generate primary key in Hibernate?
749.How will you re-attach an object in Detached state in Hibernate?
750.What is the first level of cache in Hibernate?
751.What are the different second level caches available in Hibernate?
752.Which is the default transaction factory in Hibernate?
753.What are the options to disable second level cache in Hibernate?
754.What are the different fetching strategies in Hibernate?
755.What is the difference between Immediate fetching and Lazy collection fetching?
756.What is ‘Extra lazy fetching’ in Hibernate?
757.How can we check is a collection is initialized or not under Lazy Initialization strategy?
758.What are the different strategies for cache mapping in Hibernate?
759.What is the difference between a Set and a Bag in Hibernate?
760.How can we monitor the performance of Hibernate in an application?
761.How can we check if an Object is in Persistent, Detached or Transient state in Hibernate?
762.What is ‘the inverse side of association’ in a mapping?
763.What is ORM metadata?
764.What is the difference between load() and get() method in Hibernate?
765.When should we use get() method or load() method in Hibernate?
766.What is a derived property in Hibernate?
767.How can we use Named Query in Hibernate?
768.What are the two locking strategies in Hibernate?
769.What is the use of version number in Hibernate?
770.What is the use of session.lock() method in Hibernate?
771.What inheritance mapping strategies are supported by Hibernate?

## Maven

772.What is Maven?
773.What are the main features of Maven?
774.What areas of a Project can you manage by using Maven?
775.What are the main advantages of Maven?
776.Why do we say “Maven uses convention over configuration”?
777.What are the responsibilities of a Build tool like Maven?
778.What are the differences between Ant and Maven?
779.What is MOJO in Maven?
780.What is a Repository in Maven?
781.What are the different types of repositories in Maven?
782.What is a local repository in Maven?
783.What is a central repository in Maven?
784.What is a Remote repository in Maven?
785.Why we should not store jars in CVS or any other version control system instead of Maven repository?
786.Can anyone upload JARS or artifacts to Central Repository?
787.What is a POM?
788.What is Super POM?
789.What are the main required elements in POM file?
790.What are the phases in Build lifecycle in Maven?
791.What command will you use to package your Maven project?
792.What is the format of fully qualified artifact name of a Maven project?
793.What is an Archetype in Maven?
794.What is the command in Maven to generate an Archetype?
795.What are the three main build lifecycles of Maven?
796.What are the main uses of a Maven plugin?
797.How will you find the version of a plugin being used?
798.What are the different types of profile in Maven? Where will you define these profiles?
799.What are the different setting files in Maven? Where will you find these files?
800.What are the main elements we can find in settings.xml?
801.How will you check the version of Maven in your system?
802.How will you verify if Maven is installed on Windows?
803.What is a Maven artifact?
804.What are the different dependency scopes in Maven?
805.How can we exclude a dependency in Maven?
806.How Maven searches for JAR corresponding to a dependency?
807.What is a transitive dependency in Maven?
808.What are Excluded dependencies in Maven?
809.What are Optional dependencies in Maven?
810.Where will you find the class files after compiling a Maven project successfully?
811.What are the default locations for source, test and build directories in Maven?
812.What is the result of jar:jar goal in Maven?
813.How can we get the debug or error messages from the execution of Maven?
814.What is the difference between a Release version and SNAPSHOT version in Maven?
815.How will you run test classes in Maven?
816.Sometimes Maven compiles the test classes but doesn't run them? What could be the reason for it?
817.How can we skip the running of tests in Maven?
818.Can we create our own directory structure for a project in Maven?
819.What are the differences between Gradle and Maven?
820.What is the difference between Inheritance and Multi-module in Maven?
821.What is Build portability in Maven?

## GIT(Global information tracker)

822.How can we see n most recent commits in GIT?
823.How can we know if a branch is already merged into master in GIT?
824.What is the purpose of git stash drop?
825.What is the HEAD in GIT?
826.What is the most popular branching strategy in GIT?
827.What is SubGit?
828.What is the use of git instaweb?
829.What are git hooks?
830.What is GIT?
831.What is a repository in GIT?
832.What are the main benefits of GIT?
833.What are the disadvantages of GIT?
834.What are the main differences between GIT and SVN?
835.How will you start GIT for your project?
836.What is git clone in GIT?
837.How will you create a repository in GIT?
838.What are the different ways to start work in GIT?
839.GIT is written in which language?
840.What does ‘git pull’ command in GIT do internally?
841.What does ‘git push’ command in GIT do internally?
842.What is git stash?
843.What is the meaning of ‘stage’ in GIT?
844. What is the purpose of git config command?
845.How can we see the configuration settings of GIT installation?
846.How will you write a message with commit command in GIT?
847.What is stored inside a commit object in GIT?
848.How many heads can you create in a GIT repository?
849.Why do we create branches in GIT?
850.What are the different kinds of branches that can be created in GIT?
851.How will you create a new branch in GIT?
852.How will you add a new feature to the main branch?
853.What is a pull request in GIT?
854.What is merge conflict in GIT?
855.How can we resolve a merge conflict in GIT?
856.What command will you use to delete a branch?
857.What command will you use to delete a branch that has unmerged changes?
858.What is the alternative command to merging in GIT?
859.What is Rebasing in GIT?
860.What is the ‘Golden Rule of Rebasing’ in GIT?
861.Why do we use Interactive Rebasing in place of Auto Rebasing?
862.What is the command for Rebasing in Git?
863.What is the main difference between git clone and git remote?
864.What is GIT version control?
865.What GUI do you use for working on GIT?
866.What is the use of git diff command in GIT?
867.What is git rerere?
868.What are the three most popular version of git diff command?
869.What is the use of git status command?
870.What is the main difference between git diff and git status?
871.What is the use of git rm command in GIT?
872.What is the command to apply a stash?
873.Why do we use git log command?
874.Why do we need git add command in GIT?
875.Why do we use git reset command?
876.What does a commit object contain?
877.How can we convert git log messages to a different format?
878.What are the programming languages in which git hooks can be written?
879.What is a commit message in GIT?
880.How GIT protects the code in a repository?
881.How GIT provides flexibility in version control?
882.How can we change a commit message in GIT?
883.Why is it advisable to create an additional commit instead of amending an existing commit?
884.What is a bare repository in GIT?
885.How do we put a local repository on GitHub server?
886.How will you delete a branch in GIT?
887.How can we set up a Git repository to run code sanity checks and UAT tests just before a commit?
888.How can we revert a commit that was pushed earlier and is public now?
889.In GIT, how will you compress last n commits into a single commit?
890.How will you switch from one branch to a new branch in GIT?
891.How can we clean unwanted files from our working directory in GIT?
892.What is the purpose of git tag command?
893.What is cherry-pick in GIT?
894.What is shortlog in GIT?
895.How can you find the names of files that were changed in a specific commit?
896.How can we attach an automated script to run on the event of a new commit by push command?
897.What is the difference between pre-receive, update and post-receive hooks in GIT?
898.Do we have to store Scripts for GIT hooks within same repository?
899.How can we determine the commit that is the source of a bug in GIT?
900.How can we see differences between two commits in GIT?
901.What are the different ways to identify a commit in GIT?
902.When we run git branch <branchname>, how does GIT know the SHA-1 of the last commit?
903.What are the different types of Tags you can create in GIT?
904.How can we rename a remote repository?
905.Some people use git checkout and some use git co for checkout. Howis that possible?
906.How can we see the last commit on each of our branch in GIT?
907.Is origin a special branch in GIT?
908.How can we configure GIT to not ask for password every time?
909.What are the four major protocols used by GIT for data transfer?
910.What is GIT protocol?
911.How can we work on a project where we do not have push access?
912.What is git grep?
913.How can your reorder commits in GIT?
914.How will you split a commit into multiple commits?
915.What is filter-branch in GIT?
916.What are the three main trees maintained by GIT?
917.What are the three main steps of working GIT?
918.What are ours and theirs merge options in GIT?
919.How can we ignore merge conflicts due to Whitespace?
920.What is git blame?
921.What is a submodule in GIT?

## AWS(Amazon Web Service)

922.What do you know about AWS Region?
923.What are the important components of IAM?
924.What are the important points about AWS IAM?
925.What are the important features of Amazon S3?
926.What is the scale of durability in Amazon S3?
927.What are the Consistency levels supported by Amazon S3?
928.What are the different tiers in Amazon S3 storage?
929.How will you upload a file greater than 100 megabytes in Amazon S3?
930.What happens to an Object when we delete it from Amazon S3?
931.What is the use of Amazon Glacier?
932.Can we disable versioning on a version-enabled bucket in Amazon S3?
933.What are the use cases of Cross Region Replication Amazon S3?
934.Can we do Cross Region replication in Amazon S3 without enabling versioning on a bucket?
935.What are the different types of actions in Object Lifecycle Management in Amazon S3?
936.How do we get higher performance in our application by using Amazon CloudFront?
937.What is the mechanism behind Regional Edge Cache in Amazon CloudFront?
938.What are the benefits of Streaming content?
939.What is Lambda@Edge in AWS?
940.What are the different types of events triggered by Amazon CloudFront?
941.What is Geo Targeting in Amazon CloudFront?
942.What are the main features of Amazon CloudFront?
943.What are the security mechanisms available in Amazon S3?

## Cloud Computing

944.What are the benefits of Cloud Computing?
945.What is On-demand computing in Cloud Computing?
946.What are the different layers of Cloud computing?
947.What resources are provided by Infrastructure as a Service (IAAS) provider?
948.What is the benefit of Platform as a Service?
949.What are the main advantages of PaaS?
950.What is the main disadvantage of PaaS?
951.What are the different deployment models in Cloud computing?
952.What is the difference between Scalability and Elasticity?
953.What is Software as a Service?
954.What are the different types of Datacenters in Cloud computing?
955.Explain the various modes of Software as a Service (SaaS) cloud environment?
956.What are the important things to care about in Security in a cloud environment?
957.Why do we use API in cloud computing environment?
958.What are the different areas of Security Management in cloud?
959.What are the main cost factors of cloud based data center?
960.How can we measure the cloud-based services?
961.How a traditional datacenter is different from a cloud environment?
962.How will you optimize availability of your application in a Cloud environment?
963.What are the requirements for implementing IaaS strategy in Cloud?

## DOCKER

964.What is Docker?
965.What is the difference between Docker image and Docker container?
966.How will you remove an image from Docker?
967.How is a Docker container different from a hypervisor?
968.Can we write compose file in json file instead of yaml?
969.Can we run multiple apps on one server with Docker?
970.What are the common use cases of Docker?
971.What are the main features of Docker-compose?
972.What is the most popular use of Docker?
973.What is the role of open source development in the popularity of Docker?

## UNIX Shell

974.How will you remove all files in current directory? Including the files that are two levels down in a sub-directory.
975.What is the difference between the –v and –x options in Bash shell scripts?
976.What is a Filter in Unix command?
977.What is Kernel in Unix operating system?
978.What is a Shell in Unix OS?
979.What are the different shells in Unix that you know about?
980.What is the first character of the output in ls –l command?
981.What is the difference between Multi-tasking and Multi-user environment?
982.What is Command Substitution in Unix?
983.What is an Inode in Unix?
984.What is the difference between absolute path and relative path in Unix file system?
985.What are the main responsibilities of a Unix Shell?
986.What is a Shell variable?

## Microservices

987.What is a Microservice?
988.What are the benefits of Microservices architecture?
989.What is the role of architect in Microservices architecture?
990.What is the advantage of Microservices architecture over Service Oriented Architecture (SOA)?
991.Is it a good idea to provide a Tailored Service Template for Microservices development in an organization?
992.What are the disadvantages of using Shared libraries approach to decompose a monolith application?
993.What are the characteristics of a Good Microservice?
994.What is Bounded Context?
995.What are the points to remember during integration of Microservices?
996.Is it a good idea for Microservices to share a common database?
997.What is the preferred type of communication between Microservices? Synchronous or Asynchronous?
998.What is the difference between Orchestration and Choreography in Microservices architecture?
999.What are the issues in using REST over HTTP for Microservices?
1000. Can we create Microservices as State Machines?