# 🌟 Object-Oriented Programming (OOP) Notes

## 🏛️ The Four Pillars of OOP

Object-Oriented Programming is a paradigm that organizes code into objects. It is built on four key principles:

### 1️⃣ Encapsulation 🔒

**Definition:**  
Encapsulation bundles data and methods into a class, restricting direct access and ensuring controlled interaction.

**Example:**

```java
class BankAccount {
    private double balance; // Encapsulated data

    public BankAccount(double balance) { // Constructor
        this.balance = balance;
    }

    public void deposit(double amount) { // Method
        if (amount > 0) {
            balance += amount;
        }
    }

    public double getBalance() { // Getter, Setters
        return balance;
    }
}
```

🔹 _Private variables prevent unauthorized access, and public methods control how data is modified._
| Modifier | Class | Package | Subclass | World |
|-------------|:-----:|:-------:|:--------:|:------:|
| `private` | ✅ | ❌ | ❌ | ❌ |
| _(default)_ | ✅ | ✅ | ❌ | ❌ |
| `protected` | ✅ | ✅ | ✅ | ❌ |
| `public` | ✅ | ✅ | ✅ | ✅ |

---

### 2️⃣ Inheritance 🧬

**Definition:**  
Inheritance allows a class (child) to inherit fields and methods from another class (parent), promoting code reuse and creating a relationship between the parent and child classes.

**Example:**

```java
class Animal {
    void makeSound() {
        System.out.println("Some generic sound");
    }
}

class Dog extends Animal {  // 'Dog' inherits from 'Animal'
    @Override
    void makeSound() {
        System.out.println("Bark!");
        super.makeSound();  // Calls the parent class method
    }
}
```

🔹 The `Dog` class inherits from `Animal` using the `extends` keyword and overrides the `makeSound()` method. The `super.makeSound()` calls the `makeSound()` method from the parent class `Animal`.

---

### 3️⃣ Polymorphism 🎭

**Definition:**  
Polymorphism means many shapes — it allows you to use the same method or interface, but have it behave differently depending on the object that calls it.

**Example (Method Overriding):**

```java
// Superclass
class Animal {
    void sound() {
        System.out.println("Animal makes a sound");
    }
}

// Subclass Dog
class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

// Subclass Cat
class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}
```

🔹 _The `draw()` method is overridden in the `Circle` class, allowing different behaviors for different objects._

**Example (Method Overloading):**

```java
class MathUtils {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }
}
```

🔹 _The `add` method works with both integers and doubles (same method name, different parameters)._

---

### 4️⃣ Abstraction 🎭🚪

**Definition:**  
Abstraction hides implementation details and only exposes essential features.

_It allows you to focus on WHAT an object does instead of HOW it does it._

**Example (Abstract Class):**

```java
abstract class Vehicle {
    abstract void start();
}

class Car extends Vehicle {
    @Override
    void start() {
        System.out.println("Car is starting...");
    }
}
```

🔹 _The `Vehicle` class defines `start()` but doesn't implement it—forcing subclasses to provide their own implementation._

---

## 🏆 Why Use OOP?

✅ Code Reusability  
✅ Scalability & Maintainability  
✅ Improved Security (Encapsulation)  
✅ Easy Troubleshooting & Debugging

---
