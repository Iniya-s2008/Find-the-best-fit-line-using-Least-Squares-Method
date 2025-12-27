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

 Program:
```
<img width="958" height="693" alt="image" src="https://github.com/user-attachments/assets/6b55087f-e781-42a3-a10c-43bd00efa072" />
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
xmean=np.mean(x)
ymean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    denom+=(x[i]-xmean)**2
m=num/denom
c=ymean-m*xmean
print("slope",m)
print("Y-intercept",c)
ypred=m*x+c
print("Predicted values",ypred)
plt.scatter(x,y)
plt.plot(x,ypred)
plt.show()

Output:
<img width="947" height="665" alt="image" src="https://github.com/user-attachments/assets/e7dcb13c-65b8-4bb4-afa1-b5c29c09159f" />

<img width="1068" height="742" alt="image" src="https://github.com/user-attachments/assets/691e87d1-8e68-4142-aef0-ad1999bcd975" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
