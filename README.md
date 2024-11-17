# Ex No: 1.Implementation of Univariate Linear Regression

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
Developed by: GANESH D
RegisterNumber:  212223240035
*/

import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(x)
ymean=np.mean(y)
n=0
d=0
for i in range(len(x)):
  n+=(x[i]-xmean)*(y[i]-ymean)
  d+=(x[i]-xmean)**2
m=n/d
c=ymean-m*xmean
print(m,c)
ypred=m*x+c
print(ypred)
plt.scatter(x,y)
plt.plot(x,ypred,color='red')
plt.show()
```


## Output:
<img width="780" alt="univariate regression" src="https://github.com/user-attachments/assets/dee5f7a8-3d29-4daf-a79f-00415f095146">




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
