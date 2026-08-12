
### 📁 Module 7 – `README.md`

# Module 7: Control Statements

**Duration:** 47m 40s · **Lectures:** 5

---

## 📌 Overview

Control statements are the decision‑making heart of any program. This module teaches you how to direct the flow of execution based on conditions, enabling your code to react intelligently to different inputs and states.

---

## 🎯 Learning Objectives

- Use the `if` block to execute code conditionally
- Branch with `if-else` for two‑way decisions
- Handle multiple conditions with `if-elif-else`
- Build complex logic using nested `if` statements
- Write concise conditional expressions with the ternary operator

---

## 📖 Lecture Breakdown

### 1. The `if` Block
- Syntax: `if condition:`
- Indentation matters in Python

```python
age = 18
if age >= 18:
    print("You are an adult.")
```

### 2. `if-else` Block
- Executes one block when the condition is `True`, another when `False`

```python
score = 45
if score >= 40:
    print("Pass")
else:
    print("Fail")
```

### 3. `if-elif-else` Block
- Chains multiple mutually exclusive conditions

```python
grade = 85
if grade >= 90:
    print("A")
elif grade >= 75:
    print("B")
elif grade >= 50:
    print("C")
else:
    print("F")
```

### 4. Nested `if` Statements
- Placing an `if` inside another `if` – useful for multi‑level logic

```python
x = 10
y = 20
if x > 5:
    if y > 15:
        print("Both conditions are true")
```

### 5. The Ternary Operator
- Shorthand for `if-else`: `value_if_true if condition else value_if_false`

```python
result = "Even" if num % 2 == 0 else "Odd"
```

---

## 🧪 Exercises

1. Write a program that checks if a year is a leap year.
2. Using nested `if`, classify a triangle as equilateral, isosceles, or scalene based on side lengths.
3. Convert the following `if-else` into a ternary operator:  
   `if temp > 30: print("Hot") else: print("Cold")`

---

## 📂 Prerequisites

- Basic Python syntax (variables, input/output)
- Comparison operators (`==`, `>`, `<`, `>=`, `<=`, `!=`)

---

## 🔗 How to Use This Module

1. Run each example and change the values to see different branches execute.
2. Pay close attention to indentation – it determines which block belongs to which condition.
3. Use the ternary operator for simple conditions to make your code more compact.

---

*Proceed to Module 8: Loops for repetitive execution.*
```


