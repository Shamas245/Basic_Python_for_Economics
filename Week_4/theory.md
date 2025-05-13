# Week 4: Conditional Statements — Policy Rules & Decision-Making

## 🎯 Learning Objectives

By the end of this week, you will:

* Understand how `if`, `elif`, and `else` statements work in Python.
* Use logical and comparison operators to control decision flows.
* Apply conditionals to real-world economic logic, such as:

  * Interest rate policy rules
  * Categorizing inflation levels
  * Automating policy responses based on data

---

## 1. 🧠 What Are Conditional Statements?

Conditional statements allow programs to make **decisions**.

They evaluate a condition, and based on whether it's `True` or `False`, they execute specific code blocks — a powerful tool for automating **economic decision-making**.

### 🔹 Syntax

```python
if condition:
    # Runs this block if condition is True
elif another_condition:
    # Runs this if the above is False but this is True
else:
    # Runs if none of the above conditions are True
```

---

## 2. 📊 Economic Examples

### Example 1: Interest Rate Decision Rule

```python
inflation = 3.5

if inflation > 3:
    print("Raise interest rates.")
else:
    print("No change in interest rates.")
```

### Example 2: GDP and Stability

```python
gdp_growth = 1.8

if gdp_growth >= 2:
    print("Economy is stable.")
else:
    print("Consider a stimulus package.")
```

---

## 3. 🔀 If-Elif-Else: Multiple Decision Branches

Used when you need to classify or categorize economic indicators.

### Example: Inflation Categories

```python
cpi = 252.3

if cpi < 250:
    print("Low inflation.")
elif cpi <= 255:
    print("Moderate inflation.")
else:
    print("High inflation.")
```

---

## 4. 🔎 Logical and Comparison Operators

These help us form **compound conditions**.

| Type       | Operators                        |
| ---------- | -------------------------------- |
| Comparison | `==`, `!=`, `>`, `<`, `>=`, `<=` |
| Logical    | `and`, `or`, `not`               |

### Example: Dual-condition Policy Trigger

```python
inflation = 3.4
unemployment = 6.2

if inflation > 3 and unemployment > 6:
    print("Trigger fiscal intervention.")
```

---

## 5. 🪜 Nested Conditionals: Layered Economic Logic

You can use one `if` block inside another for complex rules.

### Example: Inflation + GDP Rule

```python
inflation = 3.2
gdp_growth = 1.5

if inflation > 3:
    if gdp_growth < 2:
        print("Tighten monetary policy.")
    else:
        print("Wait and monitor.")
else:
    print("No policy change needed.")
```

---

## 6. 🧠 Real-World Applications in Economics

### 📌 1. Policy Rules

Model decisions like:

* Adjust interest rates if inflation exceeds a threshold
* Trigger fiscal packages if unemployment rises

### 📌 2. Data Categorization

Use `if-elif-else` to label economic indicators for analysis.

### 📌 3. Decision Automation

Use conditionals to **flag regions** or periods needing action.

#### Example: Unemployment Classifier

```python
unemployment = 5.8
region = "South"

if unemployment < 4:
    print(f"{region}: Low unemployment.")
elif unemployment <= 6:
    print(f"{region}: Moderate unemployment.")
else:
    print(f"{region}: High unemployment.")
```

---

## 7. ✅ Best Practices

* **Use descriptive variables** like `inflation`, `gdp_growth` — not `x`, `y`.
* **Keep nesting shallow** — too many layers make code hard to read.
* **Always cover all cases** using `else` as a safety net.

---

## 📝 Exercises (In Jupyter Notebook)

1. Write a program that decides whether to raise interest rates based on inflation.
2. Categorize CPI values as low, moderate, or high inflation.
3. Use nested conditionals to recommend monetary policy using inflation and GDP growth.
4. Write a loop over regions and flag any with unemployment above 5%.

---

