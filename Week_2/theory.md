# Week 2: Operators & Expressions

## Learning Objectives
By the end of this week, you will:

- Understand Python operators (arithmetic, comparison, logical, assignment).
- Learn how to write and evaluate expressions.
- Apply operators to economic data, such as interest rate calculations and Consumer Price Index (CPI) comparisons.

---

## 1. Arithmetic Operators
Arithmetic operators perform mathematical operations, essential for calculations like interest rates or CPI adjustments.

| Operator | Description       | Example       |
|----------|-------------------|---------------|
| +        | Addition           | 5 + 3 = 8     |
| -        | Subtraction        | 5 - 3 = 2     |
| *        | Multiplication     | 5 * 3 = 15    |
| /        | Division           | 6 / 2 = 3.0   |
| //       | Floor Division     | 7 // 2 = 3    |
| %        | Modulus            | 7 % 2 = 1     |
| **       | Exponentiation     | 2 ** 3 = 8    |

**Economic Example:**
Calculate simple interest using the formula:
```python
I = P * R * T / 100
# where P is principal, R is rate, and T is time
```

---

## 2. Comparison Operators
Comparison operators compare two values and return `True` or `False`, useful for comparing economic indicators like CPI across months.

| Operator | Description           | Example         |
|----------|-----------------------|-----------------|
| ==       | Equal to              | 5 == 5: True    |
| !=       | Not equal to          | 5 != 3: True    |
| >        | Greater than          | 5 > 3: True     |
| <        | Less than             | 3 < 5: True     |
| >=       | Greater than or equal | 5 >= 5: True    |
| <=       | Less than or equal    | 3 <= 5: True    |

**Economic Example:**
```python
cpi_current > cpi_previous  # Check if inflation is rising
```

---

## 3. Logical Operators
Logical operators combine conditions, often used in decision-making for economic policies.

| Operator | Description                         | Example                             |
|----------|-------------------------------------|-------------------------------------|
| and      | True if both conditions are True     | (5 > 3) and (2 < 4): True            |
| or       | True if at least one is True         | (5 > 6) or (2 < 4): True             |
| not      | Reverses the condition               | not (5 > 3): False                   |

**Economic Example:**
```python
inflation > 3 and unemployment > 5  # Trigger policy
```

---

## 4. Assignment Operators
Assignment operators assign values to variables, often used to update economic metrics.

| Operator | Description         | Example                      |
|----------|---------------------|------------------------------|
| =        | Assign value        | x = 10                       |
| +=       | Add and assign      | x += 5  # x = x + 5          |
| -=       | Subtract and assign | x -= 3  # x = x - 3          |
| *=       | Multiply and assign | x *= 2  # x = x * 2          |
| /=       | Divide and assign   | x /= 2  # x = x / 2          |

**Economic Example:**
```python
savings += interest  # Update total savings
```

---

## 5. Expressions
An expression combines values, variables, and operators to compute a value.

**Examples:**
```python
total_cost = price * quantity
is_inflation_high = cpi > 3 and cpi_previous < cpi
```

**Economic Example:**
Calculate compound interest:
```python
A = P * (1 + R/100) ** T
# A is the final amount
```

---

## Key Applications
- **Interest Calculations:** Use arithmetic operators to compute simple or compound interest for loans or savings.
- **CPI Comparisons:** Use comparison and logical operators to analyze inflation trends.
- **Policy Triggers:** Combine logical operators to model economic decision rules (e.g., adjust rates if inflation > 3% and GDP growth < 2%).

---

## Exercises (In Notebook)
- Calculate simple interest for a loan.
- Compare CPI values across two months to detect inflation trends.
- Use logical operators to check if economic conditions warrant policy changes.

---

## Next Week
**Lists, strings, and indexing** for handling monthly inflation data and wage storage.

