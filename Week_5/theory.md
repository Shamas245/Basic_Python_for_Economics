
# Week 5: Loops & Functions — Automated Price/Income Checks

## 🎯 Learning Objectives

By the end of this week, you will:

* Understand `for` and `while` loops in Python for repetitive tasks.
* Create reusable functions to simplify economic analysis.
* Automate data processing tasks like checking prices, incomes, or GDP across time or regions.

---

## 1. 🔁 What Are Loops?

Loops let you **repeat actions** without writing the same code over and over. This is useful in economics when checking values across:

* Multiple years
* Different regions
* Large datasets

---

### 🔹 `for` Loop

Used when you know **how many times** you want to repeat something (e.g., checking prices in a list).

```python
prices = [120, 145, 110, 130]

for price in prices:
    if price > 125:
        print("Above threshold:", price)
    else:
        print("Within normal range:", price)
```

---

### 🔹 `while` Loop

Used when you want to repeat something **until a condition is no longer true**.

```python
income = 2000

while income < 3000:
    print("Below target income:", income)
    income += 250
```

---

## 2. 📦 Applications in Economics

### 🧾 Example: Automated Income Check for Regions

```python
region_incomes = {
    "North": 2400,
    "South": 3100,
    "East": 2900,
    "West": 3300
}

for region, income in region_incomes.items():
    if income >= 3000:
        print(f"{region}: High income region")
    else:
        print(f"{region}: Needs economic support")
```

---

### 🧾 Example: Checking Price Deviations

```python
product_prices = [115, 130, 99, 140, 155]

for price in product_prices:
    if price > 140:
        print("Price alert! Overpriced item detected:", price)
```

---

## 3. 🧠 What Are Functions?

Functions are blocks of code that you can **define once and reuse**. In economics, we use them to:

* Calculate inflation or GDP growth
* Compare price indexes
* Process multiple inputs like regions or products

---

### 🔹 Function Syntax

```python
def function_name(parameters):
    # Code block
    return result
```

---

### 📌 Example 1: Inflation Decision Function

```python
def check_inflation(inflation_rate):
    if inflation_rate > 3:
        return "Raise interest rates"
    else:
        return "Keep rates stable"

print(check_inflation(3.2))
```

---

### 📌 Example 2: Income Classification Function

```python
def classify_income(income):
    if income >= 3000:
        return "High income"
    elif income >= 2000:
        return "Middle income"
    else:
        return "Low income"

print(classify_income(2100))
```

---

### 📌 Example 3: Automated Check on a List

```python
def income_alert(region, income):
    if income < 2500:
        return f"{region}: Needs attention"
    else:
        return f"{region}: Satisfactory"

regions = {
    "A": 2300,
    "B": 2800,
    "C": 1900,
    "D": 3100
}

for region, income in regions.items():
    print(income_alert(region, income))
```

---

## 4. ⛏️ Combining Loops and Functions

This combination helps build **automated economic systems**, like:

* Monthly checks for price spikes
* Flagging regions needing aid
* Running calculations over large datasets

### 🧾 Example: Loop + Function

```python
def is_price_volatile(price):
    return price > 150 or price < 90

prices = [100, 85, 160, 120, 140]

for p in prices:
    if is_price_volatile(p):
        print("Volatile price detected:", p)
```

---

## 5. ✅ Best Practices

* **Use meaningful function names**: e.g., `check_inflation`, not `func1`
* **Keep functions short** and focused on one task.
* **Reuse functions** when applying the same rule to different data.

---

## 📝 Exercises (In Jupyter Notebook)

1. Use a `for` loop to check if product prices are above or below a threshold.
2. Write a function to classify incomes as low, middle, or high.
3. Automate price checking for a list of products using functions and loops.
4. Use a `while` loop to simulate increasing GDP until it reaches a target value.

---

