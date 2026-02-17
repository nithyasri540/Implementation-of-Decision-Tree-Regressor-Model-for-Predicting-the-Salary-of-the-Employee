# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries. 
2. Upload the dataset and check for any null values using .isnull() function.
3. Import LabelEncoder and encode the dataset. 
4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:S.NITHYASRI 
RegisterNumber:  25018590
import pandas as pd
import numpy as np
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import matplotlib.pyplot as plt
df = pd.read_csv("C:/Users/acer/Downloads/Salary.csv")
print("Dataset Preview:")
print(df.head())
X = df[["Level"]]   
y = df["Salary"]             
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.3, random_state=42
)
model = DecisionTreeRegressor(
    criterion="squared_error",
    max_depth=3,
    random_state=42
)
model.fit(X_train, y_train)
y_pred = model.predict(X_test)
mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
print("MAE  :", mean_absolute_error(y_test, y_pred))
print("MSE  :", mse)
print("RMSE :", rmse)
print("R2   :", r2_score(y_test, y_pred))
plt.figure(figsize=(16, 10))
plot_tree(
    model,
    feature_names=["Level"],
    filled=True
)
plt.title("Decision Tree Regressor for Employee Salary Prediction")
plt.show()
new_exp = [[5]] 
predicted_salary = model.predict(new_exp)
print("\nPredicted Salary for 5 years experience:", predicted_salary[0])
*/
```

## Output:
<img width="374" height="238" alt="Screenshot 2026-02-17 132559" src="https://github.com/user-attachments/assets/1a5dc182-96da-4228-a784-9f51808d298e" />
<img width="1145" height="775" alt="Screenshot 2026-02-17 133003" src="https://github.com/user-attachments/assets/57516202-15d6-46f9-afcb-f534335792cd" />




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
