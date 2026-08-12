
---

### 📁 Module 13 – `README.md`


# Module 13: Tkinter – GUI Development

**Duration:** 2h 51m · **Lectures:** 12

---

## 📌 Overview

Tkinter is Python’s standard GUI toolkit. This module introduces you to building desktop applications with widgets, layouts, and event handling. You will create windows, add buttons, labels, entry fields, and more, culminating in a complete understanding of GUI fundamentals.

---

## 🎯 Learning Objectives

- Set up a Tkinter window
- Use core widgets: `Label`, `Button`, `Entry`, `Frame`, `Text`, `Separator`
- Arrange widgets using `pack()` geometry manager
- Use `ttk` for themed widgets
- Handle events (button clicks, window quitting)
- Work with `Checkbutton`, `Radiobutton`, `Listbox`, and `Spinbox`
- Organise layouts with `Frame` and background colours

---

## 📖 Lecture Breakdown

### 1. Introduction to GUI and Tkinter
- What is GUI? Why Tkinter?
- Installing Tkinter (usually built‑in)

### 2. Label, Title, Minsize, Pack
- `Tk()` – root window
- `title()`, `minsize()`
- `Label` widget and `pack()` layout

```python
import tkinter as tk
root = tk.Tk()
root.title("My App")
root.minsize(300, 200)
label = tk.Label(root, text="Hello, Tkinter!")
label.pack()
root.mainloop()
```

### 3. Button and Change Label Text
- `Button` widget with `command` option
- Updating label text via event handler

```python
def change_text():
    label.config(text="Button clicked!")

btn = tk.Button(root, text="Click me", command=change_text)
btn.pack()
```

### 4. The Entry Component
- Single‑line text input
- `get()` and `insert()` methods

```python
entry = tk.Entry(root)
entry.pack()
def show():
    print(entry.get())
```

### 5. What is ttk
- Themed widgets from `tkinter.ttk` – more modern appearance

```python
from tkinter import ttk
btn = ttk.Button(root, text="Themed", command=some_func)
```

### 6. Quitting the Window
- `root.destroy()` or `root.quit()`
- Binding the close button to a custom handler

### 7. Frames and Background Colors
- `Frame` – container for organising other widgets
- `bg` (background) option

```python
frame = tk.Frame(root, bg="lightblue", width=200, height=100)
frame.pack()
```

### 8. Text, Separator and Padding
- `Text` – multi‑line text area
- `ttk.Separator` – visual divider
- `padx`, `pady` – padding for widgets

### 9. Checkbutton Widget
- Toggle buttons with `IntVar` or `BooleanVar`

```python
var = tk.IntVar()
cb = tk.Checkbutton(root, text="Accept terms", variable=var)
cb.pack()
```

### 10. Radiobutton Widget
- Group of mutually exclusive options

```python
choice = tk.StringVar()
r1 = tk.Radiobutton(root, text="Male", variable=choice, value="M")
r2 = tk.Radiobutton(root, text="Female", variable=choice, value="F")
```

### 11. Checkbox and Listbox
- `Listbox` – scrollable list of items

```python
lb = tk.Listbox(root)
lb.insert(1, "Apple")
lb.insert(2, "Banana")
lb.pack()
```

### 12. Spinbox Widget
- Numeric up‑down control

```python
spin = tk.Spinbox(root, from_=0, to=10)
spin.pack()
```

---

## 🧪 Exercises

1. Build a simple login form with labels, entries, and a "Login" button that prints the entered credentials.
2. Create a colour selector using Radiobuttons that changes the window background.
3. Use a Listbox and a Button to add/remove items.

---

## 📂 Prerequisites

- Modules 5–9 (functions are essential for event handlers)

---

## 🔗 How to Use This Module

1. Run each example – Tkinter is very visual, so seeing the output helps.
2. Experiment with different geometry managers: `pack()`, `grid()`, `place()`.
3. Combine multiple widgets in a single window to build mini‑forms.
4. Pay attention to event binding – it’s what makes GUI interactive.

---

*Next: Module 14 – Calculator Using Tkinter (final project).*
```
