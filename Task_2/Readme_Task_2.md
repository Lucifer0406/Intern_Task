# Task 2 – Managing Hierarchical Indexing in Pandas

This task demonstrates how to work with **hierarchical (multi-level) indexing** in Pandas using the Titanic dataset (`tested.csv`). Hierarchical indexing allows more complex data selection and grouping operations.

---

## 📌 Steps and Main Functions Used

### 1. **Importing Pandas**

```python
import pandas as pd
```

* **`pandas`**: A core library for data manipulation and analysis.

---

### 2. **Loading Dataset**

```python
df = pd.read_csv("tested.csv")
df
```

* **`pd.read_csv()`**: Loads CSV data into a Pandas DataFrame.
* Displays the entire dataset for inspection.

---

### 3. **Setting Multi-Level Index**

```python
df_multi = df.set_index(["Pclass","Sex"])
df_multi.head()
```

* **`set_index(["Pclass","Sex"])`**: Creates a hierarchical index using **Passenger Class (`Pclass`)** and **Sex (`Sex`)**.
* Allows multi-dimensional slicing and grouping.

---

### 4. **Accessing Data with MultiIndex**

```python
df_multi.loc[(3,"male")].head()
```

* **`.loc[]`**: Selects rows based on hierarchical index.
* Here, it retrieves all rows where `Pclass = 3` and `Sex = male`.

---

### 5. **Grouping and Aggregation**

```python
avg_fare = df_multi["Fare"].groupby(["Pclass", "Sex"]).mean()
avg_fare
```

* **`groupby(["Pclass", "Sex"])`**: Groups passengers by class and sex.
* **`.mean()`**: Calculates the average fare for each group.

---

### 6. **Resetting Index**

```python
df_reset = df_multi.reset_index()
df_reset.head()
```

* **`reset_index()`**: Converts the MultiIndex back into regular columns.
* Useful for flattening hierarchical data into a simpler DataFrame.

---

### 7. **Swapping Index Levels**

```python
df_swapped = df_multi.swaplevel()
df_swapped.head()
```

* **`swaplevel()`**: Exchanges the order of hierarchical index levels.
* This helps when you want to prioritize a different index key for analysis.

---

## 📊 Output

* Multi-level indexing provides more structured access to data.
* Grouped analysis (e.g., average fare per class and gender) becomes intuitive.
* Resetting and swapping index levels improve flexibility for further analysis.

---

## 🚀 Key Learnings

* Hierarchical indexing is powerful for working with complex datasets.
* Selection with `.loc[]` becomes more expressive using multiple keys.
* Aggregation with `groupby()` is easier when combined with MultiIndex.