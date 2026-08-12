
---

### 📁 Module 14 – `README.md`

```markdown
# Module 14: Calculator Using Tkinter

**Duration:** 28m 49s · **Lectures:** 3

---

## 📌 Overview

This is the final project of the course – you will build a fully functional calculator with a graphical user interface using Tkinter. This project brings together everything you have learned: Python logic, event handling, layout management, and exception handling.

---

## 🎯 Learning Objectives

- Design a GUI layout for a calculator
- Create a grid of number and operation buttons
- Handle button clicks to build expressions
- Evaluate expressions safely (using `eval()` or custom parser)
- Display results and handle errors (e.g., division by zero)
- Produce a polished, user‑friendly application

---

## 📖 Lecture Breakdown

### 1. Calculator (Part 1) – UI Layout
- Design the main window with a display (`Entry` or `Label`) and a grid of buttons
- Use `grid()` geometry manager to position buttons
- Define button labels: digits 0–9, operators (`+`, `-`, `*`, `/`), clear (`C`), equals (`=`)

```python
import tkinter as tk
root = tk.Tk()
root.title("Calculator")

display = tk.Entry(root, width=16, font=("Arial", 20), borderwidth=2, relief="solid")
display.grid(row=0, column=0, columnspan=4)

buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    'C', '0', '=', '+'
]

row, col = 1, 0
for btn in buttons:
    cmd = lambda x=btn: click(x)   # will define click() later
    tk.Button(root, text=btn, width=5, height=2, command=cmd).grid(row=row, column=col)
    col += 1
    if col > 3:
        col = 0
        row += 1
```

### 2. Calculator (Part 2) – Event Handling & Logic
- Implement the `click(value)` function
- Append digits and operators to the display
- Handle `C` (clear) and `=` (evaluate)

```python
expression = ""
def click(val):
    global expression
    if val == "C":
        expression = ""
        display.delete(0, tk.END)
    elif val == "=":
        try:
            result = eval(expression)   # safe for this small project
            display.delete(0, tk.END)
            display.insert(0, str(result))
            expression = str(result)
        except Exception as e:
            display.delete(0, tk.END)
            display.insert(0, "Error")
            expression = ""
    else:
        expression += val
        display.insert(tk.END, val)
```

### 3. Calculator (Part 3) – Polishing & Edge Cases
- Handle decimal point (`.`)
- Prevent multiple consecutive operators
- Handle division by zero gracefully
- Add keyboard support (optional)
- Improve styling with `ttk` or custom fonts/colours

```python
# Example: restrict multiple dots
if val == '.' and '.' in expression.split('+')[-1].split('-')[-1]:
    return   # do not add another dot in the same number
```

---

## 🧪 Exercises / Extensions

1. Add a square root (`√`) button.
2. Add a percentage (`%`) button that divides the current number by 100.
3. Allow keyboard input – bind number keys and `Enter` to the calculator.
4. Change the colour scheme to make it more visually appealing.

---

## 📂 Prerequisites

- Module 13 (Tkinter)
- All previous modules (especially functions and exception handling)

---

## 🔗 How to Use This Module

1. Follow the three parts sequentially – do not skip ahead.
2. Test each feature as you add it (e.g., test the `C` button immediately after coding it).
3. Use `eval()` cautiously – it is acceptable for this educational project, but in production you would use a safer parser.
4. Once your calculator works, try the extensions to further challenge yourself.

---

**🎉 Congratulations!** You have now completed the core Python curriculum. You are ready to build your own real‑world applications.

---

*Return to the main course overview or proceed to your next learning adventure.*
```

---

Each README is self‑contained, packed with code examples, and ready to be dropped into its respective module folder. Let me know if you need any adjustments!