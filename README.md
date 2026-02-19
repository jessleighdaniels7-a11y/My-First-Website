# My-First-Website
The webpage I build with React is about OOP and the principles of OOP.
# 🧠 Object-Oriented Programming — Four Core Principles

> An interactive React app that defines and demonstrates the four pillars of OOP with Python code examples.

---

## 📖 Overview

This project is a single-page React application built to visually explore the four core principles of Object-Oriented Programming (OOP). Each principle includes a clear definition and a working Python code example, with a tabbed interface for easy navigation.

---

## ✨ Features

- 🗂 Tabbed navigation for each OOP principle
- 📖 Plain-English definitions for each concept
- 🐍 Python code examples with syntax highlighting
- 📋 Copy-to-clipboard button for each code snippet
- 🎨 Color-coded principle themes

---

## 🔑 The Four OOP Principles

### 🔒 Encapsulation
Bundling data and the methods that operate on it into a single class, while restricting direct access to internal state.

```python
class BankAccount:
    def __init__(self, owner, balance):
        self.__owner = owner        # Private attribute
        self.__balance = balance    # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount

    def get_balance(self):
        return self.__balance       # Controlled access

account = BankAccount("Alice", 1000)
account.deposit(500)
print(account.get_balance())  # Output: 1500
# print(account.__balance)    # Error! Private attribute
```

---

### 🧩 Abstraction
Hiding complex implementation details and exposing only the essential features of an object.

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass  # No implementation here — just the contract

    @abstractmethod
    def perimeter(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * self.radius ** 2

    def perimeter(self):
        return 2 * 3.14159 * self.radius

c = Circle(5)
print(c.area())       # Output: 78.53975
print(c.perimeter())  # Output: 31.4159
```

---

### 🧬 Inheritance
Allowing a child class to acquire properties and behaviors from a parent class, promoting code reuse and modeling "is-a" relationships.

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "Some sound"

    def describe(self):
        return f"I am {self.name}"

class Dog(Animal):          # Dog inherits from Animal
    def speak(self):
        return "Woof!"

class Cat(Animal):          # Cat inherits from Animal
    def speak(self):
        return "Meow!"

dog = Dog("Rex")
cat = Cat("Whiskers")

print(dog.describe())  # Output: I am Rex      (inherited method)
print(dog.speak())     # Output: Woof!         (overridden method)
print(cat.speak())     # Output: Meow!
```

---

### 🔀 Polymorphism
Allowing objects of different classes to be treated as objects of a common base class — where the same method name behaves differently depending on the object calling it.

```python
class Bird:
    def sound(self):
        return "Tweet!"

class Duck(Bird):
    def sound(self):
        return "Quack!"

class Parrot(Bird):
    def sound(self):
        return "Polly wants a cracker!"

# Polymorphism in action:
birds = [Bird(), Duck(), Parrot()]

for bird in birds:
    print(bird.sound())
# Output:
# Tweet!
# Quack!
# Polly wants a cracker!
```

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| React | UI framework |
| useState Hook | Managing active tab and copy state |
| CSS | Custom styling and theming |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone <your-repo-url>

# Navigate into the project
cd your-project-name

# Install dependencies
npm install

# Start the development server
npm run dev
```

---

## 👩‍💻 Author

**Jess-Leigh Daniels**
