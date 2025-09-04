# Task 5 – Custom Complex Plot using Matplotlib (Object-Oriented API)

This task demonstrates how to create a **customized plot** using Matplotlib’s **Object-Oriented API**. Two functions (`sin(x)` and `cos(x)`) are plotted with different styles, along with legends, grid, labels, and a title.

---

## 📌 Steps and Main Functions Used

### 1. **Importing Libraries**

```python
import matplotlib.pyplot as plt
import numpy as np
```

* **`numpy`**: Used to generate numeric arrays and mathematical functions.
* **`matplotlib.pyplot`**: Provides plotting functions with an **object-oriented interface** for better customization.

---

### 2. **Generating Data**

```python
x = np.linspace(0,2*np.pi,100)
y1 = np.sin(x)
y2 = np.cos(x)
```

* **`np.linspace(0, 2*np.pi, 100)`**: Creates 100 evenly spaced values between 0 and $2\pi$.
* **`np.sin(x)`** and **`np.cos(x)`**: Compute sine and cosine values for the generated points.

---

### 3. **Creating Figure and Axes**

```python
fig, ax = plt.subplots()
```

* **`plt.subplots()`**: Creates a `Figure` (`fig`) and a single subplot `Axes` (`ax`).
* Using the **OO API** (`ax`) provides more control compared to the state-based approach.

---

### 4. **Plotting Functions**

```python
ax.plot(x, y1, 'g--', label='sin(x)')
ax.plot(x, y2, 'r-.', label='cos(x)')
```

* **`ax.plot()`**: Plots data on the given axes.
* `g--`: Green dashed line for sine.
* `r-.`: Red dash-dot line for cosine.
* **`label`**: Adds names for the legend.

---

### 5. **Adding Legend and Grid**

```python
ax.legend(loc='upper center')
ax.grid(True, linestyle=':')
```

* **`ax.legend()`**: Displays a legend at the **upper center** of the plot.
* **`ax.grid()`**: Adds grid lines with a dotted (`:`) style.

---

### 6. **Customizing Labels and Title**

```python
ax.set_title("Custom Complex Plot (OO API)", fontsize=14)
ax.set_xlabel('X-Axis')
ax.set_ylabel('Y-Axis')
```

* **`ax.set_title()`**: Adds a descriptive title.
* **`ax.set_xlabel()`** and **`ax.set_ylabel()`**: Add axis labels.
* Font size customization improves readability.

---

## 📊 Output

* **Green dashed curve**: `sin(x)`
* **Red dash-dot curve**: `cos(x)`
* Includes **legend**, **grid lines**, **labels**, and a **title** for clarity.

---

## 🚀 Key Learnings

* Matplotlib’s **Object-Oriented API** (`fig, ax = plt.subplots()`) gives more flexibility than the state-based API.
* Customizing line styles, legends, grids, and titles enhances readability.
* Combining multiple functions in one plot helps in direct comparison.