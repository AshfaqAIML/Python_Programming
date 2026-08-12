
### 📁 Module 9 – `README.md`

# Module 9: Functions & Modules

**Duration:** 3h 34m · **Lectures:** 16

---

## 📌 Overview

Functions are the building blocks of reusable, maintainable code. This module covers defining functions, handling arguments, return values, recursion, scope, and the powerful lambda functions. You will also learn to organise code into modules and create your own packages. The module concludes with a mini‑project: a simple banking application.

---

## 🎯 Learning Objectives

- Define and call user‑defined functions
- Return single or multiple values
- Handle positional, keyword, default, and variable‑length arguments (`*args`, `**kwargs`)
- Write docstrings for documentation
- Implement recursive functions
- Understand local and global variable scope
- Pass functions as arguments
- Create and use lambda functions
- Use `filter()` and `map()` with lambdas
- Import and create modules
- Understand `__name__` and script vs. module execution
- Build a simple banking application

---

## 📖 Lecture Breakdown

### 1–3. Introduction, User‑defined Functions, Returning Values
- Defining with `def`, calling, and returning data

```python
def add(a, b):
    """Return the sum of a and b."""
    return a + b

result = add(5, 3)    # 8
```

### 4–6. Types of Arguments, Variable‑length Positional & Keyword
- Positional, keyword, default parameters
- `*args` – arbitrary positional arguments
- `**kwargs` – arbitrary keyword arguments

```python
def greet(name, msg="Hello"):
    print(f"{msg}, {name}")

def sum_all(*args):
    return sum(args)

def print_info(**kwargs):
    for key, val in kwargs.items():
        print(f"{key}: {val}")
```

### 7. Docstrings
- Multi‑line documentation string at the top of the function

```python
def square(n):
    """Calculate the square of a number.

    Args:
        n (int or float): The number to square.

    Returns:
        int or float: The squared value.
    """
    return n ** 2
```

### 8. Recursive Functions
- A function that calls itself – ideal for tree traversal, factorial, etc.

```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)
```

### 9. Local and Global Variables
- Variables inside vs outside functions

```python
x = 10          # global
def change():
    global x
    x = 20      # modifies global
```

### 10–12. Function as Argument, Lambda, filter/map
- Higher‑order functions, anonymous lambdas
- `filter()` – keep items where function returns `True`
- `map()` – apply function to every item

```python
nums = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, nums))
evens = list(filter(lambda x: x % 2 == 0, nums))
```

### 13–15. Modules in Python, User‑defined Modules, `__name__`
- Importing standard modules (`math`, `random`, etc.)
- Creating your own `.py` file and importing it
- `if __name__ == "__main__":` – code that runs only when executed directly

### 16. Simple Banking Application
- Combine all concepts: functions, modules, and control flow
- Features: deposit, withdraw, check balance, exit

---

## 🧪 Exercises

1. Write a function `is_palindrome` that checks if a string is a palindrome recursively.
2. Create a module `geometry.py` with functions `circle_area(radius)` and `rectangle_area(length, width)`. Import and use it.
3. Use `map()` and `filter()` to process a list of temperatures: convert Celsius to Fahrenheit and filter out those below freezing.

---

## 📂 Prerequisites

- All previous modules (especially data structures and loops)

---

## 🔗 How to Use This Module

1. Write each function type and test it with different inputs.
2. Practice recursive functions with simple problems (factorial, Fibonacci) before moving to complex ones.
3. Create a `utils.py` module and import it into another script to see modularity in action.
4. The banking mini‑project is a milestone – ensure you complete it fully.

---

*Proceed to Module 10: File Handling & Exception Handling.*
```

---
