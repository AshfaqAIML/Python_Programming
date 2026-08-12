### 📁 Module 8 – `README.md`


# Module 8: Loops

**Duration:** 2h 57m · **Lectures:** 15

---

## 📌 Overview

Loops automate repetitive tasks. This module covers Python’s two primary loop constructs – `for` and `while` – along with powerful control tools like `break`, `continue`, and `range()`. You will also apply these concepts through hands‑on exercises, including a number guessing game and star pattern printing.

---

## 🎯 Learning Objectives

- Iterate over sequences with `for` loops
- Use `range()` to generate numeric sequences
- Calculate totals, highs, and lows using loops
- Control loop flow with `continue` and `break`
- Write `while` loops and avoid infinite loops
- Generate random numbers with the `random` module
- Create nested loops and print star patterns
- Complete exercises: Roll a dice, List & Loops, Loops & Dictionaries, Number Guessing Game

---

## 📖 Lecture Breakdown

### 1–3. `for` loop, Strings & Dicts, `range()`
- Iterating over lists, strings, dictionaries, and tuples
- `range(stop)`, `range(start, stop)`, `range(start, stop, step)`

```python
for i in range(5):
    print(i)          # 0 1 2 3 4

for key, val in {'a':1, 'b':2}.items():
    print(key, val)
```

### 4. Total, Highest, Lowest Using Loops
- Accumulate sums, track min/max

```python
numbers = [12, 7, 19, 3, 8]
total = 0
highest = numbers[0]
lowest = numbers[0]
for n in numbers:
    total += n
    if n > highest: highest = n
    if n < lowest: lowest = n
print(f"Sum: {total}, Max: {highest}, Min: {lowest}")
```

### 5. `continue` and `break`
- `break` – exit loop immediately
- `continue` – skip the rest of the current iteration

```python
for i in range(10):
    if i == 3:
        continue      # skip 3
    if i == 7:
        break         # stop at 7
    print(i)          # 0 1 2 4 5 6
```

### 6–8. `while` loop, Infinite While, `random` module
- Syntax: `while condition:`
- Prevent infinite loops with proper condition updates
- `random.randint()`, `random.choice()`

```python
import random
target = random.randint(1, 10)
guess = 0
while guess != target:
    guess = int(input("Guess: "))
```

### 9–10. Nested Loops & Star Patterns
- Loops inside loops for 2D iterations
- Printing triangles, squares, pyramids

```python
for i in range(1, 6):
    for j in range(i):
        print("*", end="")
    print()
# Outputs a right-angled triangle
```

### 11–15. Exercises & Game
- **Roll a dice** – simulate die rolls with `random`
- **List & Loops** – filter, map, and reduce with loops
- **Loops & Dictionaries** – invert a dictionary
- **Number Guessing Game** – complete problem and solution

---

## 🧪 Exercises

1. Print a multiplication table (1–10) using nested loops.
2. Write a `while` loop that keeps asking for a password until the correct one is entered.
3. Generate a list of 20 random numbers and find all numbers greater than the average.
4. Build the number guessing game with a limited number of attempts.

---

## 📂 Prerequisites

- Modules 5, 6, 7 (Lists, Dicts, Control Statements)

---

## 🔗 How to Use This Module

1. Code every example – loops are best learned by doing.
2. Experiment with different `range()` arguments.
3. Be cautious with `while` loops – always ensure the condition will eventually become `False`.
4. Complete the exercises before moving on; they are the most practical part of this module.

---

*Next: Module 9 – Functions & Modules.*
```

