# Task 3 – Visualizing High-Dimensional Data

This task demonstrates **visualization of high-dimensional categorical data** using **parallel coordinates plots** in Python with Pandas and Matplotlib. The dataset used is `GenderData.csv`, which contains various facial attributes along with gender classification.

---

## 📌 Steps and Main Functions Used

### 1. **Importing Required Libraries**

```python
import pandas as pd
import matplotlib.pyplot as plt
from pandas.plotting import parallel_coordinates
```

* **`pandas`**: For handling and manipulating structured tabular data.
* **`matplotlib.pyplot`**: Used for plotting and visualization.
* **`parallel_coordinates`**: A Pandas plotting utility to visualize multi-dimensional categorical data.

---

### 2. **Loading Dataset**

```python
df = pd.read_csv("GenderData.csv")
df.head()
```

* **`pd.read_csv()`**: Reads CSV file into a Pandas DataFrame.
* **`df.head()`**: Displays the first 5 rows to quickly inspect the dataset.

---

### 3. **Inspecting Data Columns**

```python
df.columns
```

* Returns all column names of the dataset, helping to identify which features are useful for visualization.

---

### 4. **Selecting Relevant Features**

```python
df_need = df[['long_hair','nose_long', 'lips_thin','distance_nose_to_lip_long','gender']]
df_need.head()
```

* Creates a subset DataFrame with selected attributes relevant for analysis.
* Helps reduce noise and focus only on features needed for classification.

---

### 5. **Plotting Parallel Coordinates**

```python
plt.figure(figsize=(12,6))
parallel_coordinates(df_need,'gender',color=["blue","violet"])
plt.show()
```

* **`plt.figure(figsize=(12,6))`**: Sets up a large figure for better readability.
* **`parallel_coordinates(df_need, 'gender', color=[...])`**: Plots high-dimensional data with each feature on a parallel axis, grouped by the `gender` category.
* **`plt.show()`**: Renders and displays the plot.

---

## 📊 Output

The parallel coordinates plot allows us to visualize multiple features simultaneously and observe how different categories (`gender`) behave across dimensions. This helps in detecting patterns and separability in the dataset.

---

## 🚀 Key Learnings

* Parallel coordinates are useful for **visualizing multi-dimensional datasets**.
* Pandas and Matplotlib provide simple yet powerful tools for data exploration.
* Feature selection plays a key role in improving clarity of visualizations.