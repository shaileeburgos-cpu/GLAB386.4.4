📘 GLAB — Python Data & Visualization Practice
Clear explanations • Runnable examples • Beginner‑friendly notes

🧠 Overview
This lab introduces essential Python tools used in data analytics:

NumPy → fast numerical calculations

Pandas → data cleaning & manipulation

Matplotlib → data visualization

Jupyter Kernel → lets you run code in notebooks

These examples are simple, clean, and designed to help you understand why the code works — not just memorize it.

📦 Installation (Terminal Command)
Run this in your terminal (inside your virtual environment):

bash
python3 -m pip install pandas numpy matplotlib jupyterlab notebook ipykernel
📁 Project Structure
Code
GLAB-XXXX/
│── README.md
│── main.py
└── data/
    └── sample.csv
🧩 1. NumPy Basics
NumPy is used for fast math, arrays, and scientific computing.

✔️ Create an array & do math
python
import numpy as np

arr = np.array([10, 20, 30, 40])
print("Array:", arr)
print("Add 5:", arr + 5)
print("Mean:", arr.mean())
📝 What’s happening?
np.array() creates a fast numeric array

You can add numbers to the whole array at once

.mean() calculates the average

🧩 2. Pandas Basics
Pandas is used for data cleaning, filtering, and analysis.

✔️ Create a DataFrame
python
import pandas as pd

data = {
    "Name": ["Ana", "Ben", "Chris"],
    "Age": [23, 29, 31],
    "City": ["Atlanta", "Miami", "Dallas"]
}

df = pd.DataFrame(data)
print(df)
✔️ Filter rows
python
adults = df[df["Age"] > 25]
print(adults)
📝 What’s happening?
Pandas stores data in a table (DataFrame)

You can filter rows using conditions like df[df["Age"] > 25]

📊 3. Matplotlib Basics
Matplotlib is used to create charts and visualizations.

✔️ Simple Line Plot
python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [10, 20, 15, 30]

plt.plot(x, y, marker='o')
plt.title("Simple Line Chart")
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.show()
✔️ Bar Chart Example
python
plt.bar(["A", "B", "C"], [5, 7, 3])
plt.title("Bar Chart Example")
plt.show()
📝 What’s happening?
plt.plot() draws a line

plt.bar() draws bars

plt.show() displays the chart

🧪 4. Combining Pandas + Matplotlib
This is where data analytics becomes powerful.

✔️ Plot a column from a DataFrame
python
df = pd.DataFrame({
    "Month": ["Jan", "Feb", "Mar", "Apr"],
    "Sales": [1200, 1500, 1800, 1700]
})

plt.plot(df["Month"], df["Sales"], marker="o")
plt.title("Monthly Sales")
plt.xlabel("Month")
plt.ylabel("Sales ($)")
plt.show()
📝 Why this matters:
You’ll use this pattern in every real analytics job — load data → clean it → visualize it.

🧠 5. Easy Interpretation (What You Should Remember)
✔️ NumPy
Works with numbers

Fast math

Arrays, means, sums

✔️ Pandas
Works with tables

Filtering, sorting, cleaning

.DataFrame() is your best friend

✔️ Matplotlib
Makes charts

Line, bar, scatter, histograms

✔️ Kernel
Lets Jupyter run your Python environment

🚀 6. How to Run the Code
Option A — Run in Terminal
bash
python3 main.py
Option B — Run in Jupyter Notebook
bash
jupyter lab