### 📁 Module 6 – `README.md`


# Module 6: Tuples, Sets & Dictionaries

**Duration:** 2h 59m · **Lectures:** 12

---

## 📌 Overview

This module expands your data structure toolkit with three essential collection types: **tuples** (immutable sequences), **sets** (unique, unordered collections), and **dictionaries** (key‑value mappings). Understanding when and how to use each is critical for writing efficient Python code.

---

## 🎯 Learning Objectives

- Create and manipulate tuples
- Understand the immutability of tuples vs. mutability of lists
- Build sets and perform set operations (union, intersection, difference)
- Use `frozenset` for immutable sets
- Create and update dictionaries
- Iterate over keys, values, and items
- Distinguish between shallow and deep copies
- Apply `for` loops to all collection types

---

## 📖 Lecture Breakdown

### 1–3. Introducing Tuples & Basic Operations
- Syntax: `t = (1, 2, 3)`
- Indexing, slicing, concatenation, repetition
- **Key concept:** Tuples are immutable – you cannot change, add, or remove elements

```python
t = (10, 20, 30)
print(t[1])          # 20
# t[1] = 99          # TypeError: 'tuple' object does not support item assignment
```

### 4–7. Introducing Sets & Operations
- Creating sets: `s = {1, 2, 3}` or `set([1,2,3])`
- No duplicates allowed
- Operations: `union()`, `intersection()`, `difference()`, `symmetric_difference()`
- `frozenset` – immutable version

```python
A = {1, 2, 3}
B = {3, 4, 5}
print(A | B)          # union – {1,2,3,4,5}
print(A & B)          # intersection – {3}
print(A - B)          # difference – {1,2}
fs = frozenset([1,2,3])   # can be used as dictionary keys
```

### 8–12. Introducing Dictionaries, Updating, Deleting, Keys & Values, Copy
- Dictionary literal: `d = {'name': 'Alice', 'age': 25}`
- Adding/updating: `d['city'] = 'NYC'`
- Deleting: `del d['age']` or `pop()`
- Looping: `.keys()`, `.values()`, `.items()`
- **Shallow vs deep copy:** `copy.copy()` vs `copy.deepcopy()`
- The `for` loop works seamlessly with dicts

```python
d = {'a': 1, 'b': 2}
for key, value in d.items():
    print(f"{key}: {value}")

import copy
d2 = copy.deepcopy(d)   # completely independent copy
```

---

## 🧪 Exercises

1. Given two sets, find their symmetric difference without using the `^` operator.
2. Write a function that counts the frequency of each word in a sentence using a dictionary.
3. Create a tuple of 5 numbers and write a function that returns a new tuple with all elements doubled.

---

## 📂 Prerequisites

- Module 5 (Lists)
- Basic understanding of loops and conditionals

---

## 🔗 How to Use This Module

1. Watch the lectures in order.
2. Code along, paying special attention to the immutability of tuples and the uniqueness of sets.
3. Practice dictionary operations – they are heavily used in real‑world applications.
4. Complete the exercises to reinforce your understanding.

---

*Next: Module 7 – Control Statements.*
```

