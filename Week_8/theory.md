
### **Week 8: Data Visualization with Matplotlib**

#### 🎯 **What You’ll Learn This Week:**

By the end of this week, you’ll be able to:

* Understand how Matplotlib works for making graphs and charts.
* Create **line plots**, **bar charts**, and **scatter plots** using Python.
* Use these plots to study trends like GDP growth and inflation.

---

### **1. What is Matplotlib?**

**Matplotlib** is a Python library that helps you **make graphs** from your data. It is very useful when you want to see trends or patterns in economic data like:

* **GDP (Gross Domestic Product)**
* **CPI (Consumer Price Index)**
* **Unemployment Rate**

**Main tool used:**

```python
import matplotlib.pyplot as plt
```

You can show your plot using `plt.show()` or save it as an image using `plt.savefig("name.png")`.

---

### **2. How to Start Using Matplotlib**

Usually, in Google Colab, you don’t need to install Matplotlib—it’s already there.

Just import the libraries:

```python
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
```

🔸 **Tip**: In Google Colab, use `plt.savefig("myplot.png")` to save your plots as images. This helps you keep a copy of your work.

---

### **3. Types of Graphs You Can Make**

#### ✅ **Line Plot** – for Trends Over Time

Great for plotting something like monthly inflation or GDP growth.

```python
months = ["Jan", "Feb", "Mar", "Apr"]
cpi = [250.5, 252.3, 251.8, 253.1]

plt.plot(months, cpi, marker="o", label="CPI")
plt.title("Monthly CPI Trend")
plt.xlabel("Month")
plt.ylabel("CPI")
plt.legend()
plt.grid(True)
plt.savefig("cpi_trend.png")
```

---

#### ✅ **Bar Chart** – for Comparing Categories

Good for comparing GDP between different regions.

```python
regions = ["North", "South", "East"]
gdp = [500, 450, 600]

plt.bar(regions, gdp, color="blue")
plt.title("Regional GDP Comparison")
plt.xlabel("Region")
plt.ylabel("GDP (Billions)")
plt.savefig("gdp_bar.png")
```

---

#### ✅ **Scatter Plot** – for Relationships Between Variables

Used to see how two things are related, like CPI and unemployment.

```python
unemployment = [5.8, 5.5, 5.9, 5.7]

plt.scatter(cpi, unemployment, color="red")
plt.title("CPI vs. Unemployment")
plt.xlabel("CPI")
plt.ylabel("Unemployment (%)")
plt.savefig("cpi_unemployment_scatter.png")
```

---

### **4. Plotting Data from a CSV File**

You can also use data from a `.csv` file. This is where you combine **pandas (Week 7)** and **Matplotlib**.

```python
df = pd.read_csv("economic_data.csv")
plt.plot(df["Month"], df["CPI"], marker="o", label="CPI")
plt.title("CPI Trend from CSV")
plt.xlabel("Month")
plt.ylabel("CPI")
plt.legend()
plt.grid(True)
plt.savefig("cpi_from_csv.png")
```

You can also plot **GDP growth** or any other column from your file in a similar way.

---

### **5. Make Your Plots Look Better**

You can customize your plots to make them more clear and attractive:

| **Feature** | **What it Does**                | **Example**                               |
| ----------- | ------------------------------- | ----------------------------------------- |
| Title       | Adds a name to the chart        | `plt.title("GDP Trend")`                  |
| X/Y Labels  | Shows what each axis means      | `plt.xlabel("Year")`, `plt.ylabel("GDP")` |
| Legend      | Adds labels for different lines | `plt.legend()`                            |
| Grid        | Adds background gridlines       | `plt.grid(True)`                          |
| Color       | Changes line or bar colors      | `color="green"`                           |
| Marker      | Adds dots or shapes to lines    | `marker="o"`                              |

#### 📊 Example:

```python
years = [2020, 2021, 2022, 2023]
gdp = [1800, 1900, 1950, 2000]

plt.plot(years, gdp, color="green", marker="s", label="GDP")
plt.title("Annual GDP Growth")
plt.xlabel("Year")
plt.ylabel("GDP (Billions)")
plt.legend()
plt.grid(True)
plt.savefig("gdp_growth.png")
```

---

### **6. How to Use Visualizations in Economics**

✅ **GDP Charts**
See how GDP changes over time or compare it across different regions.

✅ **Inflation Plots**
Understand how CPI rises or falls monthly or yearly.

✅ **Economic Relationships**
Check if there’s a connection between CPI and unemployment using a scatter plot.

✅ **Policy Analysis**
Use your charts to support reports or research findings.

#### 📊 Example: Plot CPI and Unemployment Together

```python
plt.plot(df["Month"], df["CPI"], marker="o", label="CPI")
plt.plot(df["Month"], df["Unemployment"], marker="s", label="Unemployment")
plt.title("CPI and Unemployment Trends")
plt.xlabel("Month")
plt.ylabel("Value")
plt.legend()
plt.grid(True)
plt.savefig("cpi_unemployment_trend.png")
```

---

### **7. Tips and Best Practices**

* ✅ **Always label** your chart, x-axis, y-axis, and lines.
* ✅ **Don’t add too much info** in one graph—keep it clean.
* ✅ **Save your plots** using `plt.savefig("filename.png")`.
* ✅ **Use pandas** to handle your data quickly.
* ✅ **Test your code** in Google Colab to see if everything works.

---

### ✅ **Practice Tasks (Do These in Your Notebook):**

1. 📈 Make a **line plot** of monthly CPI values from a CSV file.
2. 📊 Create a **bar chart** comparing GDP in different regions.
3. 🔴 Plot a **scatter graph** of CPI vs. unemployment.
4. 🟪 Make a plot that shows both **CPI and GDP** on the same graph.
5. 🎨 Customize any plot with a **title, labels, grid, and legend**.

---

### 🎉 **Wrap-Up**

**Congratulations!** 🎓
You’ve now learned how to **make, customize, and understand economic graphs using Python**.

These skills will help you:

* Present your research in a better way
* Analyze trends quickly
* Make data-driven economic decisions

---

