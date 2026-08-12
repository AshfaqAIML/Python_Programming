
### 📁 Module 10 – `README.md`

```markdown
# Module 10: File Handling & Exception Handling

**Duration:** 2h 44m · **Lectures:** 14

---

## 📌 Overview

This module teaches you to persist data beyond the life of your program using file I/O, and to write robust programs that gracefully handle errors using exceptions. You will work with plain text, JSON, and even binary serialisation with the `pickle` module.

---

## 🎯 Learning Objectives

- Create, read, write, and append to files
- Use the `with` statement for safe file operations
- Check if a file exists before opening it
- Recognise and fix common file‑handling issues
- Handle exceptions with `try-except-else-finally`
- Raise custom exceptions
- Work with structured data using `json`
- Serialise/deserialise objects with `pickle`
- Combine pickle with exception handling for data persistence

---

## 📖 Lecture Breakdown

### 1–8. File Handling: Introduction, Creating, `w`, `r`, `a`, `with`, Existence Check, Common Issues
- Opening modes: `'r'` (read), `'w'` (write, overwrites), `'a'` (append)
- `with open(...) as f:` – auto‑closes the file
- `os.path.exists()` to check before opening

```python
# Writing
with open('data.txt', 'w') as f:
    f.write("Hello, World!\n")

# Reading
with open('data.txt', 'r') as f:
    content = f.read()
    print(content)

# Appending
with open('data.txt', 'a') as f:
    f.write("Appended line.\n")

import os
if os.path.exists('data.txt'):
    print("File found")
```

### 9–11. Exception Handling: `try-except`, `else`, `finally`, Raising Exceptions
- Catch specific exceptions (e.g., `FileNotFoundError`, `ZeroDivisionError`)
- `else` – runs if no exception occurs
- `finally` – always runs (cleanup actions)
- `raise` – manually trigger an exception

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("That's not a valid integer.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
else:
    print(f"Result: {result}")
finally:
    print("Execution complete.")

if num < 0:
    raise ValueError("Number cannot be negative.")
```

### 12–14. `json` Module, `pickle` Module, Pickle + Exception Handling
- **JSON:** `json.dump()` / `json.load()` for structured data (lists, dicts)
- **Pickle:** `pickle.dump()` / `pickle.load()` for any Python object (including custom classes)
- Combine with `try-except` to handle corruption or missing files gracefully

```python
import json
data = {"name": "Alice", "age": 30}
with open("data.json", "w") as f:
    json.dump(data, f)

import pickle
class Person:
    def __init__(self, name):
        self.name = name
p = Person("Bob")
with open("person.pkl", "wb") as f:
    pickle.dump(p, f)
with open("person.pkl", "rb") as f:
    loaded = pickle.load(f)
    print(loaded.name)
```

---

## 🧪 Exercises

1. Write a program that reads a CSV‑style text file and prints the sum of all numbers in the second column.
2. Create a JSON file with a list of student records (name, grade). Write a script that loads it and prints the student with the highest grade.
3. Use `pickle` to save a dictionary of user preferences, and load it on startup – handle the case where the file does not exist.

---

## 📂 Prerequisites

- Modules 5–9 (data structures, functions, loops)

---

## 🔗 How to Use This Module

1. Create sample text files and practice all file modes.
2. Always use the `with` statement – it's safer and cleaner.
3. Use specific exception types rather than a bare `except:` to avoid masking unexpected errors.
4. Experiment with JSON for configuration files and Pickle for saving game states or ML models.

---

*Next: Module 11 – Regular Expressions.*
```
---

