
### Week 7: Data Analysis with pandas and NumPy

#### Learning Objectives

By the end of this week, you will:

* Understand the basics of pandas and NumPy for data analysis.
* Learn to read, manipulate, and analyze CSV files.
* Apply statistical computations and filtering to economic datasets.

---

### 1. Introduction to pandas and NumPy

**pandas**: A Python library for data manipulation and analysis, ideal for handling tabular data like economic datasets.

**NumPy**: A library for numerical computations, providing efficient array operations for statistical analysis.

**Economic Example**: Use pandas to analyze a CSV of CPI data and NumPy to compute average inflation rates.

---

### 2. Reading and Exploring CSV Files with pandas

CSV files are common for storing economic data (e.g., GDP, unemployment rates). pandas makes it easy to read and explore them.

**Key Operations**

| Operation | Description                 | Example                        |
| --------- | --------------------------- | ------------------------------ |
| Read CSV  | Load CSV into a DataFrame   | `df = pd.read_csv("data.csv")` |
| View Data | Display first rows          | `df.head()`                    |
| Get Info  | Show columns and data types | `df.info()`                    |
| Describe  | Summary statistics          | `df.describe()`                |

**Example**: Load a CSV with monthly CPI and unemployment data.

```python
import pandas as pd
df = pd.read_csv("economic_data.csv")
print(df.head())
```

---

### 3. Basic Data Manipulation with pandas

pandas DataFrames allow you to select, filter, and modify data.

**Key Operations**

* **Select Columns**: `df["column_name"]` or `df[["col1", "col2"]]`.
* **Select Rows**: `df.iloc[0:5]` (index-based) or `df.loc[df["CPI"] > 250]` (condition-based).
* **Add Column**: `df["new_col"] = df["CPI"] * 1.05`.
* **Drop Column**: `df.drop("column_name", axis=1)`.

**Economic Example**: Calculate year-over-year CPI change.

```python
df["CPI_Change"] = df["CPI"] - df["CPI"].shift(1)
print(df[["Month", "CPI", "CPI_Change"]].head())
```

---

### 4. Statistical Computations with NumPy

NumPy provides fast array operations for statistical analysis.

**Key Functions**

| Function           | Description         | Example                |
| ------------------ | ------------------- | ---------------------- |
| Mean               | Compute average     | `np.mean(df["CPI"])`   |
| Median             | Compute median      | `np.median(df["CPI"])` |
| Standard Deviation | Measure variability | `np.std(df["CPI"])`    |
| Sum                | Compute total       | `np.sum(df["GDP"])`    |

**Example**: Calculate average and standard deviation of unemployment rates.

```python
import numpy as np
avg_unemployment = np.mean(df["Unemployment"])
std_unemployment = np.std(df["Unemployment"])
print(f"Average Unemployment: {avg_unemployment:.2f}%")
print(f"Std Deviation: {std_unemployment:.2f}%")
```

---

### 5. Filtering Data with pandas

Filtering selects rows based on conditions, crucial for analyzing specific economic scenarios.

**Key Techniques**

* **Single Condition**: `df[df["CPI"] > 250]`.
* **Multiple Conditions**: `df[(df["CPI"] > 250) & (df["Unemployment"] < 5)]`.
* **Query Method**: `df.query("CPI > 250 and Unemployment < 5")`.

**Economic Example**: Filter regions with high inflation and low unemployment.

```python
high_inflation_low_unemp = df[(df["CPI"] > 250) & (df["Unemployment"] < 5)]
print(high_inflation_low_unemp[["Region", "CPI", "Unemployment"]])
```

---

### 6. Applications in Economics

* **CSV Analysis**: Load and summarize economic datasets (e.g., GDP, CPI, unemployment).
* **Statistical Insights**: Compute metrics like average inflation or GDP growth variability.
* **Filtering**: Identify regions or periods meeting policy criteria (e.g., high CPI and low GDP growth).
* **Data Cleaning**: Handle missing values or outliers in economic data.

**Example**: Analyze a CSV to find months with CPI above the annual average.

```python
avg_cpi = np.mean(df["CPI"])
above_avg_cpi = df[df["CPI"] > avg_cpi]
print(above_avg_cpi[["Month", "CPI"]])
```

---

### 7. Best Practices

* **Check Data**: Use `df.info()` and `df.head()` to verify CSV contents.
* **Handle Missing Data**: Use `df.dropna()` or `df.fillna(value)` for incomplete datasets.
* **Use Descriptive Names**: Name DataFrames and columns clearly (e.g., `cpi_df` instead of `df1`).
* **Optimize with NumPy**: Use NumPy for large-scale numerical computations to improve performance.

---

### Exercises (In Notebook)

1. Load a CSV file with economic data and display summary statistics.
2. Calculate the average and standard deviation of GDP values using NumPy.
3. Filter a DataFrame to show months with CPI above 255.
4. Create a new column for inflation rate based on CPI changes.
5. Identify regions with unemployment below 4% and CPI above 250.

---

### Next Week: Data visualization with Matplotlib for GDP charts and inflation plots.

---

