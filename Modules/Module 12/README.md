
---

### 📁 Module 12 – `README.md`


# Module 12: Object Oriented Programming (OOP)

**Duration:** 4h 55m · **Lectures:** 24

---

## 📌 Overview

Object Oriented Programming is a paradigm that organises code around objects rather than functions. This extensive module covers classes, inheritance, polymorphism, encapsulation, and abstraction – the pillars of OOP. You will also build a Phone Book mini‑project and create custom exception classes.

---

## 🎯 Learning Objectives

- Understand classes and objects
- Create classes with attributes and instance methods
- Use `__init__` to initialise instance variables
- Distinguish between instance and class variables
- Use `@classmethod` and `@staticmethod`
- Build a mini Phone Book application (Parts 1 & 2)
- Implement single, multiple, and multilevel inheritance
- Understand polymorphism: operator overloading, method overloading, method overriding
- Apply encapsulation and abstraction
- Create abstract classes using the `abc` module
- Write custom exception classes for your domain

---

## 📖 Lecture Breakdown

### 1–10. Introduction to OOP, Classes & Objects, Attributes, Methods, Initializer, Class/Static Methods
- Defining a class, creating instances, accessing attributes
- `self` parameter – reference to the current instance
- `__init__` – constructor
- Class variables (shared) vs instance variables (unique)
- `@classmethod` – alternate constructors; `@staticmethod` – utility functions

```python
class Student:
    school = "Python University"   # class variable

    def __init__(self, name, grade):
        self.name = name           # instance variable
        self.grade = grade

    def display(self):
        print(f"{self.name} – {self.grade}")

    @classmethod
    def change_school(cls, new_name):
        cls.school = new_name

    @staticmethod
    def is_passing(grade):
        return grade >= 40
```

### 11–12. Mini Project – Phone Book Parts 1 & 2
- Build a contact management system using OOP
- Part 1: Basic CRUD (Create, Read, Update, Delete) with lists
- Part 2: Persistence with file I/O and exception handling

### 13–17. Inheritance: Single, Single + Init, Arguments, Multiple, Multilevel
- Derived class inherits from base class
- `super().__init__()` to invoke parent initialiser
- Method Resolution Order (MRO) in multiple inheritance

```python
class Person:
    def __init__(self, name):
        self.name = name

class Employee(Person):
    def __init__(self, name, emp_id):
        super().__init__(name)
        self.emp_id = emp_id

class Manager(Employee):
    def __init__(self, name, emp_id, team_size):
        super().__init__(name, emp_id)
        self.team_size = team_size
```

### 18–21. Polymorphism: Operator Overloading, Method Overloading, Method Overriding
- **Operator overloading:** using magic methods like `__add__`, `__eq__`
- **Method overloading:** not natively supported – use default arguments or `*args`
- **Method overriding:** child class redefines a parent method

```python
class Vector:
    def __init__(self, x, y):
        self.x, self.y = x, y
    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

class Animal:
    def speak(self):
        pass
class Dog(Animal):
    def speak(self):
        return "Woof!"
```

### 22–23. Encapsulation, Abstraction, Abstract Class
- Encapsulation: use `_` (protected) and `__` (private) naming conventions
- Abstraction: hide implementation details
- Abstract classes using `ABC` and `@abstractmethod` – force subclasses to implement methods

```python
from abc import ABC, abstractmethod
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    def area(self):
        return 3.14 * self.radius ** 2
```

### 24. Custom Exception Classes
- Inherit from `Exception` and add custom fields or logic

```python
class NegativeAmountError(Exception):
    def __init__(self, amount):
        super().__init__(f"Amount cannot be negative: {amount}")
        self.amount = amount

def withdraw(amount):
    if amount < 0:
        raise NegativeAmountError(amount)
```

---

## 🧪 Exercises

1. Create a `BankAccount` class with deposit, withdraw, and balance methods, with proper checks.
2. Use multiple inheritance to create a `SmartPhone` class that inherits from `Phone` and `Device`.
3. Write a custom exception `InsufficientFundsError` and use it in a banking context.

---

## 📂 Prerequisites

- All previous modules – especially functions and modules

---

## 🔗 How to Use This Module

1. This is the longest and most important module – take your time.
2. Code every example from scratch – do not copy‑paste.
3. The Phone Book mini‑project is your chance to apply everything; complete it fully.
4. Understand the theory behind each OOP pillar – they are often asked in interviews.

---

*Next: Module 13 – Tkinter (GUI).*
```
