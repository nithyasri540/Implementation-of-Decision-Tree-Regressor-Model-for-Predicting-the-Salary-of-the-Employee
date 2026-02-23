# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the dataset using pandas, select the independent variable (Position Level) as X and dependent variable (Salary) as y.
2.Initialize the DecisionTreeRegressor model with a random state for consistent results. 
3. Fit the model using regressor.fit(X, y) so that the decision tree learns patterns from the training data.
4. Predict salary for a given input (e.g., 6.5) using predict() and plot the regression results to visualize how the decision tree fits the data.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.NITHYASRI
RegisterNumber:  25018590
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.tree import DecisionTreeRegressor
dataset = pd.read_csv("C:/Users/acer/Downloads/Salary.csv")
X = dataset.iloc[:, 1:2].values
y = dataset.iloc[:, 2].values
regressor = DecisionTreeRegressor(random_state=0)
regressor.fit(X, y)
salary_pred = regressor.predict([[6.5]])
print("Predicted Salary:", salary_pred)
X_grid = np.arange(min(X), max(X), 0.01)
X_grid = X_grid.reshape((len(X_grid), 1))

plt.scatter(X, y, color='red')
plt.plot(X_grid, regressor.predict(X_grid), color='blue')
plt.title('Decision Tree Regression')
plt.xlabel('Position Level')
plt.ylabel('Salary')
plt.show()

*/
```

## Output:
<img width="743" height="555" alt="image" src="https://github.com/user-attachments/assets/aa251a4a-9a80-4847-8df4-8a93b6298d01" />



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
