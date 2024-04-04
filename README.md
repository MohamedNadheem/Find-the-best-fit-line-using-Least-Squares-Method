# EX-01 Implementation of Univariate Linear Regression
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

Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: MOHAMED NADHEEM N
RegisterNumber: 212223240091

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
print("X_values")
X=np.array(eval(input()))
print("Y_values")
Y=np.array(eval(input()))
X_mean=np.mean(X)
print("X_MEAN VALUE")
print(X_mean)
Y_mean=np.mean(Y)
print("Y_MEAN VALUE")
print(Y_mean)
num=0
den=0
for i in range (len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    den+=(X[i]-X_mean)**2
print("INTERCEPT")    
m=num/den
b=Y_mean-m*X_mean
print(b)
Y_pred=m*X+b
print("Y_PREDICTED")
print(Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='yellow')
plt.title("UNIVARIATE LINEAR REGRESSION")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.show()

```

## Output:
![O1](https://github.com/BALA291/Find-the-best-fit-line-using-Least-Squares-Method/assets/120717501/5f49f5a8-4647-4431-a274-10059b94cecd)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
