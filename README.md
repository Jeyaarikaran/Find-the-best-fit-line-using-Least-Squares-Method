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
Developed by:JEYAARIKARAN P 
RegisterNumber:212224240064  
*/


import numpy as np
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

```

## Output:
##  X  and Y Value
![image](https://github.com/user-attachments/assets/a9415d17-78f2-4c56-98fa-6354da040e58)
 ## Slope
 ![image](https://github.com/user-attachments/assets/a43f285c-0376-48c9-9186-388ddad146f9)
## y_intercept
![image](https://github.com/user-attachments/assets/03e0d17b-c3c0-4117-b3b3-4b2937b37c26)
## y_predicted
![image](https://github.com/user-attachments/assets/9a6cfb2b-28bb-4e42-a7df-e6982b789b9e)
## Graph
![image](https://github.com/user-attachments/assets/c1ef2916-74b1-4010-81aa-fa2614c67a92)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
