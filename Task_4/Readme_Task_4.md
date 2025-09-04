# Task 4 – Multiple Y-Axes Sharing a Common X-Axis

This task demonstrates how to plot **two different functions with separate Y-axes but a shared X-axis** using Matplotlib. This approach is useful when comparing variables with different scales.

---

## 📌 Steps and Main Functions Used

### 1. **Importing Required Libraries**

```python
import matplotlib.pyplot as plt
import numpy as np
```

* **`numpy`**: For generating numeric data (arrays, ranges, functions).
* **`matplotlib.pyplot`**: For plotting graphs and customizing visualizations.

---

### 2. **Generating Data**

```python
x = np.arange(0,10,0.1)
y1 = np.sin(x)
y2 = np.exp(0.1*x)
```

* **`np.arange(0,10,0.1)`**: Creates an array of values from 0 to 10 with step size 0.1.
* **`np.sin(x)`**: Computes sine values for array `x`.
* **`np.exp(0.1*x)`**: Computes exponential growth for `x`.

---

### 3. **Creating Multiple Y-Axes**

```python
fig, ax1 = plt.subplots()
ax2 = ax1.twinx()
```

* **`plt.subplots()`**: Creates a figure (`fig`) and a primary axis (`ax1`).
* **`twinx()`**: Creates a second Y-axis (`ax2`) sharing the same X-axis.
* This allows plotting two datasets with different scales.

---

### 4. **Plotting Functions**

```python
ax1.plot(x, y1, 'g-', label='sin(x)')
ax2.plot(x, y2, 'b^', label='exp(0.1x)')
```

* **`ax1.plot()`**: Plots sine function (`y1`) in green line.
* **`ax2.plot()`**: Plots exponential function (`y2`) in blue triangle markers.
* Labels are added for clarity.

---

### 5. **Customizing Axes and Labels**

```python
ax1.set_xlabel('Values')
ax1.set_ylabel('Sin(x)', color='g')
ax2.set_ylabel('Exp(0.1x)', color='b')
```

* Sets axis labels and assigns colors to match the plotted curves.
* Helps distinguish between the two functions.

---

### 6. **Final Touches**

```python
plt.title("Multiple Y Axis with a common X Axis")
plt.show()
```

* Adds a **title** to the plot.
* **`plt.show()`** displays the final graph.

---

## 📊 Output

* The **green curve** shows the sine function (`sin(x)`).
* The **blue curve** shows the exponential function (`exp(0.1x)`).
* Both functions are plotted against the same `x` values, but each has its own **Y-axis** for clarity.

---

## 🚀 Key Learnings

* `twinx()` allows plotting **two Y-axes with a shared X-axis**.
* Useful when comparing datasets with **different scales**.
* Combining trigonometric and exponential functions provides clear contrast in behavior.