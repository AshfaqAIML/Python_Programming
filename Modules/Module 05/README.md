



### 📁 Module 5 – `README.md`


# Module 5: Lists in Python

**Duration:** 1h 19m · **Lectures:** 6

---

## 📌 Overview

Lists are the most versatile and frequently used sequence type in Python. They are mutable, ordered, and can hold elements of any data type. This module covers everything from basic creation to advanced nested structures, equipping you to handle collections of data efficiently.

---

## 🎯 Learning Objectives

- Create, index, and slice lists
- Modify lists using `append`, `insert`, `extend`, `remove`, and `pop`
- Concatenate and repeat lists
- Sort, reverse, and count elements
- Test membership with `in` and `not in`
- Perform numerical operations (`sum`, `min`, `max`, `len`) on list elements
- Build and traverse nested lists

---

## 📖 Lecture Breakdown

### 1. Lists Introduction
- What is a list?
- Creating lists with `[]` and `list()`
- Accessing elements by index (positive and negative)

### 2. List Operations – Slicing, Concat, Repeat, Append, Insert
- Slicing: `list[start:stop:step]`
- Concatenation: `list1 + list2`
- Repetition: `list * n`
- Adding items: `append()` and `insert()`

```python
fruits = ['apple', 'banana']
fruits.append('orange')          # ['apple', 'banana', 'orange']
fruits.insert(1, 'grape')        # ['apple', 'grape', 'banana', 'orange']
```

### 3. List Operations – Extend, Remove, Pop
- `extend()` – merge another iterable
- `remove()` – delete first matching value
- `pop()` – remove and return an item by index (default: last)

```python
nums = [1, 2, 3]
nums.extend([4, 5])      # [1, 2, 3, 4, 5]
nums.remove(3)           # [1, 2, 4, 5]
last = nums.pop()        # last = 5, nums = [1, 2, 4]
```

### 4. List Operation – Reverse, Sort, Count, Membership
- `reverse()` – reverse in place
- `sort()` – ascending/descending
- `count()` – occurrences of a value
- Membership tests: `if x in list`

```python
letters = ['b', 'a', 'c']
letters.sort()           # ['a', 'b', 'c']
letters.reverse()        # ['c', 'b', 'a']
print(letters.count('b')) # 1
print('a' in letters)    # True
```

### 5. Numerical Operations on List Elements
- Built‑in helpers: `sum()`, `max()`, `min()`, `len()`
- Works on numeric lists

```python
scores = [88, 72, 93, 65]
print(sum(scores))    # 318
print(max(scores))    # 93
print(min(scores))    # 65
print(len(scores))    # 4
```

### 6. Nested Lists
- Lists inside lists – matrix representation
- Accessing elements with double indexing
- Iterating over nested structures

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(matrix[1][2])   # 6
for row in matrix:
    for val in row:
        print(val, end=' ')
# Output: 1 2 3 4 5 6 7 8 9
```

---

## 🧪 Exercises

1. Create a list of 10 random integers and find the second largest.
2. Given a nested list representing a tic‑tac‑toe board, check if any row is all `'X'`.
3. Write a function that flattens a nested list (e.g., `[[1,2],[3,4]]` → `[1,2,3,4]`).

---

## 📂 Prerequisites

- Basic Python syntax (variables, `print()`)
- Familiarity with `for` loops (covered in Module 8, but basic knowledge is helpful)

---

## 🔗 How to Use This Module

1. Read through each lecture sequentially.
2. Type every code snippet into your own Python environment.
3. Modify the examples – experiment with different inputs.
4. Complete the exercises at the end.

---

*Proceed to Module 6: Tuples, Sets & Dictionaries after mastering lists.*
```

---

