
### 📁 Module 11 – `README.md`

```markdown
# Module 11: Regular Expressions (RegEx)

**Duration:** 2h 1m · **Lectures:** 9

---

## 📌 Overview

Regular expressions are a powerful language for pattern matching in text. This module introduces you to the syntax and functions of Python’s `re` module, enabling you to search, extract, and substitute patterns with speed and precision.

---

## 🎯 Learning Objectives

- Understand RegEx syntax and metacharacters
- Use the dot (`.`) and character classes (`\d`, `\w`, `\s`)
- Handle special characters and anchors (`^`, `$`)
- Apply quantifiers (`*`, `+`, `?`, `{m,n}`)
- Use more metacharacters: groups, alternation (`|`)
- Find all matches with `findall()` and `finditer()`
- Substitute patterns with `sub()`
- Compile patterns with `compile()` for efficiency
- Apply all concepts to find valid email addresses

---

## 📖 Lecture Breakdown

### 1. Introduction to RegEx
- Why RegEx? Use cases (form validation, log parsing, data cleaning)
- Importing `re`

### 2. Dot Metacharacter and Character Classes
- `.` – any character except newline
- `\d` – digits `[0-9]`, `\D` – non‑digits
- `\w` – word characters `[a-zA-Z0-9_]`, `\W` – non‑word
- `\s` – whitespace, `\S` – non‑whitespace

```python
import re
text = "My phone is 123-456-7890."
matches = re.findall(r'\d{3}-\d{3}-\d{4}', text)
print(matches)   # ['123-456-7890']
```

### 3. Special Characters in RegEx
- Anchors: `^` (start of string), `$` (end of string)
- Escaping: `\.` to match a literal dot, `\\` for backslash

### 4. Quantifiers
- `*` – 0 or more, `+` – 1 or more, `?` – 0 or 1
- `{n}` – exactly n, `{n,}` – n or more, `{n,m}` – between n and m

```python
pattern = r'colou?r'     # matches 'color' and 'colour'
```

### 5. More Metacharacters
- Groups: `(abc)` – captures the group
- Alternation: `|` – OR, e.g., `cat|dog`
- Character sets: `[aeiou]` – any vowel

### 6. Finding All Matches – `findall`, `finditer`
- `findall()` – returns list of strings (or tuples if groups)
- `finditer()` – returns iterator of match objects (with positions)

```python
for match in re.finditer(r'\d+', 'I have 10 apples and 20 oranges'):
    print(match.group(), match.span())
# 10 (7, 9), 20 (22, 24)
```

### 7. Substituting the Pattern – `sub()`
- Replace matches with a replacement string

```python
cleaned = re.sub(r'\s+', ' ', 'Too   many   spaces')  # 'Too many spaces'
```

### 8. The `compile()` Function
- Precompile for performance when using the same pattern repeatedly

```python
pattern = re.compile(r'\d{3}-\d{3}-\d{4}')
result = pattern.search(text)
```

### 9. Exercise – Finding Valid Emails
- Combine all learned concepts to build a robust email‑matching pattern

```python
email_pattern = r'^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$'
emails = ['test@example.com', 'invalid-email', 'user@co.uk']
valid = [e for e in emails if re.match(email_pattern, e)]
print(valid)   # ['test@example.com', 'user@co.uk']
```

---

## 🧪 Exercises

1. Write a pattern to extract all hashtags (`#word`) from a tweet.
2. Replace all occurrences of `"foo"` with `"bar"` but only if they are whole words (use `\b`).
3. Write a function that validates an IPv4 address using RegEx.

---

## 📂 Prerequisites

- Basic string handling, loops, and conditionals (Modules 5, 7, 8)

---

## 🔗 How to Use This Module

1. Practice with online RegEx testers (e.g., regex101.com) to visualise your patterns.
2. Start with simple patterns and gradually add complexity.
3. Remember that RegEx can become cryptic – use comments or verbose mode (`re.VERBOSE`) for readability.
4. The email validation exercise is the culmination – make sure you understand every part of the pattern.

---

*Next: Module 12 – Object Oriented Programming.*
```
