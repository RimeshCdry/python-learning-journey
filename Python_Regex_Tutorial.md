# 📘 Python Regex Tutorial for Beginners

### Instructor: *[Your Name]*

> Learn how to search, extract, validate, and manipulate strings using powerful patterns known as **regular expressions** (regex).

---

## 📌 Table of Contents
1. [What is Regex?](#1-what-is-regex)
2. [Why Use Regex in Projects?](#2-why-use-regex-in-projects)
3. [How to Use Regex in Python](#3-how-to-use-regex-in-python)
4. [Common `re` Module Methods (Table)](#4-common-re-module-methods-table)
5. [Regex Syntax and Meta-characters](#5-regex-syntax-and-meta-characters)
6. [How to Create Your Own Regex Pattern](#6-how-to-create-your-own-regex-pattern)
7. [Practical Examples](#7-practical-examples)
8. [Mini Practice Exercises](#8-mini-practice-exercises)
9. [Tips for Using Regex in Projects](#9-tips-for-using-regex-in-projects)

---

## 1. ✅ What is Regex?

Regex (short for Regular Expression) is a sequence of characters that forms a search pattern.
It's mainly used to:
- Find or match strings
- Validate input formats (like email or phone numbers)
- Extract specific parts of text

---

## 2. 💡 Why Use Regex in Projects?

| Scenario           | Use Case Example                          |
|--------------------|-------------------------------------------|
| Validating input   | Email, password, username format check    |
| Parsing text       | Extract date, time, tags from logs        |
| Search keywords    | Filter tweets that contain "python"       |
| Data cleaning      | Remove extra spaces, HTML tags, symbols   |
| Web scraping       | Extract phone numbers from webpages       |

---

## 3. 🛠️ How to Use Regex in Python?

Python provides the `re` module.

```python
import re

text = "My phone number is 9876543210"
pattern = r"\d{10}"
match = re.search(pattern, text)
if match:
    print("Phone number found:", match.group())
```

---

## 4. 📋 Common `re` Module Methods (Table)

| Method         | Description                                   | Use Case                              |
|----------------|-----------------------------------------------|----------------------------------------|
| `search()`     | Returns first match object or `None`          | Check if a pattern exists              |
| `match()`      | Matches only at start of the string           | When pattern must appear at beginning |
| `findall()`    | Returns all matches as a list                 | Extract all pattern matches           |
| `finditer()`   | Returns an iterator of match objects          | When position info is needed          |
| `sub()`        | Replaces matches with a new string            | Text replacement/cleaning             |
| `split()`      | Splits a string based on the pattern          | When delimiters are regex             |
| `compile()`    | Compiles a regex pattern for reuse            | Better performance & readability      |

---

## 5. 🔣 Regex Syntax and Meta-characters

| Symbol     | Meaning                               | Example Match        |
|------------|----------------------------------------|-----------------------|
| `.`        | Any character except newline           | `c.t` -> `cat`, `cut` |
| `^`        | Start of string                        | `^Hello`              |
| `$`        | End of string                          | `end$`                |
| `*`        | 0 or more repetitions                  | `lo*` -> `l`, `loo`   |
| `+`        | 1 or more repetitions                  | `go+` -> `gooo`       |
| `?`        | 0 or 1 repetition (optional)           | `colou?r`             |
| `{n}`      | Exactly n times                        | `\d{4}` -> 1234      |
| `{n,m}`    | Between n and m times                  | `\d{2,4}`            |
| `[]`       | One character from set                 | `[aeiou]`             |
| `[^]`      | Excludes characters in set             | `[^0-9]`              |
| `\d`      | Digit [0-9]                            | `\d+` -> `123`       |
| `\w`      | Word character                         | `\w+` -> `abc_123`   |
| `\s`      | Whitespace                             | `\s+`                |
| `|`        | OR operator                            | `cat|dog`             |
| `()`       | Grouping                               | `(abc)+`              |
| `\b`       | Word Boundary(start or end of a    word) |                                           `\b`                                           

---

## 6. 🧠 How to Create Your Own Regex Pattern

1. Define what pattern you want (e.g., date: `25-06-2025`)
2. Break into parts:
   - `\d{2}` for day
   - `-` separator
   - `\d{2}` for month
   - `-` separator
   - `\d{4}` for year
3. Combine: `r"\d{2}-\d{2}-\d{4}"`

```python
date = "Today is 25-06-2025"
pattern = r"\d{2}-\d{2}-\d{4}"
match = re.search(pattern, date)
print(match.group())
```

---

## 7. 🧪 Practical Examples

### ✅ Validate Email
```python
pattern = r"^[\w.-]+@[\w.-]+\.\w+$"
```

### ✅ Extract Hashtags from Tweet
```python
re.findall(r"#\w+", "#python is great! #coding")
```

### ✅ Replace Multiple Spaces
```python
re.sub(r"\s+", " ", "This   is   spaced")
```

---

## 8. 🎯 Mini Practice Exercises

Try writing regex for:

1. Indian Phone Number → `\d{10}`
2. Postal Code → `\d{6}`
3. Date (dd-mm-yyyy) → `\d{2}-\d{2}-\d{4}`
4. Extract numbers → `\d+`
5. Validate password → min 8 chars, 1 letter, 1 number

---

## 9. 🧰 Tips for Using Regex in Projects

- Use **raw strings** (r"...") to avoid escape issues.
- Use `re.compile()` when reusing patterns.
- Test patterns on [regex101.com](https://regex101.com)
- Add comments for complex patterns.
- Don't use regex for deeply nested or logical validation.

---

> 🏁 **Conclusion**: Regex is an essential skill for any Python developer working with text data, from cleaning and validation to extraction and automation. Practice often to master it!
