
# Week 6: Dictionaries & Functions — Region-wise GDP, Subsidies

## 🎯 Learning Objectives

By the end of this week, you will:

* Understand how to create and access dictionaries in Python.
* Use functions to process and analyze region-wise economic data.
* Automate tasks like checking GDP thresholds or calculating subsidies for different regions.

---

## 1. 📚 Introduction to Dictionaries

Dictionaries store data in **key-value pairs**. They’re ideal for mapping region names to GDP, inflation, unemployment, or subsidy amounts.

```python
# Example: Region-wise GDP
gdp_data = {
    "North": 3200,
    "South": 2800,
    "East": 3100,
    "West": 2900
}
```

* **Keys** = Region names
* **Values** = Associated economic data

---

## 2. 🔎 Accessing and Modifying Dictionaries

### ✅ Access a Value

```python
print(gdp_data["South"])  # Output: 2800
```

### ✏️ Modify a Value

```python
gdp_data["South"] = 3000
```

### ➕ Add a New Key-Value Pair

```python
gdp_data["Central"] = 2700
```

### ❌ Remove a Key

```python
del gdp_data["West"]
```

---

## 3. 🔁 Looping Through Dictionaries

To analyze all regions:

```python
for region, gdp in gdp_data.items():
    print(f"{region}: GDP = {gdp}")
```

---

## 4. ⚙️ Functions with Dictionaries

Using functions makes economic checks reusable and organized.

---

### 📌 Example 1: GDP Classification Function

```python
def classify_gdp(region, gdp):
    if gdp >= 3000:
        return f"{region}: High GDP"
    elif gdp >= 2500:
        return f"{region}: Medium GDP"
    else:
        return f"{region}: Low GDP"
```

Looping through data:

```python
for region, gdp in gdp_data.items():
    print(classify_gdp(region, gdp))
```

---

### 📌 Example 2: Subsidy Allocation Based on GDP

```python
def calculate_subsidy(gdp):
    if gdp < 2800:
        return 500
    elif gdp < 3000:
        return 300
    else:
        return 100
```

Apply to each region:

```python
for region, gdp in gdp_data.items():
    subsidy = calculate_subsidy(gdp)
    print(f"{region}: Subsidy = {subsidy}")
```

---

## 5. 🧠 Advanced Use: Multiple Indicators

You can use **nested dictionaries** for richer economic data.

```python
eco_data = {
    "North": {"gdp": 3200, "inflation": 2.5},
    "South": {"gdp": 2700, "inflation": 3.2}
}

for region, data in eco_data.items():
    gdp = data["gdp"]
    inflation = data["inflation"]
    print(f"{region} — GDP: {gdp}, Inflation: {inflation}")
```

---

## 6. ✅ Best Practices

* Use **clear key names** (e.g., `"gdp"`, `"inflation"`).
* Create **functions** for repeated rules (e.g., subsidy, classification).
* Use **loops** with functions for clean and scalable code.

---

## 📝 Exercises (In Notebook)

1. Store GDP data for 5 regions in a dictionary.
2. Write a function to calculate subsidies for each region based on GDP. If GDP is below 2800, assign a higher subsidy. If it’s between 2800 and 3000, assign a medium subsidy. Otherwise, assign a lower subsidy.
3. Apply these functions to a dictionary containing GDP data for various regions and print out the results for each region.