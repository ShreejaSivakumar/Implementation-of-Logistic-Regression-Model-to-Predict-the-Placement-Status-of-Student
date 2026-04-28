# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

# DATE : 28/04/26

# NAME : SHREEJA R S
# REF.NO : 25017561

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook


## Algorithm

1. Load `Placement_Data.csv`, drop `salary` column and convert categorical columns to numeric using dummy encoding
2. Separate features `X` and target `y` then split into 80% train and 20% test
3. Train `LogisticRegression` model and print accuracy score on test data
4. Select first feature column and train a second model for visualization
5. Plot actual data as scatter and draw sigmoid probability curve over it
6. Add labels, title, legend and display the logistic regression plot


## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: SHREEJA R S
RegisterNumber:  25017561
*/

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Load dataset
data = pd.read_csv("Placement_Data.csv")

# Drop salary column (contains missing values)
data = data.drop("salary", axis=1)

# Convert categorical data to numeric
data = pd.get_dummies(data, drop_first=True)

# Features and target
X = data.drop("status_Placed", axis=1)
y = data["status_Placed"]

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42)

# Train model
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

# Accuracy
print("Accuracy:", model.score(X_test, y_test))

# ── Logistic Regression Plot ──────────────────────────────
# Use only ONE feature for plotting
X1 = X.iloc[:, 0].values.reshape(-1, 1)

# Train model on single feature
model_plot = LogisticRegression(max_iter=1000)
model_plot.fit(X1, y)

# Scatter plot
plt.scatter(X1, y, color='blue', label='Actual')

# Sigmoid curve
x_values = np.linspace(X1.min(), X1.max(), 100).reshape(-1, 1)
y_values  = model_plot.predict_proba(x_values)[:, 1]

plt.plot(x_values, y_values, color='red', label='Sigmoid Curve')
plt.xlabel("Feature")
plt.ylabel("Probability")
plt.title("Logistic Regression Curve")
plt.legend()
plt.tight_layout()
plt.show()



```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)
<img width="926" height="643" alt="Screenshot 2026-04-28 234745" src="https://github.com/user-attachments/assets/f92fad8a-9634-47e3-b271-6e3f9f306a4d" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.























































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.






















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.





















































































































.
.
.
.
.
.
.
.
.
.
.
.
.

.
..
.

.

.
.
.
.

.

.
.
.
.
..
