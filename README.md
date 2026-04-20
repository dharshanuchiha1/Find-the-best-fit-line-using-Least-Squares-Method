# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Dharshan G
RegisterNumber:  212225230054
*/
import numpy as np
import matplotlib.pyplot as plt

A = np.array([1, 2, 3, 4, 5])
B = np.array([2, 4, 5, 4, 5])

a_mean = np.mean(A)
b_mean = np.mean(B)

numerator = np.sum((A - a_mean) * (B - b_mean))
denominator = np.sum((A - a_mean) ** 2)

m = numerator/denominator
c = b_mean - m *a_mean

print("Slope (m):", m)
print("Intercept (b):", c)

B_pred = m * A + c
a = input("Enter value: ")
bb = m * float(a) + c
print("Value:", bb)
plt.scatter(A, B, label="Data Points")
plt.plot(A, B_pred, label="Best Fit Line")
plt.xlabel("A")
plt.ylabel("B")
plt.legend()
plt.title("Univariate Linear Regression")
plt.show()
```

## Output:
![best fit line](sam.png)
<img width="790" height="609" alt="Screenshot 2026-04-20 203154" src="https://github.com/user-attachments/assets/083f9cb5-d732-40f1-a275-2cc58b6c6252" />
<img width="719" height="601" alt="Screenshot 2026-04-20 203236" src="https://github.com/user-attachments/assets/2b8cfbc9-94bc-4077-a5f8-f74c6a91b8f4" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
