# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Create a dataset containing employee experience and salary details.
2.Separate the input feature (X) and target salary (y).
3.Split the dataset into training and testing sets.
4.Create and train a Decision Tree Regressor using the training data.
5.Predict the employee salary and calculate the model's accuracy using R² score.

## Program:
```python

# Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
# Developed by: Vigneshwar M
# Register Number:  212225060298


import pandas as pd
from sklearn.tree import DecisionTreeRegressor
from sklearn.metrics import r2_score

# Load CSV file
data = pd.read_csv("Salary.csv")

# Select input and output
X = data[["Level"]]
y = data["Salary"]

# Create Decision Tree Regressor
model = DecisionTreeRegressor(random_state=42)

# Train the model
model.fit(X, y)

# Predict salary for all employees
y_pred = model.predict(X)

# Display actual and predicted salaries
print("Actual Salary:")
print(y.values)

print("\nPredicted Salary:")
print(y_pred)

# Calculate R2 score
print("\nR2 Score:", r2_score(y, y_pred))

# Predict salary for a new employee
level = [[6]]
predicted_salary = model.predict(level)

print("\nPredicted Salary for Level 6:", predicted_salary[0])

```

## Output:

<img width="1772" height="424" alt="image" src="https://github.com/user-attachments/assets/b1e50053-19ec-4551-ba1b-ad5ea5b95850" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
