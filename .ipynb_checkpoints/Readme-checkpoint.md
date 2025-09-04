# BrainyBeam Data Analysis & Visualization Tasks (1–5)

This repository contains five tasks demonstrating **data manipulation and visualization** using **Pandas, NumPy, and Matplotlib**.
Each task focuses on a specific concept, building skills in data analysis and plotting.

---

## 📑 Task Overview

### **Task 1 – Custom DataFrame Transformation**

* **Goal**: Apply a custom normalization function to grouped data.
* **Key Methods**:

  * `pd.DataFrame()` → Create DataFrame from dictionary.
  * `groupby()` + `apply()` → Apply custom normalization within groups.
  * `reset_index()` → Clean up index after applying group operations.
* **Learning**: Custom functions can be applied to groups, making transformations flexible.

---

### **Task 2 – Managing Hierarchical Indexing**

* **Goal**: Work with multi-level (hierarchical) indexing in Pandas.
* **Key Methods**:

  * `set_index(["col1","col2"])` → Create hierarchical index.
  * `.loc[(level1, level2)]` → Access data using multi-index keys.
  * `groupby()` + `mean()` → Group and aggregate values (e.g., average fare).
  * `reset_index()` → Convert index back to columns.
  * `swaplevel()` → Change priority of index levels.
* **Learning**: MultiIndex enables complex selection and aggregation.

---

### **Task 3 – Visualizing High-Dimensional Data**

* **Goal**: Use **parallel coordinates plot** to visualize multi-dimensional features.
* **Key Methods**:

  * `parallel_coordinates(df, 'class_column', color=[...])` → Plot multiple features by category.
  * `plt.figure(figsize=(...))` → Control figure size.
  * `plt.show()` → Render plot.
* **Learning**: Parallel coordinates help identify feature patterns across categories.

---

### **Task 4 – Multiple Y-Axes with Shared X-Axis**

* **Goal**: Plot two different functions with separate Y-axes but a shared X-axis.
* **Key Methods**:

  * `plt.subplots()` → Create figure and axis (`ax1`).
  * `ax1.twinx()` → Create a second Y-axis (`ax2`).
  * `ax1.plot()`, `ax2.plot()` → Plot different data series.
  * `set_xlabel()`, `set_ylabel()`, `set_title()` → Customize labels and title.
* **Learning**: `twinx()` is powerful for comparing datasets with different scales.

---

### **Task 5 – Custom Complex Plot (OO API)**

* **Goal**: Create a styled plot using Matplotlib’s Object-Oriented API.
* **Key Methods**:

  * `np.linspace()` → Generate evenly spaced values.
  * `ax.plot()` → Plot sine and cosine with different styles (`g--`, `r-.`).
  * `ax.legend()` → Add legend.
  * `ax.grid(linestyle=':')` → Add styled grid.
  * `set_title()`, `set_xlabel()`, `set_ylabel()` → Customize text elements.
* **Learning**: The **OO API** in Matplotlib allows flexible and professional customization.

---

## 🚀 Combined Learnings

* **Task 1 & 2**: Show how Pandas can manipulate and group structured datasets.
* **Task 3**: Demonstrates visualization of **high-dimensional categorical data**.
* **Task 4 & 5**: Show advanced plotting techniques using Matplotlib.
* Together, they provide a foundation in **data wrangling and visualization** for analytics.

---

## ▶️ How to Run

1. Clone the repository or download the `.ipynb` files.
2. Install dependencies:

   ```bash
   pip install pandas matplotlib numpy
   ```
3. Run Jupyter Notebook:

   ```bash
   jupyter notebook
   ```
4. Open any task file (`BrainyBeam_Task_X.ipynb`) and execute cells step by step.

## Reach Out to me:
**Email:vrund0406@gmail.com**
Thank you for visiting this Repo!