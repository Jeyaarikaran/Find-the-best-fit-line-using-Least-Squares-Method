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
```import numpy as np
import matplotlib.pyplot as plt
# getting input from the user
X = np.array(eval(input()))
Y = np.array(eval(input()))
# Mean
X_Mean = np.mean(X)
Y_Mean = np.mean(Y)
num = 0 #for slope
dem = 0 #for slope
for i in range(len(X)):
  num += (X[i] - X_Mean) * (Y[i] - Y_Mean)
  dem += (X[i] - X_Mean) ** 2
#slope 
mean = num/dem
# Y intercept
b = Y_Mean - mean * X_Mean
print(f"Slope,b: {s}")
print(f"Y_Intercept,b: {b}")
#line equation
Y_predict = mean*X+b
print(Y_predict)

#to plot graph
plt.scatter(X,Y)
plt.plot(X,Y_predict,color='red')
plt.show()
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by:JEYAARIKARAN P 
RegisterNumber:212224240064  
*/
```

## Output:
![image](https://github.com/user-attachments/assets/2ad3b558-c772-4e15-829e-b4eba560d5df)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
