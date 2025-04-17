# 📘 Week 1: Python Basics, Variables & Data Types

Welcome to your first week of Python programming!

In this module, we’ll explore:
- What is Python?
- What are variables?
- What are data types?
- How do these apply to economics (like GDP, inflation, income)?

---

## 🐍 1. What is Python?

Python is a programming language used to analyze data, automate boring tasks, and even do economic research.  
Think of it as **a calculator with superpowers**. 😄

Python is used by economists, statisticians, and researchers around the world to:
- Clean and analyze data
- Make graphs and charts
- Build models for forecasting

In this course, we’ll use Python to understand the economy of Pakistan in fun and simple ways.

---

## 📆 2. What is a Variable?

A **variable** is like a box where we store information.

> 🧠 Think of GDP as a number stored in a box named `GDP`.

```python
GDP = 350
```

Now `GDP` holds the value 350. This is just like writing GDP = 350 Billion USD in your economics assignment.

Just like:
```python
inflation = 12.5
income = 50000
```

Now you have 3 variables that store key economic values.

### 🔍 Rules for Naming Variables in Python:

- Variable names **cannot start with a number**.
  - ❌ `1income = 50000` → Invalid
  - ✅ `income1 = 50000` → Valid

- No spaces allowed. Use underscores `_` instead.
  - ❌ `total income = 100000`
  - ✅ `total_income = 100000`

- Only letters, numbers, and underscores are allowed.
- Variable names **are case-sensitive**.
  - `GDP`, `gdp`, and `Gdp` are all different.

- Don't use Python reserved keywords (like `if`, `for`, `while`, etc.).

Good examples:
```python
GDP = 350
inflation_rate = 12.5
monthly_income = 50000
```

Bad examples:
```python
1gdp = 350     # starts with a number ❌
total income = 60000  # contains a space ❌
for = 10       # reserved word ❌
```

---

## 🧬 3. Data Types in Python

Every variable has a **data type** — it tells Python what kind of value is stored.

| Data Type | What It Means       | Real Example                          |
|-----------|---------------------|----------------------------------------|
| `int`     | Whole number         | `GDP = 350`                            |
| `float`   | Decimal number       | `inflation = 12.5`                     |
| `str`     | Text (string)        | `country = "Pakistan"`                |
| `bool`    | True/False           | `is_expensive = True`                 |

---

## 👩‍🌾 Real-Life Example (Funny but True 😅)

Let’s say you're selling **naan** and **chai** in Lahore:

```python
price_naan = 30      # naan price in rupees
price_chai = 50      # chai price
total = price_naan + price_chai
```

If someone orders one naan and one chai, the total bill is `80`.

You just used Python to run a mini economic transaction! 💵

---

## 🎯 Summary

- Python is beginner-friendly and powerful.
- A **variable** stores a value.
- **Data types** tell us what kind of value is stored.
- We can use Python to represent real economic concepts like GDP, inflation, and income.
- There are **rules** for naming variables to avoid errors.

---

## 📝 Practice Tasks

1. Store your **name** and **university name** using variables.
2. Create a variable for:
   - GDP of Pakistan in 2023
   - Inflation rate in January
   - Your monthly income (real or imaginary 😄)
3. Add two income sources and find your **total income**.

---

Stay curious, and get ready to write your first lines of code!

