Here’s a comprehensive list of **100 Java interview questions** that cover a wide range of Java concepts, including basic, advanced, and practical aspects of Java programming:

### **Core Java Concepts:**
Here are the answers to your Java-related questions:

### 1. **What is Java, and what are its main features?**

Java is a high-level, object-oriented programming language designed to have as few implementation dependencies as possible. It was developed by Sun Microsystems (now owned by Oracle). Java is widely used for building platform-independent applications, including web and mobile apps. Key features of Java include:

- **Platform Independence**: Java programs can run on any device or platform with a Java Virtual Machine (JVM) installed.
- **Object-Oriented**: Java follows the principles of object-oriented programming (OOP), such as inheritance, polymorphism, encapsulation, and abstraction.
- **Security**: Java provides a secure environment for developing applications, including features like bytecode verification.
- **Multithreading**: Java supports multithreaded programming, allowing efficient use of resources.
- **Automatic Memory Management**: Java handles memory management through garbage collection.

### 2. **What are the differences between Java and other programming languages like C or C++?**

- **Platform Independence**: Unlike C and C++, which are compiled into platform-specific machine code, Java is compiled into bytecode that runs on the JVM, allowing Java programs to be platform-independent.
- **Memory Management**: Java uses automatic garbage collection for memory management, whereas C and C++ require manual memory management using pointers and `malloc/free`.
- **Object-Oriented**: Java is a strictly object-oriented language (everything is an object), whereas C is procedural, and C++ supports both procedural and object-oriented paradigms.
- **Pointers**: Java does not support direct pointers, unlike C and C++, which use pointers to reference memory locations.

### 3. **What is the JVM, JRE, and JDK? How do they differ?**

- **JVM (Java Virtual Machine)**: The JVM is the runtime environment that executes Java bytecode. It provides platform independence by translating the bytecode into native code for the specific platform it runs on.
- **JRE (Java Runtime Environment)**: The JRE is a package that includes the JVM along with libraries and other components required to run Java applications. It does not include development tools.
- **JDK (Java Development Kit)**: The JDK is a full development kit that includes the JRE and additional tools needed to develop Java applications, such as compilers (javac) and debuggers.

### 4. **====**


### 5. **What are the four pillars of Object-Oriented Programming (OOP)?**

The four pillars of OOP are:

- **Encapsulation**: Wrapping data and methods into a single unit (class) and restricting access to some components using access modifiers.
- **Inheritance**: The ability of a class to inherit the properties and behaviors of another class.
- **Polymorphism**: Allowing one entity to take multiple forms (e.g., method overloading, method overriding).
- **Abstraction**: Hiding the implementation details and showing only the necessary functionality to the user.

### 6. **What is a class in Java? How is it different from an object?**

- **Class**: A class is a blueprint or template for creating objects in Java. It defines attributes (variables) and behaviors (methods) that the objects created from it will have.
- **Object**: An object is an instance of a class. It represents a concrete entity created using the class blueprint. While a class is a template, an object is a real-world instance.

### 7. **What is the difference between instance variables and class variables?**

- **Instance Variables**: These are variables defined inside a class but outside any method, constructor, or block. They are unique to each instance of the class, meaning each object has its own copy of instance variables.
  
- **Class Variables (Static Variables)**: These are variables defined with the `static` keyword. They belong to the class itself, rather than any instance, and all instances of the class share the same value for class variables.

### 8. **What is a constructor in Java? How is it different from a method?**

- **Constructor**: A constructor is a special method that is used to initialize objects. It has the same name as the class and is invoked when an object of the class is created. Constructors do not have a return type.
  
- **Method**: A method is a function defined in a class that describes the behavior of the object. Methods have a return type and are used to perform specific operations or calculations.

### 9. **What is the purpose of the `this` keyword in Java?**

The `this` keyword in Java refers to the current object, and it is used in the following scenarios:
- To refer to instance variables when they are shadowed by method or constructor parameters.
- To call the current object's method or constructor.
- To pass the current object as a parameter to other methods or constructors.

### 10. **Explain the concept of method overloading in Java.**

Method overloading in Java occurs when multiple methods have the same name but differ in their parameter lists (either in the number or type of parameters). The return type can be the same or different, but overloading is determined based on the method's signature (name + parameter list).

Example:
```java
class Example {
    void display(int a) {
        System.out.println(a);
    }

    void display(String a) {
        System.out.println(a);
    }
}
```
Here are the answers to the additional Java-related questions:

### 11. **What is method overriding in Java?**

Method overriding in Java occurs when a subclass provides a specific implementation of a method that is already defined in its superclass. The method in the subclass must have the same name, return type, and parameters as the method in the superclass. Overriding allows the subclass to offer a more specific behavior for a method inherited from the superclass.

- **Key points**:
  - The method in the subclass overrides the inherited method from the parent class.
  - The `@Override` annotation is used (though optional) to indicate that the method is overriding a method in the superclass.
  - Overriding is used for runtime polymorphism.

**Example**:
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
```
In this example, the `Dog` class overrides the `sound()` method of the `Animal` class.

### 12. **What is the difference between `==` and `equals()` in Java?**

- **`==`**: The `==` operator is used for reference comparison. It checks if two references point to the exact same object in memory (i.e., it compares object addresses).
  
- **`equals()`**: The `equals()` method is used to compare the contents or state of two objects. It is used to check if two objects are logically equivalent (depending on how `equals()` is implemented in the class). The `equals()` method can be overridden to provide custom equality logic.

**Example**:
```java
String a = new String("Hello");
String b = new String("Hello");

System.out.println(a == b);       // false (different memory references)
System.out.println(a.equals(b));  // true (same value)
```

### 13. **========**



### 14. **What is the difference between `public`, `private`, `protected`, and default access modifiers?**

- **`public`**: The class, method, or variable is accessible from any other class, regardless of the package.
- **`private`**: The class, method, or variable is accessible only within the same class.
- **`protected`**: The class, method, or variable is accessible within the same package and by subclasses, even if they are in different packages.
- **Default (no modifier)**: The class, method, or variable is accessible only within classes that belong to the same package.

### 15. **What is a static method in Java?**

A static method is a method that belongs to the class rather than to instances of the class. It can be called without creating an instance of the class. Static methods can access static variables and other static methods directly but cannot access instance variables or instance methods without creating an object.

**Example**:
```java
class MyClass {
    static void greet() {
        System.out.println("Hello, World!");
    }
}

public class Main {
    public static void main(String[] args) {
        MyClass.greet(); // No object is required to call this static method
    }
}
```

### 16. **What is a static block in Java?**

A static block (or static initializer) is a block of code inside a class that is executed only once, when the class is first loaded into memory. It is typically used to initialize static variables or perform one-time setup tasks.

**Example**:
```java
class MyClass {
    static {
        System.out.println("Static block executed");
    }
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass();  // Static block is executed when the class is loaded
    }
}
```

### 17. **What is the difference between a final class, final method, and final variable?**

- **`final class`**: A class declared as `final` cannot be subclassed. For example, the `String` class is `final`, meaning you cannot extend it.
  
- **`final method`**: A method declared as `final` cannot be overridden by subclasses.
  
- **`final variable`**: A variable declared as `final` cannot have its value changed once it is initialized. This makes the variable a constant if it's a primitive type or an immutable reference if it's an object.

**Example**:
```java
final class MyClass { }  // Cannot be subclassed

class Base {
    final void myMethod() { }  // Cannot be overridden by subclasses
}

final int myVar = 10;  // Cannot be reassigned
```

### 18. **What is the difference between `String`, `StringBuilder`, and `StringBuffer` in Java?**

- **`String`**: Immutable, meaning once a `String` object is created, its value cannot be changed. Operations that modify a `String` create a new `String` object.
- **`StringBuilder`**: Mutable, used for manipulating strings when you need to modify them frequently. It is more efficient than `String` for such tasks.
- **`StringBuffer`**: Similar to `StringBuilder`, but it is **synchronized**, making it thread-safe. It is slower than `StringBuilder` because of the synchronization overhead.

### 19. **What is the significance of `hashCode()` and `equals()` methods?**

- **`hashCode()`**: The `hashCode()` method returns an integer value (hash code) that represents the memory address of the object or a value derived from its state. It is used in hashing-based collections like `HashMap` and `HashSet` to efficiently locate objects.
  
- **`equals()`**: The `equals()` method is used to compare two objects for equality based on their content or state. The `hashCode()` method must be overridden if `equals()` is overridden to ensure correct behavior in collections that rely on hashing (like `HashMap`).

### 20. **======**


### **Object-Oriented Concepts:**
Here are the answers to your Java-related questions:

### 21. **What is polymorphism in Java?**

Polymorphism in Java refers to the ability of an object to take on many forms. It allows one interface to be used for a general class of actions, with the specific action determined by the object that is calling it. There are two types of polymorphism in Java:

- **Compile-time polymorphism (Method Overloading)**: Occurs when multiple methods with the same name but different parameters exist in the same class.
- **Runtime polymorphism (Method Overriding)**: Occurs when a subclass provides a specific implementation of a method that is already defined in its superclass.

**Example**:
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

public class Test {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.sound();  // Runtime polymorphism: Dog barks
    }
}
```

### 22. **=====**


### 23. **What is inheritance in Java? Explain with an example.**

Inheritance in Java is a mechanism where one class (the subclass or child class) inherits the fields and methods of another class (the superclass or parent class). It promotes code reusability and method overriding.

**Example**:
```java
class Animal {
    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

public class Test {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();  // Inherited method
        dog.bark(); // Dog's own method
    }
}
```
Here, `Dog` inherits the `eat()` method from `Animal` class.

### 24. **What is encapsulation? Why is it important in Java?**

Encapsulation is the concept of bundling the data (variables) and the methods that operate on the data into a single unit, a class. It also involves controlling access to the data by using access modifiers (`private`, `public`, etc.). It helps in hiding the internal state of the object and restricting direct access to its fields, providing controlled access through getter and setter methods.

**Importance**:
- Helps in data hiding, reducing complexity, and increasing security.
- Improves maintainability by controlling how data is accessed and modified.

**Example**:
```java
class Person {
    private String name; // private field
    
    public String getName() { // getter
        return name;
    }

    public void setName(String name) { // setter
        this.name = name;
    }
}
```

### 25. **What is the difference between composition and inheritance?**

- **Composition**: In composition, a class contains references to objects of other classes, allowing one class to be composed of multiple other classes. It is a "has-a" relationship.
  - **Example**: A `Car` has an `Engine`.

- **Inheritance**: In inheritance, a subclass inherits properties and behaviors from a superclass, establishing an "is-a" relationship.
  - **Example**: A `Dog` is an `Animal`.

Composition is generally favored over inheritance as it provides better flexibility and avoids the complexities of multiple inheritance.

### 26. **What is abstraction in Java, and how is it implemented?**

Abstraction is the process of hiding implementation details and showing only essential features to the user. It helps in reducing complexity and allows focusing on high-level functionalities. In Java, abstraction can be achieved using:

- **Abstract classes**: A class that cannot be instantiated and may have abstract methods (methods without implementation).
- **Interfaces**: A contract that defines methods that must be implemented by a class.

**Example of Abstract Class**:
```java
abstract class Animal {
    abstract void sound();  // Abstract method
    
    void breathe() {  // Concrete method
        System.out.println("Breathing");
    }
}
```

**Example of Interface**:
```java
interface Animal {
    void sound();  // Abstract method
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Barking");
    }
}
```

### 27. **What is the `super` keyword in Java?**

The `super` keyword is used to refer to the superclass (parent class) of the current object. It can be used to:

- Access superclass methods.
- Call the superclass constructor.

**Example**:
```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    void sound() {
        super.sound();  // Calling superclass method
        System.out.println("Dog barks");
    }
}
```

### 28. **What is the `instanceof` keyword in Java?**

The `instanceof` keyword is used to check whether an object is an instance of a particular class or subclass or implements a specific interface. It returns `true` if the object is an instance of the specified type, otherwise `false`.

**Example**:
```java
String str = "Hello";
System.out.println(str instanceof String);  // true
```

### 29. **Can you override a `private` or `static` method in Java?**

- **Private methods**: Cannot be overridden because they are not visible to the subclass. They are only accessible within the same class.
  
- **Static methods**: Can be hidden (not overridden) in a subclass. Static methods are resolved at compile time, so they are bound to the class rather than the object.

**Example**:
```java
class Parent {
    private void display() {
        System.out.println("Parent display");
    }
}

class Child extends Parent {
    // Cannot override private method
    // private void display() {}  // This will cause a compile-time error
}
```

### 30. **What is the difference between an interface and an abstract class?**

- **Interface**:
  - Cannot have any method implementations (prior to Java 8).
  - All methods are implicitly `abstract` unless defined as `default` or `static` (Java 8+).
  - A class can implement multiple interfaces (supports multiple inheritance).
  - Interfaces are used to define a contract that multiple classes can implement.

- **Abstract Class**:
  - Can have both abstract and concrete (implemented) methods.
  - A class can inherit only one abstract class (single inheritance).
  - Abstract classes are used when we want to provide a common base with shared functionality, while allowing some methods to be abstract.

### 31. **How do you implement multiple inheritance in Java?**

Java does not support multiple inheritance for classes to avoid ambiguity. However, multiple inheritance can be achieved through interfaces, where a class can implement multiple interfaces.

**Example**:
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

### 32. **Can a class implement multiple interfaces in Java? How?**

Yes, a class can implement multiple interfaces in Java by separating the interface names with a comma. This allows a class to inherit behavior from more than one interface.

**Example**:
```java
interface A {
    void methodA();
}

interface B {
    void methodB();
}

class MyClass implements A, B {
    public void methodA() {
        System.out.println("Method A");
    }

    public void methodB() {
        System.out.println("Method B");
    }
}
```

### 33. **What is the use of `default` methods in interfaces in Java?**

The `default` keyword in interfaces (introduced in Java 8) allows you to define concrete methods in interfaces. This enables adding new methods to interfaces without breaking the existing implementations. The `default` method provides a default behavior that can be used by implementing classes.

**Example**:
```java
interface MyInterface {
    default void greet() {
        System.out.println("Hello, World!");
    }
}

class MyClass implements MyInterface {
    // Inheriting the default greet() method
}

public class Test {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.greet();  // Outputs: Hello, World!
    }
}
```

### **Memory Management and Garbage Collection:**
Here are the answers to your Java-related questions:

### 34. **What is garbage collection in Java?**

Garbage collection (GC) in Java is the process of automatically identifying and reclaiming memory that is no longer in use by the program. It is a part of Java’s memory management system. The primary goal of garbage collection is to free up memory by removing objects that are no longer reachable from the program, thus preventing memory leaks and improving performance.

### 35. **How does garbage collection work in Java?**

Garbage collection works by automatically identifying objects that are no longer referenced by the program. The JVM (Java Virtual Machine) uses several algorithms to perform garbage collection, such as the **Mark-and-Sweep** algorithm, the **Generational Garbage Collection** algorithm, and others. Here’s an overview of how it typically works:

1. **Marking phase**: The garbage collector identifies which objects are still being referenced and which are not.
2. **Sweeping phase**: The garbage collector removes unreferenced objects, reclaiming their memory.
3. **Compaction**: After sweeping, the memory may be fragmented. Compaction may be performed to move the remaining objects together to reduce fragmentation.

Garbage collection in Java is automatic, but developers can suggest or trigger garbage collection using `System.gc()` (though this is not guaranteed to actually perform GC).

### 36. **What is the role of the `finalize()` method in garbage collection?**

The `finalize()` method in Java is a method that is called by the garbage collector before an object is destroyed. It provides an opportunity to release resources or perform cleanup tasks before the object’s memory is reclaimed. However, `finalize()` is rarely used and has been largely replaced by other resource management techniques (like `try-with-resources` and `AutoCloseable`).

- **Note**: `finalize()` is not guaranteed to be called, and it is not recommended to rely on it for important cleanup tasks.

```java
protected void finalize() throws Throwable {
    // Cleanup code, e.g., releasing resources
    super.finalize();
}
```

### 37. **What is memory leak, and how can you prevent it in Java?**

A **memory leak** in Java occurs when an application consumes memory but fails to release it when no longer needed. This happens when objects are no longer used but are still being referenced, preventing the garbage collector from reclaiming their memory.

**How to prevent memory leaks**:
- **Avoid unnecessary object references**: Ensure objects that are no longer needed are dereferenced (set to `null`).
- **Use try-with-resources**: For managing resources like file streams, database connections, etc., which automatically close and release resources.
- **Profile memory usage**: Use tools like **VisualVM** or **JProfiler** to monitor memory and identify potential leaks.

### 38. **Explain the concept of heap and stack memory in Java.**

- **Heap Memory**: Heap is used to store objects in Java. It is shared among all threads and is managed by the garbage collector. Objects created using `new` (like instances of classes) are allocated in the heap. The heap is large and can be expanded dynamically, but memory allocation and deallocation are slower than in stack memory.

- **Stack Memory**: Stack is used to store method frames and local variables. Each thread has its own stack, and the memory is organized in a last-in, first-out (LIFO) manner. Stack memory is faster but limited in size. Once a method call is completed, the stack space for local variables is freed.

### 39. **What is the `WeakReference` in Java?**

A `WeakReference` is a reference type in Java that does not prevent an object from being garbage-collected. Unlike a strong reference (the default reference type in Java), a weak reference allows the object to be collected by the garbage collector when there are no strong references to it.

- **Use case**: Weak references are commonly used in **caching** or **memory-sensitive data structures** where you want objects to be automatically discarded when memory is needed.

```java
import java.lang.ref.WeakReference;

class MyObject {
    // Some fields and methods
}

public class WeakReferenceExample {
    public static void main(String[] args) {
        MyObject obj = new MyObject();
        WeakReference<MyObject> weakRef = new WeakReference<>(obj);

        // obj can now be garbage collected when weakRef is the only reference
    }
}
```

### 40. **How do you create a memory leak in Java?**

A memory leak in Java can occur if you hold onto references to objects that are no longer needed, preventing the garbage collector from reclaiming their memory. Common ways to create a memory leak:

- Storing objects in static fields or collections, which arent cleared even after the objects are no longer needed.
- Creating circular references (e.g., two objects referencing each other) that are not cleared.
- Not releasing resources like database connections, sockets, or file streams.

**Example of a memory leak**:
```java
import java.util.ArrayList;

public class MemoryLeakExample {
    static ArrayList<MyObject> list = new ArrayList<>();
    
    public static void main(String[] args) {
        while (true) {
            list.add(new MyObject());  // Objects are never removed, causing a memory leak
        }
    }
}
```

### 41. **What is the difference between `Shallow Copy` and `Deep Copy` in Java?**

- **Shallow Copy**: A shallow copy creates a new object but does not recursively copy the objects contained within the original object. Instead, it copies references to the objects, so both the original and copied objects refer to the same objects.

  **Example**:
  ```java
  class MyObject {
      int value;
  }

  MyObject original = new MyObject();
  original.value = 10;
  MyObject shallowCopy = original; // Both point to the same object
  ```

- **Deep Copy**: A deep copy creates a new object and also recursively copies the objects contained within it. This ensures that the original and copied objects do not share any references.

  **Example**:
  ```java
  class MyObject {
      int value;
  }

  MyObject original = new MyObject();
  original.value = 10;
  MyObject deepCopy = new MyObject();
  deepCopy.value = original.value;  // New copy of the value, no shared references
  ```

**Key difference**:  
- **Shallow copy** copies references, meaning changes to nested objects affect both the original and copied objects.
- **Deep copy** creates independent objects, so changes to one do not affect the other.

### **Exception Handling:**
Here are the answers to your Java-related questions on exceptions:

### 42. **What is an exception in Java?**

An exception in Java is an event that disrupts the normal flow of the program. It is an object that represents an abnormal condition or error that occurs during the execution of a program. Exceptions can be caused by various issues such as invalid input, network failures, division by zero, or resource unavailability.

Java provides a robust exception handling mechanism to manage such situations and allow the program to recover or terminate gracefully.

### 43. **What is the difference between `checked` and `unchecked` exceptions?**

- **Checked Exceptions**: These are exceptions that are checked at compile-time. The compiler forces you to handle these exceptions either using a `try-catch` block or by declaring them in the method signature using the `throws` keyword. Common examples include `IOException`, `SQLException`, etc.

- **Unchecked Exceptions**: These are exceptions that are not checked at compile-time but are checked at runtime. They are subclasses of `RuntimeException` and do not need to be explicitly handled. Examples include `NullPointerException`, `ArrayIndexOutOfBoundsException`, etc.

**Key Difference**:
- **Checked Exceptions** must be explicitly handled or declared.
- **Unchecked Exceptions** can be optionally handled and are not required to be declared.

### 44. **How do you handle exceptions in Java?**

Exceptions in Java are handled using a combination of `try`, `catch`, and `finally` blocks:

1. **`try` block**: You write code that might throw an exception in the `try` block.
2. **`catch` block**: If an exception occurs, it is caught by the `catch` block, where you can handle it (e.g., logging the error or retrying).
3. **`finally` block**: Code inside the `finally` block is always executed, regardless of whether an exception was thrown or not. It is typically used for cleanup operations (e.g., closing files or releasing resources).

**Example**:
```java
try {
    int result = 10 / 0;  // Will throw ArithmeticException
} catch (ArithmeticException e) {
    System.out.println("Error: " + e.getMessage());
} finally {
    System.out.println("This block is always executed.");
}
```

### 45. **What is the purpose of `try`, `catch`, `finally` blocks in Java?**

- **`try` block**: Encapsulates code that might throw an exception. It defines a scope where the exception might occur.
- **`catch` block**: Handles the exception if it occurs within the `try` block. You can specify the type of exception to catch.
- **`finally` block**: Executes code after the `try` and `catch` blocks, regardless of whether an exception was thrown or not. It is commonly used for cleanup operations, such as closing database connections or releasing resources.

### 46. **What is the difference between `throw` and `throws` in Java?**

- **`throw`**: It is used to explicitly throw an exception from a method or block of code. You can throw both checked and unchecked exceptions using `throw`.

  **Example**:
  ```java
  throw new ArithmeticException("Cannot divide by zero");
  ```

- **`throws`**: It is used in the method signature to declare that a method might throw one or more exceptions. This is mainly used for checked exceptions. The caller of the method must handle or declare the exception.

  **Example**:
  ```java
  public void readFile() throws IOException {
      // code that may throw IOException
  }
  ```

### 47. **What is a `RuntimeException`?**

`RuntimeException` is a subclass of `Exception` and represents exceptions that can occur during the runtime of the program. These exceptions are **unchecked**, meaning they do not need to be explicitly declared or handled. They usually indicate programming errors, such as logic errors, invalid input, or improper resource handling.

**Common examples**:
- `NullPointerException`
- `ArrayIndexOutOfBoundsException`
- `ArithmeticException`

### 48. **Can a `finally` block throw an exception in Java?**

Yes, a `finally` block can throw an exception in Java. However, if an exception is thrown in the `finally` block, it will override any exception that was already thrown in the `try` or `catch` block. If both the `try` block and `finally` block throw exceptions, the exception thrown by the `finally` block will be propagated to the caller.

**Example**:
```java
public void test() {
    try {
        System.out.println("In try block");
        throw new RuntimeException("Exception in try");
    } catch (Exception e) {
        System.out.println("In catch block");
        throw new RuntimeException("Exception in catch");
    } finally {
        System.out.println("In finally block");
        throw new RuntimeException("Exception in finally");
    }
}
```
In this case, the exception from the `finally` block will be propagated, even if an exception occurred in the `try` or `catch`.

### 49. **What is the `Throwable` class in Java?**

`Throwable` is the superclass of all errors and exceptions in Java. It is the root class in the exception hierarchy. `Throwable` has two main subclasses:
- **`Error`**: Represents serious issues that the application should not attempt to handle (e.g., `OutOfMemoryError`).
- **`Exception`**: Represents conditions that the application might want to catch and handle (e.g., `IOException`).

`Throwable` provides methods like `getMessage()`, `printStackTrace()`, and others to provide details about the error or exception.

### 50. **How do you create a custom exception in Java?**

To create a custom exception in Java, you need to create a new class that extends `Exception` (for checked exceptions) or `RuntimeException` (for unchecked exceptions). You can add custom constructors to pass messages or error codes.

**Example**:
```java
class MyCustomException extends Exception {
    public MyCustomException(String message) {
        super(message);
    }
}

public class TestCustomException {
    public static void main(String[] args) {
        try {
            throw new MyCustomException("This is a custom exception");
        } catch (MyCustomException e) {
            System.out.println(e.getMessage());
        }
    }
}
```

In this example, `MyCustomException` is a custom checked exception that is thrown and caught in the `main` method. The `getMessage()` method is used to print the exception message.

### **Java Collections Framework:**
Here are the answers to your Java Collections-related questions:

### 51. **What are the core interfaces in the Java Collections Framework?**

The core interfaces in the Java Collections Framework are:

1. **`Collection`**: The root interface for most collection types (e.g., `List`, `Set`, and `Queue`).
2. **`List`**: Represents an ordered collection of elements, allowing duplicate elements (e.g., `ArrayList`, `LinkedList`).
3. **`Set`**: Represents a collection that does not allow duplicate elements (e.g., `HashSet`, `TreeSet`).
4. **`Queue`**: Represents a collection designed for holding elements prior to processing (e.g., `LinkedList`, `PriorityQueue`).
5. **`Map`**: Represents an object that maps keys to values, with no duplicate keys (e.g., `HashMap`, `TreeMap`, `LinkedHashMap`).
6. **`SortedSet`** and **`NavigableSet`**: Extensions of `Set` that maintain order (e.g., `TreeSet`).
7. **`SortedMap`** and **`NavigableMap`**: Extensions of `Map` that maintain order (e.g., `TreeMap`).

These interfaces define the standard behaviors for collections in Java, while the classes (such as `ArrayList`, `HashMap`) provide the actual implementations.

### 52. **What is the difference between a `List`, `Set`, and `Map` in Java?**

- **`List`**: 
  - An ordered collection that allows duplicate elements.
  - Elements are indexed and can be accessed by position.
  - Example: `ArrayList`, `LinkedList`.

- **`Set`**: 
  - A collection that does not allow duplicate elements.
  - No guarantee of the order of elements.
  - Example: `HashSet`, `TreeSet`.

- **`Map`**: 
  - A collection that stores key-value pairs, where each key maps to a value.
  - A `Map` cannot have duplicate keys, but values can be duplicated.
  - Example: `HashMap`, `TreeMap`.

**Key Differences**:
- **`List`** allows duplicates and maintains order, while **`Set`** does not allow duplicates and may not guarantee order.
- **`Map`** stores key-value pairs, unlike `List` and `Set`, which store only individual elements.

### 53. **What is the difference between `ArrayList` and `LinkedList` in Java?**

- **`ArrayList`**:
  - Implements the `List` interface and uses an array for storage.
  - Provides fast random access to elements (`O(1)` for get/set).
  - Insertions or deletions (except at the end) can be slower due to the need to shift elements (`O(n)`).
  - Better for frequent access or modification of elements by index.

- **`LinkedList`**:
  - Implements the `List` interface and uses a doubly linked list for storage.
  - Provides slower random access to elements (`O(n)` for get/set).
  - Insertions or deletions are faster compared to `ArrayList` (`O(1)` if the position is known).
  - Better for frequent insertions or deletions of elements.

### 54. **How does a `HashMap` work in Java?**

A **`HashMap`** is an implementation of the `Map` interface that stores key-value pairs. It uses a hash table internally for efficient retrieval. The **hashing** mechanism ensures that keys are evenly distributed across the table, allowing for fast lookups, insertions, and deletions.

- **Hashing**: When a key is inserted into the `HashMap`, its hash code is computed, and the key-value pair is stored in the bucket corresponding to the hash value.
- **Collisions**: If two keys have the same hash code, they are stored in the same bucket using a linked list or balanced tree (Java 8 introduced tree nodes for long chains to improve performance).

- **Time complexity**: For typical operations (e.g., get, put), the time complexity is `O(1)` in average cases, but it can degrade to `O(n)` in cases of poor hashing or collisions.

### 55. **What is the difference between `HashMap` and `TreeMap`?**

- **`HashMap`**:
  - Does not maintain any order of the keys.
  - Provides constant-time complexity (`O(1)`) for basic operations (get, put) under ideal conditions.
  - It is not thread-safe.

- **`TreeMap`**:
  - Maintains the keys in **sorted** order (natural ordering or by a comparator).
  - Provides `O(log n)` time complexity for operations like `get`, `put`, and `remove` because it uses a red-black tree internally.
  - It is also not thread-safe.

**Key Difference**: 
- **`HashMap`** is faster for basic operations, but **`TreeMap`** is useful when you need to maintain order among keys.

### 56. **What is the difference between `HashSet` and `TreeSet`?**

- **`HashSet`**:
  - Implements the `Set` interface and stores elements in an unordered way using a hash table.
  - Does not maintain any order of elements.
  - Provides constant-time complexity (`O(1)`) for operations like add, remove, and contains under ideal conditions.

- **`TreeSet`**:
  - Implements the `Set` interface and stores elements in a **sorted** order, either natural order or using a provided comparator.
  - Operations like add, remove, and contains have a time complexity of `O(log n)` because it uses a red-black tree.

**Key Difference**: 
- **`HashSet`** is faster for basic operations but does not maintain order, while **`TreeSet`** maintains a sorted order of elements.

### 57. **What is the difference between `Iterator` and `ListIterator`?**

- **`Iterator`**:
  - Provides methods to iterate over elements in a collection (e.g., `hasNext()`, `next()`, `remove()`).
  - Can iterate in only one direction (forward).
  - Can be used on all collections that implement the `Collection` interface.

- **`ListIterator`**:
  - Extends `Iterator` and provides additional methods to iterate both forward and backward through a list (e.g., `hasPrevious()`, `previous()`).
  - Allows modification of elements while iterating (e.g., `set()`, `add()`).
  - Can only be used with **`List`** collections like `ArrayList` and `LinkedList`.

**Key Difference**: 
- **`ListIterator`** allows bidirectional iteration and element modification, while **`Iterator`** only supports forward iteration.

### 58. **How do you sort a `List` in Java?**

You can sort a `List` in Java using the `Collections.sort()` method or by using `List.sort()` (introduced in Java 8).

- **Using `Collections.sort()`**:
  ```java
  List<Integer> list = Arrays.asList(5, 3, 8, 1);
  Collections.sort(list);  // Sorts in ascending order
  ```

- **Using `List.sort()`** (Java 8 and above):
  ```java
  list.sort(Comparator.naturalOrder());  // Sorts in ascending order
  ```

- **Custom sorting**: You can provide a custom comparator for sorting in a specific order:
  ```java
  list.sort((a, b) -> b - a);  // Sorts in descending order
  ```

### 59. **What is the `Comparable` interface in Java?**

The `Comparable` interface is used to define a natural ordering of objects. A class that implements the `Comparable` interface must define the `compareTo(T o)` method, which compares the current object with another object of the same type.

**Example**:
```java
class Person implements Comparable<Person> {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public int compareTo(Person other) {
        return Integer.compare(this.age, other.age);  // Sort by age
    }
}
```

**Key Points**:
- `compareTo()` returns a negative value if the current object is less than the other, zero if they are equal, and a positive value if the current object is greater.

### 60. **What is the `Comparator` interface, and how does it differ from `Comparable`?**

The **`Comparator`** interface is used to define an external comparison logic to compare two objects. It is often used when you need to sort objects in multiple ways, or the class does not implement `Comparable`.

- **`compare(T o1, T o2)`** method compares two objects.
- **`Comparator`** is typically used when you need different sorting strategies for the same class or to sort a class that does not implement `Comparable`.

**Key Difference**:
- **`Comparable`** is used to define the natural ordering of objects in a class, and the comparison logic is implemented in the class itself.
- **`Comparator`** is used to define custom ordering externally without modifying the class.

### **Java Streams and Lambda Expressions:**
Here are the answers to your Java Lambda expressions, Streams, and Optional class-related questions:

### 61. **What are Lambda expressions in Java?**

Lambda expressions in Java are a feature introduced in Java 8 that allow you to write concise, functional-style code. A lambda expression provides a clear and concise way to represent one method interface (functional interface) using an expression. It enables passing behavior as a parameter, making it easier to write more flexible and readable code.

**Syntax**:
```java
(parameters) -> expression
```

### 62. **How do you define a Lambda expression in Java?**

A Lambda expression is defined as a combination of parameters, the `->` symbol (which separates parameters from the body), and an expression or block of code.

**Basic syntax**:
```java
(parameters) -> expression
```

**Example**:
```java
// Lambda expression for addition
(int a, int b) -> a + b
```

If there is only one parameter, the parentheses can be omitted:
```java
x -> x * 2  // Multiplies the input by 2
```

Lambda expressions are often used to implement functional interfaces, which have exactly one abstract method.

**Example in use**:
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4);
numbers.forEach(number -> System.out.println(number));  // Using lambda expression in forEach
```

### 63. **What is the difference between `Function` and `Consumer` interfaces in Java?**

Both `Function` and `Consumer` are functional interfaces in Java, but they serve different purposes:

- **`Function<T, R>`**: Represents a function that takes an argument of type `T` and returns a result of type `R`. It has one method: `R apply(T t)`.
  - **Example**: Convert an integer to its square:
    ```java
    Function<Integer, Integer> square = x -> x * x;
    System.out.println(square.apply(5));  // Output: 25
    ```

- **`Consumer<T>`**: Represents an operation that takes an argument of type `T` and returns no result (void). It is used for operations that perform actions on the argument without returning any result.
  - **Example**: Print an integer:
    ```java
    Consumer<Integer> print = x -> System.out.println(x);
    print.accept(5);  // Output: 5
    ```

**Key Difference**: 
- `Function` produces a result based on the input, while `Consumer` performs an action and does not return any result.

### 64. **What is the purpose of the `Stream` API in Java?**

The **`Stream`** API, introduced in Java 8, provides a high-level abstraction for working with sequences of elements (e.g., collections) in a functional style. It allows you to process data in a declarative manner using operations like filtering, mapping, sorting, and reducing. 

Streams support parallel processing, making it easier to perform operations concurrently on large datasets. They are used for processing collections of objects and can simplify code by allowing operations to be chained together.

### 65. **How do you filter a collection using streams in Java?**

You can filter a collection using the `filter()` method in the `Stream` API. This method takes a `Predicate` (a functional interface that returns a boolean value) to evaluate each element and decide whether to include it in the result.

**Example**:
```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6);
List<Integer> evenNumbers = numbers.stream()
                                   .filter(n -> n % 2 == 0)
                                   .collect(Collectors.toList());
System.out.println(evenNumbers);  // Output: [2, 4, 6]
```

Here, `filter()` is used to keep only the even numbers from the list.

### 66. **What is the difference between `map()` and `flatMap()` in Java streams?**

- **`map()`**: It transforms each element of the stream by applying a function to it, producing a new stream of elements. The result of the `map()` function is a stream of the transformed elements.

  **Example**:
  ```java
  List<String> words = Arrays.asList("apple", "banana", "cherry");
  List<Integer> lengths = words.stream()
                               .map(String::length)
                               .collect(Collectors.toList());
  System.out.println(lengths);  // Output: [5, 6, 6]
  ```

- **`flatMap()`**: It is used when the transformation function returns a stream of elements, rather than a single element. It flattens the nested streams into a single stream.

  **Example**:
  ```java
  List<List<String>> lists = Arrays.asList(Arrays.asList("a", "b"), Arrays.asList("c", "d"));
  List<String> flattened = lists.stream()
                                .flatMap(List::stream)
                                .collect(Collectors.toList());
  System.out.println(flattened);  // Output: [a, b, c, d]
  ```

**Key Difference**:
- **`map()`** transforms each element into a single value, resulting in a stream of transformed elements.
- **`flatMap()`** transforms each element into a stream and then flattens the resulting streams into one.

### 67. **What is the `Optional` class in Java?**

The **`Optional`** class is a container object that may or may not contain a non-null value. It is used to avoid `NullPointerException` by explicitly handling cases where a value may be absent.

- **`Optional`** provides methods like `isPresent()`, `ifPresent()`, `get()`, and `orElse()` to check if a value exists and retrieve it if present.
  
**Example**:
```java
Optional<String> name = Optional.ofNullable("John");
System.out.println(name.isPresent());  // Output: true
System.out.println(name.orElse("Unknown"));  // Output: John
```

**Key Point**: `Optional` is useful for handling null values in a clean and expressive way.

### 68. **How do you use `Collectors` in Java streams?**

The `Collectors` class in Java provides various static methods that are used to collect the elements of a stream into a different form, such as a `List`, `Set`, `Map`, or a single summary result (like sum, average, etc.).

Common methods:
- **`toList()`**: Collects the stream into a `List`.
- **`toSet()`**: Collects the stream into a `Set`.
- **`joining()`**: Concatenates the elements into a single string.
- **`groupingBy()`**: Groups the elements of the stream by a classifier function.
- **`partitioningBy()`**: Partitions the elements of the stream into two groups based on a predicate.

**Example**:
```java
List<String> words = Arrays.asList("apple", "banana", "cherry");
List<String> upperCaseWords = words.stream()
                                   .map(String::toUpperCase)
                                   .collect(Collectors.toList());
System.out.println(upperCaseWords);  // Output: [APPLE, BANANA, CHERRY]
```

### 69. **What is the difference between `reduce()` and `collect()` methods in Java streams?**

- **`reduce()`**: The `reduce()` method is used to perform a reduction operation on the elements of the stream, which produces a single result (e.g., sum, product). It takes an associative accumulation function and a starting value (optional). The operation is performed iteratively over the stream elements.

  **Example**:
  ```java
  List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
  int sum = numbers.stream()
                   .reduce(0, Integer::sum);
  System.out.println(sum);  // Output: 15
  ```

- **`collect()`**: The `collect()` method is a terminal operation that transforms the elements of the stream into a different form, usually a collection like a `List`, `Set`, or `Map`. It uses a `Collector` (e.g., `Collectors.toList()`).

  **Example**:
  ```java
  List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
  List<Integer> squares = numbers.stream()
                                 .map(x -> x * x)
                                 .collect(Collectors.toList());
  System.out.println(squares);  // Output: [1, 4, 9, 16, 25]
  ```

**Key Difference**:
- **`reduce()`** is used for reducing the stream into a single result.
- **`collect()`** is used to gather the stream elements into a collection or other data structures.

### **Concurrency and Multithreading:**
Here are the answers to your questions related to threads and multithreading in Java:

### 70. **What is the difference between process and thread in Java?**

- **Process**: A process is an independent program that runs in its own memory space. It is the execution of a program that is isolated from other processes. A process may contain multiple threads.
- **Thread**: A thread is the smallest unit of execution within a process. Threads share the same memory space of the process they belong to, making them lightweight compared to processes. Multiple threads within a process can run concurrently and share resources such as memory.

**Key Difference**: Processes run independently, while threads run within a process and share the same resources.

### 71. **What is multithreading in Java? Explain with an example.**

**Multithreading** in Java refers to the concurrent execution of two or more threads within a single process. Java provides built-in support for multithreading, allowing programs to perform multiple tasks simultaneously.

**Example**:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println(Thread.currentThread().getId() + " is executing");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
        t1.start(); // Starts thread 1
        t2.start(); // Starts thread 2
    }
}
```
In this example, two threads are created and executed concurrently.

### 72. **What is the `Thread` class in Java?**

The **`Thread`** class in Java is part of the `java.lang` package, and it is used to create and manage threads. It provides several methods for managing thread execution, such as `start()`, `sleep()`, `join()`, and `interrupt()`. By extending the `Thread` class, you can define the code that will run in a thread by overriding its `run()` method.

**Example**:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t = new MyThread();
        t.start(); // Starts the thread
    }
}
```

### 73. **What is the `Runnable` interface in Java?**

The **`Runnable`** interface is a functional interface in Java that represents a task to be executed by a thread. It has a single abstract method `run()`, which defines the code to be executed by the thread. You can implement `Runnable` if you don't want to extend the `Thread` class.

**Example**:
```java
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyRunnable task = new MyRunnable();
        Thread t = new Thread(task);
        t.start(); // Starts the thread
    }
}
```

### 74. **How do you create a thread in Java?**

In Java, you can create a thread in two ways:
1. **By extending the `Thread` class**: Override the `run()` method to define the code to be executed by the thread.
2. **By implementing the `Runnable` interface**: Implement the `run()` method and pass it to a `Thread` object.

**Example 1 (Extending `Thread` class)**:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t = new MyThread();
        t.start(); // Starts the thread
    }
}
```

**Example 2 (Implementing `Runnable` interface)**:
```java
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running");
    }
}

public class Main {
    public static void main(String[] args) {
        MyRunnable task = new MyRunnable();
        Thread t = new Thread(task);
        t.start(); // Starts the thread
    }
}
```

### 75. **What is synchronization in Java, and why is it important?**

**Synchronization** in Java is a mechanism that ensures that only one thread can access a particular resource (or code block) at a time. It is used to prevent thread interference and memory consistency errors in a multi-threaded environment.

It is important because:
- It ensures that shared resources are accessed by only one thread at a time.
- It prevents inconsistent data due to concurrent modifications by multiple threads.

### 76. **What is the `synchronized` keyword in Java?**

The **`synchronized`** keyword in Java is used to define a block of code or a method that can only be executed by one thread at a time. It is used to ensure that shared resources are accessed in a thread-safe manner.

**Example**:
```java
class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++;
    }
}

public class Main {
    public static void main(String[] args) {
        Counter counter = new Counter();
        counter.increment(); // The increment method is synchronized
    }
}
```
Here, `increment()` is a synchronized method that ensures only one thread can modify `count` at a time.

### 77. **What is the difference between `wait()` and `sleep()` in Java?**

- **`wait()`**: It is used to make a thread pause execution until it is notified by another thread. It is called on an object, and the thread releases the lock on the object while waiting.
- **`sleep()`**: It pauses the execution of the current thread for a specified amount of time, without releasing the lock. It is called on the `Thread` class.

**Key Difference**: `wait()` is used for thread communication (inter-thread synchronization), while `sleep()` is used to pause the current threads execution for a given duration.

### 78. **What are the thread states in Java?**

A thread in Java can be in one of the following states:
1. **New**: The thread is created but not yet started.
2. **Runnable**: The thread is ready to run and is waiting for CPU time.
3. **Blocked**: The thread is blocked and waiting for a resource (e.g., a synchronized block).
4. **Waiting**: The thread is waiting indefinitely for another thread to perform a particular action.
5. **Timed Waiting**: The thread is waiting for a specific period (e.g., using `sleep()` or `join()`).
6. **Terminated**: The thread has finished execution.

### 79. **What is a deadlock in Java, and how can you prevent it?**

A **deadlock** occurs when two or more threads are blocked indefinitely, each waiting for the other to release a resource. This situation causes the threads to never proceed.

**To prevent deadlock**:
- Avoid nested locks.
- Lock resources in a consistent order.
- Use a timeout to acquire locks, allowing the thread to give up if it cannot acquire the lock in time.

**Example**: Two threads waiting for each other to release locks on different resources can cause a deadlock.

### 80. **What is the `ExecutorService` in Java?**

The **`ExecutorService`** is part of the `java.util.concurrent` package and provides a higher-level replacement for managing threads. It simplifies the process of thread management by allowing you to submit tasks for execution and manage thread pooling efficiently.

It provides methods like `submit()`, `invokeAll()`, and `shutdown()` to manage the execution of tasks. The `ExecutorService` uses thread pools, which helps in improving performance by reusing existing threads instead of creating new ones for each task.

**Example**:
```java
ExecutorService executor = Executors.newFixedThreadPool(2);
executor.submit(() -> System.out.println("Task 1"));
executor.submit(() -> System.out.println("Task 2"));
executor.shutdown();
```
In this example, two tasks are submitted for execution in a fixed thread pool, and the executor shuts down after the tasks are completed.

### **Java I/O (Input/Output):**
Here are the answers to your questions regarding Java I/O, serialization, and NIO:

### 81. **What is the difference between `InputStream` and `Reader` in Java?**

- **`InputStream`**: It is an abstract class used for reading byte-based input. It reads data in the form of bytes (8-bit data) and is used for binary data such as images or audio files.
  - Example classes: `FileInputStream`, `ByteArrayInputStream`.

- **`Reader`**: It is an abstract class used for reading character-based input. It reads data in the form of characters (16-bit data) and is used for text files.
  - Example classes: `FileReader`, `BufferedReader`.

**Key Difference**: `InputStream` handles byte data, while `Reader` handles character data.

---

### 82. **What is serialization in Java?**

**Serialization** is the process of converting an object's state into a byte stream so that it can be easily stored in a file or transmitted over a network. The serialized object can be later deserialized (reconstructed back) into its original state.

---

### 83. **How do you serialize and deserialize an object in Java?**

- **Serialization**: You use the `ObjectOutputStream` class to serialize an object by writing it to a stream.
- **Deserialization**: You use the `ObjectInputStream` class to deserialize the object by reading it from a stream.

**Example**:
```java
import java.io.*;

class Person implements Serializable {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class SerializationExample {
    public static void main(String[] args) throws IOException, ClassNotFoundException {
        // Serialization
        Person p = new Person("Alice", 25);
        FileOutputStream fileOut = new FileOutputStream("person.ser");
        ObjectOutputStream out = new ObjectOutputStream(fileOut);
        out.writeObject(p);
        out.close();
        fileOut.close();

        // Deserialization
        FileInputStream fileIn = new FileInputStream("person.ser");
        ObjectInputStream in = new ObjectInputStream(fileIn);
        Person deserializedPerson = (Person) in.readObject();
        in.close();
        fileIn.close();
        System.out.println("Name: " + deserializedPerson.name + ", Age: " + deserializedPerson.age);
    }
}
```

---

### 84. **What is the `Serializable` interface in Java?**

The **`Serializable`** interface is a marker interface (it doesn't have any methods) in Java that marks a class as being capable of being serialized. If a class implements this interface, its objects can be serialized into a byte stream and later deserialized.

---

### 85. **What is the purpose of `transient` keyword in Java serialization?**

The **`transient`** keyword is used to indicate that a field of a class should not be serialized. When an object is serialized, any field marked as `transient` will not be included in the serialized data.

**Example**:
```java
class Person implements Serializable {
    String name;
    transient int age; // This field will not be serialized

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```
In this example, the `age` field will not be serialized because it is marked as `transient`.

---

### 86. **What is the difference between `BufferedReader` and `FileReader`?**

- **`FileReader`**: It is a low-level class that reads characters from a file. It reads one character at a time.
- **`BufferedReader`**: It wraps around a `Reader` (like `FileReader`) and provides buffering for efficient reading of characters, arrays, and lines. It improves performance by reducing the number of I/O operations.

**Key Difference**: `BufferedReader` is more efficient for reading data line-by-line or large chunks of data, while `FileReader` reads data one character at a time.

---

### 87. **How do you read and write data to files in Java?**

To read and write files in Java:
- **Reading**: Use classes like `FileReader`, `BufferedReader`, `FileInputStream`, or `Scanner`.
- **Writing**: Use classes like `FileWriter`, `BufferedWriter`, `FileOutputStream`, or `PrintWriter`.

**Example (Reading)**:
```java
import java.io.*;

public class ReadFile {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new FileReader("file.txt"));
        String line;
        while ((line = reader.readLine()) != null) {
            System.out.println(line);
        }
        reader.close();
    }
}
```

**Example (Writing)**:
```java
import java.io.*;

public class WriteFile {
    public static void main(String[] args) throws IOException {
        BufferedWriter writer = new BufferedWriter(new FileWriter("file.txt"));
        writer.write("Hello, Java!");
        writer.close();
    }
}
```

---

### 88. **What are the differences between `FileInputStream` and `FileOutputStream` in Java?**

- **`FileInputStream`**: Used to read data from a file as a byte stream. It is used for reading binary data (e.g., image or audio files).
- **`FileOutputStream`**: Used to write data to a file as a byte stream. It is used for writing binary data.

**Key Difference**: `FileInputStream` is for reading data, while `FileOutputStream` is for writing data.

---

### 89. **What is NIO (New I/O) in Java, and how is it different from traditional I/O?**

**NIO (New I/O)** is a more scalable and flexible I/O API introduced in Java 1.4, found in the `java.nio` package. It provides faster I/O operations and offers non-blocking, buffer-based I/O operations, and file channel operations. NIO is designed for handling large volumes of data, such as reading/writing large files and handling multiple clients in networking applications.

**Key Differences**:
- **Blocking vs. Non-Blocking**: Traditional I/O is blocking, while NIO supports non-blocking I/O operations.
- **Buffer-based I/O**: NIO uses buffers to hold data, making it more efficient than traditional I/O which reads/writes byte-by-byte.

---

### 90. **What is the `Path` class in Java NIO?**

The **`Path`** class, introduced in Java 7, is part of the `java.nio.file` package and represents a path in the filesystem. It can be used to manipulate file and directory paths, and it offers various methods for file operations, such as `resolve()`, `normalize()`, `getFileName()`, and `toAbsolutePath()`.

**Example**:
```java
import java.nio.file.*;

public class PathExample {
    public static void main(String[] args) {
        Path path = Paths.get("C:/Users/Java/Example.txt");
        System.out.println("File name: " + path.getFileName());
        System.out.println("Absolute path: " + path.toAbsolutePath());
    }
}
```

In this example, the `Path` class is used to represent a file path, and you can manipulate it using various methods provided by the class.

### **Java 8 and Later Features:**
Here are the answers to your Java 8, Java 9, and Java 10-related questions:

### 91. **What are the new features introduced in Java 8?**

Java 8 introduced several significant features, including:
1. **Lambda Expressions**: Allows you to pass behavior as arguments to methods, enabling functional programming.
2. **Streams API**: Provides a way to process sequences of elements (e.g., collections) in a declarative manner.
3. **Default Methods in Interfaces**: Enables interfaces to have methods with implementations.
4. **Method References**: A shorthand notation for calling methods via a reference to them.
5. **Optional Class**: Helps to avoid null pointer exceptions by representing the presence or absence of a value.
6. **New Date and Time API**: Introduced the `java.time` package to simplify date-time operations.
7. **Nashorn JavaScript Engine**: Allows executing JavaScript code within Java applications.
8. **Parallel Streams**: Enables parallel processing of data using the Streams API.

---

### 92. **How do you use `default` methods in interfaces in Java 8?**

**Default methods** in interfaces allow you to provide a method body inside the interface itself. They can be called just like regular methods of a class but are part of the interface. This helps to add new methods to interfaces without breaking existing code.

**Example**:
```java
interface MyInterface {
    default void printMessage() {
        System.out.println("Default method in interface");
    }
}

class MyClass implements MyInterface {
    // No need to override printMessage(), as it's a default method
}

public class Main {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.printMessage(); // Calls the default method
    }
}
```

---

### 93. **What is the significance of the `Stream` API in Java 8?**

The **Stream API** in Java 8 provides a new abstraction for processing sequences of elements, such as collections, in a functional and declarative style. The primary benefits are:
- **Laziness**: Streams can be processed lazily, meaning computations are deferred until the result is needed.
- **Parallelism**: Streams can be processed in parallel with minimal effort, improving performance.
- **Concise and Readable Code**: The API simplifies processing large amounts of data through functional-style operations like `filter()`, `map()`, and `reduce()`.

**Example**:
```java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
names.stream().filter(name -> name.startsWith("A")).forEach(System.out::println);  // Output: Alice
```

---

### 94. **What are `Method References` in Java 8?**

**Method References** in Java 8 are a shorthand for calling methods via a reference to the method. They can be used where a lambda expression calls a method.

There are four types of method references:
1. **Reference to a static method**: `ClassName::staticMethodName`
2. **Reference to an instance method of a specific object**: `instance::instanceMethod`
3. **Reference to an instance method of an arbitrary object of a particular type**: `ClassName::instanceMethod`
4. **Reference to a constructor**: `ClassName::new`

**Example**:
```java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
names.forEach(System.out::println);  // Equivalent to names.forEach(name -> System.out.println(name))
```

---

### 95. **What is the purpose of the `Optional` class in Java 8?**

The **`Optional`** class in Java 8 is used to represent a value that might or might not be present. It helps to avoid `NullPointerException` by explicitly handling the case where a value could be absent.

Methods like `isPresent()`, `ifPresent()`, and `orElse()` are used to check and handle values.

**Example**:
```java
Optional<String> name = Optional.of("Alice");
System.out.println(name.orElse("Unknown"));  // Output: Alice

Optional<String> emptyName = Optional.empty();
System.out.println(emptyName.orElse("Unknown"));  // Output: Unknown
```

---

### 96. **What are `CompletableFuture` and `Future` in Java?**

- **`Future`**: Represents the result of an asynchronous computation. It provides methods like `get()`, `cancel()`, and `isDone()` to work with asynchronous tasks.
- **`CompletableFuture`**: Extends `Future` and adds features for completing asynchronous tasks manually. It also provides methods for combining multiple futures, handling exceptions, and executing tasks in parallel.

**Example**:
```java
CompletableFuture<Integer> future = CompletableFuture.supplyAsync(() -> 42);
future.thenApply(result -> result * 2).thenAccept(System.out::println);  // Output: 84
```

---

### 97. **How do you use `LocalDate`, `LocalTime`, and `LocalDateTime` in Java 8?**

Java 8 introduced the **`java.time`** package for handling dates and times more effectively:

- **`LocalDate`**: Represents a date without a time zone (e.g., 2024-12-03).
- **`LocalTime`**: Represents a time without a date (e.g., 10:30 AM).
- **`LocalDateTime`**: Represents both a date and a time (e.g., 2024-12-03T10:30).

**Example**:
```java
LocalDate date = LocalDate.now();
LocalTime time = LocalTime.now();
LocalDateTime dateTime = LocalDateTime.now();
System.out.println(date);  // Output: 2024-12-03
System.out.println(time);  // Output: 10:30
System.out.println(dateTime);  // Output: 2024-12-03T10:30
```

---

### 98. **What is the `DateTimeFormatter` class in Java?**

The **`DateTimeFormatter`** class is used to format and parse dates and times. It allows you to convert `LocalDate`, `LocalTime`, and `LocalDateTime` objects to strings and vice versa.

**Example**:
```java
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");
LocalDate date = LocalDate.now();
System.out.println(date.format(formatter));  // Output: 2024-12-03
```

---

### 99. **How does Java 9’s module system work?**

Java 9 introduced the **module system**, which allows developers to modularize their applications. The key components of the module system are:
1. **Modules**: Encapsulate packages and make them available to other modules.
2. **`module-info.java`**: A special file in the root of a module that defines its name, dependencies, and exported packages.
3. **Dependencies**: A module can declare dependencies on other modules.

**Example (`module-info.java`)**:
```java
module mymodule {
    requires java.base;  // Dependency on the java.base module
    exports com.example;  // Exports the com.example package
}
```

---

### 100. **What is the `var` keyword introduced in Java 10?**

The **`var`** keyword in Java 10 allows local variable type inference. The compiler infers the type of the variable based on the assigned value. It simplifies code, especially in cases of complex generic types.

**Example**:
```java
var number = 42;  // Inferred as int
var message = "Hello, Java!";  // Inferred as String
```

**Key Point**: The `var` keyword can only be used for local variables with an initializer, and the type must be determinable from the context.

### **Java Frameworks (Bonus):**
### **1. Explain the concept of Spring Framework and its major components.**

The **Spring Framework** is an open-source framework that provides comprehensive infrastructure support for developing Java applications. It simplifies the development of Java applications by offering solutions to common challenges such as dependency injection, transaction management, and aspect-oriented programming. It is designed to promote loose coupling and ease of testing.

**Major Components of Spring:**
- **Core Container**: Contains the fundamental features of Spring, including:
  - **Beans**: Central to the Spring IoC (Inversion of Control) container. Manages objects and their dependencies.
  - **Context**: A configuration container that holds bean definitions and provides access to them. Typically, it uses an application context.
  - **Expression Language (SpEL)**: A powerful language for querying and manipulating objects at runtime.
- **Spring AOP (Aspect-Oriented Programming)**: Allows separation of cross-cutting concerns (such as logging or security) from business logic, improving modularity.
- **Spring Data Access**: Provides simplified integration with databases through JDBC, JPA, Hibernate, and other persistence technologies.
- **Spring Web**: A comprehensive module for building web applications, including both traditional MVC-based web apps and RESTful APIs.
- **Spring Security**: Handles authentication and authorization in web applications, supporting a wide range of authentication mechanisms.
- **Spring Test**: Provides support for testing Spring-based applications, including integration tests.

---

### **2. What is Spring Boot, and how does it differ from traditional Spring?**

**Spring Boot** is an extension of the Spring Framework that simplifies the setup and development of Spring applications by providing default configurations and an embedded server (like Tomcat or Jetty). It eliminates the need for complex XML configurations and manual setup of various components.

**Key Differences Between Spring Boot and Traditional Spring:**
- **Auto Configuration**: Spring Boot automatically configures application components based on the libraries present in the classpath. Traditional Spring requires manual configuration, typically through XML files or annotations.
- **Embedded Server**: Spring Boot supports embedded servers (e.g., Tomcat, Jetty), meaning you don’t need to deploy your application to an external server. Traditional Spring requires you to configure a web server separately (e.g., deploying a WAR file to a servlet container).
- **Production-Ready Features**: Spring Boot comes with built-in features like health checks, metrics, and application monitoring, which are crucial for production environments.
- **Simplified Setup**: Spring Boot applications can be set up with minimal configuration and no need for complex XML-based setup, while traditional Spring may require more configuration.

**Example**: With Spring Boot, you can create a simple web app in just a few steps:
```java
@SpringBootApplication
public class Application {
    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```
This eliminates the need for many configurations and boilerplate code.

---

### **3. What is the difference between Hibernate and JPA?**

**Hibernate** and **JPA (Java Persistence API)** are both used for Object-Relational Mapping (ORM) in Java, but they differ in scope and functionality:

- **JPA** is a specification, which means it defines a standard set of interfaces and annotations for ORM, but it does not provide the implementation itself.
  - **JPA Providers**: Hibernate is one of the popular implementations of the JPA specification, but others include EclipseLink and OpenJPA.
  - JPA is part of Java EE (Enterprise Edition), now integrated into Jakarta EE.

- **Hibernate** is an ORM framework and also an implementation of the JPA specification. It provides its own set of features beyond the JPA specification.
  - **Advanced Features**: Hibernate offers additional features such as caching, query language (HQL), and session management, which are not part of the JPA standard.
  - **Compatibility**: Hibernate is fully compatible with JPA, meaning it can be used as a JPA provider.
  
**Key Differences**:
- JPA is a specification, and Hibernate is one of its implementations. You can use Hibernate as the JPA provider, or use another provider like EclipseLink.
- Hibernate offers more features beyond JPA (e.g., caching and custom query mechanisms), while JPA is focused solely on providing a standard for ORM.

---

### **4. How does Spring AOP work?**

**Spring AOP (Aspect-Oriented Programming)** is a programming paradigm that allows for the separation of cross-cutting concerns from the business logic of an application. AOP allows you to define "aspects" (such as logging, security, or transaction management) and apply them to specific points in your application without modifying the core business logic.

**Key Concepts in Spring AOP**:
- **Aspect**: A module that defines cross-cutting concerns (e.g., logging or transaction management).
- **Join Point**: A point in the program execution where an aspect can be applied (e.g., method execution).
- **Advice**: The code that is executed at a particular join point. Types of advice include:
  - **Before**: Runs before a method execution.
  - **After**: Runs after a method execution.
  - **Around**: Can run before and after the method execution, and can also prevent the method from running.
- **Pointcut**: An expression that matches one or more join points, allowing the advice to be applied at the specified points.
- **Weaving**: The process of applying aspects to the target objects (can be done at compile time, load time, or runtime).

**Example**:
```java
@Aspect
@Component
public class LoggingAspect {
    
    @Before("execution(* com.example.service.*.*(..))")
    public void logBefore(JoinPoint joinPoint) {
        System.out.println("Before method: " + joinPoint.getSignature());
    }
}
```
In this example, the `logBefore` method will run before any method in `com.example.service` package is executed.

---

### **5. What are RESTful APIs, and how are they built with Spring Boot?**

**RESTful APIs** are a type of web service that follow the principles of **Representational State Transfer (REST)**. REST is an architectural style that allows communication between systems using standard HTTP methods (GET, POST, PUT, DELETE) and standard data formats such as JSON or XML.

**Key Characteristics of RESTful APIs**:
- **Stateless**: Every request from a client must contain all the information needed to process it, and the server does not store any client context between requests.
- **Client-Server**: The client and server are separate, and communication happens over HTTP.
- **Uniform Interface**: The API should have a consistent, well-defined interface (usually defined via URLs).
- **Cacheable**: Responses can be marked as cacheable or non-cacheable, allowing for performance optimization.

**Building a RESTful API with Spring Boot**:
Spring Boot provides tools and libraries to easily create RESTful APIs. You can use the `@RestController` annotation to define your endpoints, and `@RequestMapping` or other HTTP-specific annotations to map the methods to specific HTTP requests.

**Example**:
```java
@RestController
@RequestMapping("/api/users")
public class UserController {

    @GetMapping("/{id}")
    public ResponseEntity<User> getUser(@PathVariable Long id) {
        User user = userService.findById(id);
        if (user == null) {
            return ResponseEntity.notFound().build();
        }
        return ResponseEntity.ok(user);
    }

    @PostMapping
    public ResponseEntity<User> createUser(@RequestBody User user) {
        User createdUser = userService.save(user);
        return ResponseEntity.status(HttpStatus.CREATED).body(createdUser);
    }
}
```
- **`@RestController`**: Marks the class as a RESTful controller where each method returns a response directly (no need for `@ResponseBody`).
- **`@GetMapping`, `@PostMapping`, etc.**: Specific HTTP method mappings for creating GET, POST, PUT, DELETE endpoints.
- **`@RequestBody`**: Binds the request body to a method parameter (e.g., JSON data).
- **`@PathVariable`**: Extracts variables from the URL (e.g., `/users/{id}`).

This way, Spring Boot enables the rapid development of RESTful APIs that are easy to consume and test.