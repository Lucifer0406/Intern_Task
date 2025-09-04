# Task 1 – Custom DataFrame Transformation with GroupBy and Apply

This task demonstrates how to create a **custom transformation function** in Pandas and apply it to groups within a dataset. The dataset contains department-wise employee salary information.

---

## 📌 Steps and Main Functions Used

### 1. **Importing Pandas and Creating a DataFrame**

```python
import pandas as pd

data = {
    "Department":["HR","HR","IT","IT","Finance","Finance"],
    "Employee":["A","B","C","D","E","F"],
    "Salary":[3000,3500,5000,5500,7000,7200]
}
df = pd.DataFrame(data)
df
```

* **`pd.DataFrame(data)`**: Creates a structured DataFrame from a dictionary.
* Represents employee salary data across departments.

---

### 2. **Defining a Custom Function**

```python
def normalize(series):
    return (series - series.mean())/series.std()
```

* Defines a **normalization function** that scales values relative to the group’s mean and standard deviation.
* Formula:

  $$
  z = \frac{x - \mu}{\sigma}
  $$

  where $\mu$ is mean and $\sigma$ is standard deviation.

---

### 3. **Applying Function with GroupBy**

```python
df["Normalized_Salary"] = df.groupby("Department")["Salary"].apply(normalize).reset_index(level=0,drop=True)
df
```

* **`groupby("Department")`**: Splits the data by department.
* **`apply(normalize)`**: Applies the custom normalization function to each department group.
* **`reset_index(level=0, drop=True)`**: Removes the extra index added during groupby operations.
* A new column **`Normalized_Salary`** is created, showing department-wise normalized salaries.

---

## 📊 Output

* Each department’s salary values are normalized independently.
* This ensures fair comparison across departments regardless of different pay scales.

---

## 🚀 Key Learnings

* **Custom functions** can be applied to grouped data using `.apply()`.
* **GroupBy operations** allow transformations within logical subsets of a dataset.
* Normalization helps in **standardizing data** for analysis and comparison.