
# 📘 JSON Guide in Python

---

## ✅ What is JSON?

**JSON** (JavaScript Object Notation) is:

- A lightweight **data interchange** format
- **Human-readable**
- Easy for machines to **parse** and **generate**
- Commonly used in **web APIs**, **configuration files**, and **data storage**

---

## 🛠️ JSON vs Python Data Types

| JSON Type     | Python Equivalent |
|---------------|-------------------|
| Object        | `dict`            |
| Array         | `list`            |
| String        | `str`             |
| Number        | `int`, `float`    |
| Boolean       | `True`, `False`   |
| Null          | `None`            |

---

## 📦 Working with JSON in Python

Use Python’s built-in `json` module.

```python
import json
```

---

## 🔧 Common JSON Methods

| Method               | Description                                 | Use Case                            |
|----------------------|---------------------------------------------|-------------------------------------|
| `json.load(file)`    | Reads JSON from a file                      | Reading a config or dataset         |
| `json.loads(str)`    | Converts JSON string to Python object       | Parsing API response                |
| `json.dump(obj, f)`  | Writes Python object to file in JSON format | Saving preprocessed data            |
| `json.dumps(obj)`    | Converts Python object to JSON string       | Sending data to a web service       |

---

## 📥 Reading JSON

### 1. From JSON String

```python
import json

json_data = '{"name": "Sita", "age": 25, "city": "Kathmandu"}'
python_obj = json.loads(json_data)

print(python_obj["city"])  # Output: Kathmandu
```

### 2. From JSON File

**data.json**
```json
{
  "name": "Sita",
  "age": 25,
  "city": "Kathmandu"
}
```

```python
with open("data.json") as file:
    data = json.load(file)

print(data["name"])  # Output: Sita
```

---

## 📤 Writing JSON

### 1. Python to JSON String

```python
person = {"name": "Ramesh", "age": 30, "city": "Pokhara"}
json_string = json.dumps(person, indent=4)

print(json_string)
```

### 2. Save JSON to File

```python
with open("output.json", "w") as f:
    json.dump(person, f, indent=4)
```

---

## 💡 Real-World Use Cases in Data Science

| Use Case              | Description                                  |
|------------------------|----------------------------------------------|
| APIs                   | Most APIs return JSON (e.g., weather, Twitter) |
| Config Files           | `.json` used to store pipeline or ML settings |
| Storing Processed Data | Save cleaned/structured datasets             |
| MongoDB                | NoSQL DB stores data in JSON-like format     |

---

## ⚠️ Tips & Warnings

- JSON keys **must be strings**
- JSON doesn't support **comments**
- JSON has no `tuple`, converts it to `list`
- Python `None` becomes JSON `null`

---

## 🧪 Mini Practice Tasks

### 🟢 Beginner

#### Weather Data Parsing
```json
{
  "city": "Kathmandu",
  "temperature": {
    "current": 28,
    "min": 20,
    "max": 30
  },
  "humidity": 70,
  "condition": "Cloudy"
}
```

**Task**: Extract city, current temperature, and humidity.

---

### 🟡 Intermediate

#### E-commerce Order

```json
{
  "order_id": 1123,
  "customer": {
    "name": "Sita Karki",
    "location": "Lalitpur"
  },
  "items": [
    {"product": "Laptop", "price": 85000},
    {"product": "Mouse", "price": 1500}
  ],
  "status": "Delivered"
}
```

**Task**:
- Calculate total order amount
- Extract product names

---

### 🔴 Advanced

#### COVID-19 Stats

```json
[
  {
    "country": "Nepal",
    "cases": {"confirmed": 800, "recovered": 600, "deaths": 10}
  },
  {
    "country": "India",
    "cases": {"confirmed": 50000, "recovered": 47000, "deaths": 500}
  },
  {
    "country": "USA",
    "cases": {"confirmed": 100000, "recovered": 95000, "deaths": 800}
  }
]
```

**Task**:
- Calculate total confirmed cases
- Compute and display death rate per country

---

## ✅ Summary

JSON is essential for any data-driven application. In Python, it helps you:
- Read/write data from APIs
- Store config or processed data
- Parse nested structures

> Tip: Always validate JSON using online tools like https://jsonlint.com or using `json.loads()` in Python.

---
