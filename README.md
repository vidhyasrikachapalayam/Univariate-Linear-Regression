# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eq1](https://user-images.githubusercontent.com/119477817/215306388-2b84c96e-56db-4eb4-a3e9-c03904b3ee3c.jpg)

4.	Compute the y -intercept of the line by using the formula:
![eq2](https://user-images.githubusercontent.com/119477817/215306408-a26d3a0b-2457-47dd-9c1b-b2f6b227bd11.jpg)

5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
Developed by: vidhyasri.k

RegisterNumber: 22008468

import numpy as np

import matplotlib.pyplot as plt

X=np.array(eval(input()))

Y=np.array(eval(input()))

Xmean=np.mean(X)

Ymean=np.mean(Y)

num,den=0,0

for i in range(len(X)):

     num+=(X[i]-Xmean)*(Y[i]-Ymean)

     den+=(X[i]-Xmean)**2

m=num/den

c=Ymean-m*Xmean

print(m,c)

Y_pred=m*X+c

print(Y_pred)

plt.scatter(X,Y)

plt.plot(X,Y_pred,color="purple")

plt.show()







## Output:
![univariate](https://user-images.githubusercontent.com/119477817/215306070-6a78ef92-81fb-4bd6-9eae-2dc6aa49eba9.png)



## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
