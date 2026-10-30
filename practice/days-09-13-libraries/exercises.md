# Practice: Python libraries, Days 9 to 13

Data for the Pandas, Matplotlib and Seaborn days is in `data/`. There are two files:

- `students.csv`: 20 students with department, year, gender, marks in three subjects, attendance and city. Some marks are missing on purpose.
- `departments.csv`: the head of department and block for each department.

Install the libraries with `pip install -r requirements.txt` or use Colab, where they are already installed. Work in a notebook for these days. Save as `my-progress/day09.ipynb` and so on.

---

## Day 9: NumPy

```python
import numpy as np
```

1. Create these arrays and print each with its `shape` and `dtype`: from the list `[1, 2, 3, 4]`, `np.zeros((3, 4))`, `np.ones((2, 2))`, `np.arange(0, 20, 3)`, and `np.linspace(0, 1, 5)`.
2. Create `np.arange(12)` and reshape it to 3 by 4, then to 2 by 6, then to 4 by 3. Use `-1` in one reshape and explain what it does.
3. For `a = np.arange(1, 13).reshape(3, 4)`:
   - Print the second row, the last column, and the 2 by 2 block in the top-right corner.
   - Print every element greater than 6 using a boolean mask.
   - Set every even element to 0 using a mask.
4. Compute the sum, mean and maximum of `a`, then along `axis=0` and along `axis=1`. Write down which axis gives one value per column.
5. Broadcasting. Create `m = np.ones((3, 4))`, a row vector `r = np.array([1, 2, 3, 4])` and a column vector `c = np.array([[10], [20], [30]])`. Compute `m + r` and `m + c`. Predict the shapes before you run it.
6. Vectorization. Make an array of 1,000,000 random numbers. Compute the sum of the squares using a Python `for` loop, then using NumPy. Time both with `%timeit` or `time.time()`. Write down how many times faster NumPy is.
7. Set a seed with `np.random.seed(42)` and generate 5 random integers between 0 and 100. Run it twice and confirm you get the same values.
8. Linear algebra. For `A = np.array([[2, 1], [1, 3]])` and `b = np.array([1, 2])`:
   - Compute `A @ A`, `A.T` and `np.linalg.inv(A)`.
   - Check that `A @ np.linalg.inv(A)` is close to the identity matrix.
   - Solve `A x = b` with `np.linalg.solve`. Check the answer by multiplying back.
   - Find the eigenvalues with `np.linalg.eig`.
9. Without a loop, normalize each column of a random 5 by 3 array so that every column has mean 0 and standard deviation 1.

Check: why does `a[a > 6]` return a flat array even if `a` is 2D?

---

## Day 10: Pandas I, loading, inspecting, selecting

```python
import pandas as pd
df = pd.read_csv("data/students.csv")
```

1. Print `df.head()`, `df.tail(3)`, `df.shape`, `df.columns`, `df.dtypes`.
2. Run `df.info()` and `df.describe()`. The shape should be `(20, 10)`. Which columns show fewer than 20 non-null values?
3. Select the `name` column. Select `name` and `math` together. Note the type each returns.
4. Use `loc` to get the row with `id` 5 (after setting `id` as the index, or by filtering). Use `iloc` to get the first 3 rows and the first 4 columns.
5. Filter and print:
   - Students in the CSE department
   - Students in year 3 or 4
   - Students with math above 80 and attendance above 90
   - Students whose city is Warangal or Hyderabad (use `isin`)
6. Sort by `math` descending. Print the top 5 names and marks.
7. Create a new column `total` = math + physics + programming. Notice what happens to rows where a mark is missing.
8. Use `value_counts()` on `department`, `city` and `gender`. Which city has the most students?
9. Create a column `result` that is `"pass"` if `math` is 50 or above, otherwise `"fail"`. Use `np.where`.

Check: what is the difference between `df["math"]` and `df[["math"]]`?

---

## Day 11: Pandas II, missing data, groupby, merge

1. Count missing values per column using `df.isna().sum()`. You should see 3 missing in `physics` and 2 in `programming`.
2. Make three copies of the DataFrame and handle the missing values in three ways: drop rows with any missing value, fill with the column mean, fill with the column median. Compare the mean of `physics` in all three. Write two lines on which you would choose and why.
3. Group by `department` and compute the mean of `math`, `physics` and `programming`. Which department has the highest mean programming mark?
4. Use `agg` to get, per department, the count of students, the mean attendance, and the maximum math mark in one table.
5. Group by `department` and `gender` together. Show the average total marks.
6. Use `pivot_table` to show mean `math` with `department` as rows and `year` as columns. Explain the NaN cells.
7. Read `departments.csv` and merge it into the student table on `department`. Check that you still have 20 rows. Try an inner merge and a left merge and explain when they would differ.
8. Use `apply` or `map` to add a column that is `"high"` when attendance is 90 or above, `"medium"` between 75 and 89, and `"low"` otherwise. Count each.
9. Use string methods: make `name` upper case, find names that start with a vowel, and find names with more than 6 characters.
10. Save the cleaned and merged table to `students_clean.csv` with `index=False`. Reload it and confirm it matches.

Check: after `fillna(df["math"].mean())`, was the original `df` changed? Why or why not?

---

## Day 12: Matplotlib

```python
import matplotlib.pyplot as plt
```

1. Plot `y = x^2` for x from -5 to 5 as a line. Add a title, axis labels and a grid.
2. On the same axes, plot `y = x^2` and `y = 2x + 3`. Add a legend and different line styles.
3. Make a bar chart of the average math mark per department. Sort the bars from highest to lowest. Label the axes.
4. Make a horizontal bar chart of the number of students per city.
5. Make a scatter plot of `math` against `physics`. Color the points by department. Add a legend.
6. Make a histogram of `attendance` with 5 bins, then with 10 bins. Say what each tells you.
7. Make a figure with 2 rows and 2 columns of subplots containing a line, a bar, a scatter and a histogram. Give each a title and call `plt.tight_layout()`.
8. Change the figure size, font size and colors of one chart. Save it as `chart.png` with `dpi=200`.
9. Make a pie chart of students per department. Then write one sentence on why a bar chart would usually be a better choice.

Check: what is the difference between `plt.plot(...)` and `fig, ax = plt.subplots()` followed by `ax.plot(...)`? Which one scales better to complex figures?

---

## Day 13: Seaborn

```python
import seaborn as sns
sns.set_theme()
```

1. Draw a `histplot` of `programming` with `kde=True`.
2. Draw a `boxplot` of `math` by `department`. Which department has the widest spread? Are there outliers?
3. Draw a `countplot` of `department` split by `gender` using `hue`.
4. Draw a `scatterplot` of `math` against `programming` with `hue="department"` and `style="gender"`.
5. Draw a `violinplot` of `attendance` by `year`.
6. Compute the correlation matrix of the numeric columns with `df.corr(numeric_only=True)` and draw it as a `heatmap` with `annot=True`. Which two columns correlate most strongly?
7. Draw a `pairplot` of `math`, `physics`, `programming` and `attendance`, colored by `gender`.
8. Draw a `barplot` of mean `total` marks by `city`. What do the error bars show?
9. Pick any three of your charts and write two sentences under each that explain what a reader should notice.

Check: which of these questions can a boxplot answer that a histogram of the same data answers less clearly?

---

## End of block

By the end of Day 13 you should be able to:

- Load a CSV, inspect it, clean missing values, and group and summarize it.
- Draw a bar chart, a scatter plot, a histogram and a heatmap, and explain what each shows.
- Write a short function and a small class.

Day 14 is Project 1: choose a Kaggle dataset and put all of this together in one exploratory analysis notebook. If any bullet above feels shaky, use the Day 14 time to go back to that topic first.
