# task12-NumPy-Aggregations-and-Statistics

## Overview
This project demonstrates NumPy aggregation and statistical functions using a numerical student-score dataset. It calculates sum, mean, median, minimum, maximum, standard deviation, and variance.

## Objective
Build basic numerical analysis skills using NumPy and interpret statistical results.

## Tools Used
- Python
- NumPy
- Pandas
- Jupyter Notebook or Google Colab

## Dataset
This example uses sample student scores in Mathematics, Science, and English. You can replace this sample with the Student Performance Dataset or Iris Dataset suggested in the task.

## Code

```python
import numpy as np
import pandas as pd

data = {
    "Student": ["Asha", "Ravi", "Meena", "Arjun", "Priya"],
    "Math": [85, 78, 92, 69, 88],
    "Science": [90, 82, 89, 75, 94],
    "English": [80, 85, 87, 72, 91]
}

df = pd.DataFrame(data)
print("Student Dataset:")
print(df)

scores = df[["Math", "Science", "English"]].to_numpy()

# Overall statistics
print("\nSum:", np.sum(scores))
print("Mean:", np.mean(scores))
print("Median:", np.median(scores))
print("Minimum:", np.min(scores))
print("Maximum:", np.max(scores))
print("Standard deviation:", np.std(scores))
print("Variance:", np.var(scores))

# Subject-wise statistics: axis=0 (columns)
print("\nSubject-wise sum:", np.sum(scores, axis=0))
print("Subject-wise mean:", np.mean(scores, axis=0))
print("Subject-wise median:", np.median(scores, axis=0))
print("Subject-wise minimum:", np.min(scores, axis=0))
print("Subject-wise maximum:", np.max(scores, axis=0))
print("Subject-wise standard deviation:", np.std(scores, axis=0))
print("Subject-wise variance:", np.var(scores, axis=0))

# Student-wise statistics: axis=1 (rows)
print("\nStudent-wise mean:", np.mean(scores, axis=1))
print("Student-wise sum:", np.sum(scores, axis=1))
```

## NumPy Functions Demonstrated
1. `np.sum()` — adds values.
2. `np.mean()` — calculates the average.
3. `np.median()` — finds the middle value.
4. `np.min()` — finds the smallest value.
5. `np.max()` — finds the largest value.
6. `np.std()` — calculates standard deviation.
7. `np.var()` — calculates variance.

## Understanding `axis`
- `axis=0`: calculates a result for each column/subject.
- `axis=1`: calculates a result for each row/student.
- No `axis`: calculates a result across all numerical values.

## Steps to Run
1. Open Google Colab or Jupyter Notebook.
2. Create a new notebook.
3. Copy the code into a cell.
4. Run the cell and review the results.
5. If required, replace the sample scores with your chosen dataset.

## Result Interpretation
The code calculates overall statistics, subject-wise statistics, and student-wise totals and averages. Compare the subject-wise means to identify the subject with the highest average. Standard deviation and variance indicate how spread out the scores are: lower values generally mean more consistent scores.

## Repository Structure

```text
numpy-aggregations-statistics/
├── README.md
└── numpy_aggregations_statistics.ipynb
```

## Conclusion
This task demonstrates how NumPy can be used for basic statistical analysis and how the `axis` parameter changes calculations across rows and columns.
