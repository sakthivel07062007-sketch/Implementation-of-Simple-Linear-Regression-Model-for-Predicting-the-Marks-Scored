# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import required libraries and load the dataset from the CSV file.
2. Separate the dataset into independent variable (Experience) and dependent variable (Salary).
3. Create the Linear Regression model and train it using the given data.
4. Predict the salary values, display slope and intercept, and plot the regression line with the data points. 


## Program:
```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
Y = np.array([35, 50, 65, 70, 85])
model = LinearRegression()
model.fit(X, Y)
m = model.coef_[0]
b = model.intercept_
print("Slope (m):", m)
print("Intercept (b):", b)
x_input = float(input("Enter hours studied: "))
predicted_marks = model.predict([[x_input]])
print("Predicted Marks:", predicted_marks[0])
Y_pred = model.predict(X)
plt.scatter(X, Y, label="Actual Data")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression (Using sklearn)")
plt.legend()
plt.show()
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: SAKTHIVEL K
RegisterNumber:  212225240133
*/
```

## Output:

<img width="789" height="670" alt="image" src="https://github.com/user-attachments/assets/73b88b93-77e9-4a81-9732-f77d5594e457" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
