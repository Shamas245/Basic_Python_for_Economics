# Week 3: Lists, Strings & Indexing

## Learning Objectives
By the end of this week, you will:

- Understand Python lists and their operations for storing and manipulating data.
- Learn string manipulation and indexing techniques.
- Apply lists and strings to economic data, such as monthly inflation rates and wage storage.

---

## 1. Lists

Lists are ordered, mutable collections of items, ideal for storing sequences like monthly inflation rates or wage data.

### 🔑 Key Operations

| Operation | Description              | Example                            |
|----------|--------------------------|------------------------------------|
| Create   | Define a list             | `rates = [2.5, 2.7, 3.0]`          |
| Access   | Get item by index (0-based) | `rates[0]` → `2.5`              |
| Modify   | Change item by index      | `rates[1] = 2.8`                   |
| Append   | Add item to end           | `rates.append(3.2)`               |
| Remove   | Remove item               | `rates.remove(2.5)`               |
| Pop      | Remove and return by index | `rates.pop(0)` → `2.5`          |
| Sort     | Sort list in place        | `rates.sort()` → `[2.5, 2.7, 3.0]` |
| Length   | Number of items           | `len(rates)` → `3`               |

**Economic Example**:  
Store monthly CPI values in a list:
```python
cpi = [250.5, 252.3, 251.8]
average = sum(cpi) / len(cpi)
```

### 🔹 Slicing
Extract a subset using `list[start:end]`.  
Example: `rates[1:3]` → `[2.7, 3.0]`  
Negative indexing: `rates[-1]` → `3.0`

### 🔄 Iteration
Use loops to process each item, e.g., compute CPI difference:
```python
cpi = [250.5, 252.3]
diff = cpi[1] - cpi[0]  # 1.8
```

### 💡 Tips
- Check list length before accessing (e.g., `if i < len(rates)`).
- Use `sort()` to find highest inflation rate or wage.

---

## 2. Strings

Strings are immutable sequences of characters, useful for handling text data like region names or economic indicators.

### 🔑 Key Operations

| Operation     | Description           | Example                           |
|---------------|-----------------------|-----------------------------------|
| Create        | Define a string       | `region = "North"`                |
| Access        | Get character by index| `region[0]` → "N"               |
| Concatenate   | Join strings          | `"North" + "South"` → "NorthSouth" |
| Length        | Number of characters  | `len(region)` → `5`             |
| Upper/Lower   | Change case           | `region.upper()` → `"NORTH"`    |

**Economic Example**:  
Store a region name (`"North"`) and convert it to uppercase for reporting.

### 🔹 String Methods
- `split()`: Split string into list  
  Example: `"Jan,Feb,Mar".split(",")` → `['Jan', 'Feb', 'Mar']`
- `strip()`: Remove whitespace  
  Example: `" GDP ".strip()` → `"GDP"`

---

## 3. Indexing and Slicing

Indexing accesses individual elements, while slicing extracts a range of elements. Both apply to lists and strings.

- **Indexing**: `list[0]` or `string[0]` (0-based)
- **Slicing**: `list[start:end]` or `string[start:end]` (end exclusive)
- **Negative Indexing**: Access from end, e.g., `list[-1]`

**Economic Example**:  
Extract the first three months' inflation rates from a list: `inflation_rates[:3]`  
Get a substring from a region name: `region[0:2]` → `"No"`

---

## 4. Applications in Economics

- **Monthly Inflation**: Store CPI values in a list, access specific months, or calculate changes (`cpi[1] - cpi[0]`).
- **Wage Storage**: Store employee wages in a list, update values, or compute averages.
- **Text Processing**: Use strings to format economic reports, e.g., concatenate region and indicator: `"North" + " CPI"`

---

## 📜 Exercises (In Notebook)

1. Create a list of monthly inflation rates and compute the average.
2. Use slicing to extract the first quarter's CPI values.
3. Sort a list of wages to find the highest earner.
4. Manipulate a region name string (e.g., convert to uppercase, extract first two characters).
5. Split a comma-separated string of economic indicators into a list.

---

## 📅 Next Week
Conditional statements for policy rules and decision-making.

