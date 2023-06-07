# Correlation and regression for data analysis
# Aim : 

To analyse given data using coeffificient of correlation and regression line
![image](https://user-images.githubusercontent.com/104613195/168224136-d6b64e64-7d3d-4775-9337-c8f96fe41f2d.png)


# Software required :  

Python

# Theory:

Correlation describes the strength of an association between two variables, and is completely symmetrical, the correlation between A and B is the same as the correlation between B and A. However, if the two variables are related it means that when one changes by a certain amount the other changes on an average by a certain amount.  

If y represents the dependent variable and x the independent variable, this relationship is described as the regression of y on x. The relationship can be represented by a simple equation called the regression equation. The regression equation representing how much y changes with any given change of x can be used to construct a regression line on a scatter diagram, and in the simplest case this is assumed to be a straight line.

# Procedure :

![image](https://user-images.githubusercontent.com/104613195/168225866-ac8f6610-bdc3-4ac2-a24e-2b24ba08e189.png)

# Program :

![image](https://github.com/ramjan1729/Correlation_Regression/assets/103921593/9eb48cbf-8ca3-4cd9-8440-ff45fd98333e)
```python
import numpy as np
import math
import matplotlib.pyplot as plt 
x=[int(i) for i in input().split()]
y=[int(i) for i in input().split()]
N=len(x)
```
```python
sx=0
sy=0
sxy=0
sx2=0
sy2=0
for i in range(0,N):
    sx=sx+x[i]
    sy=sy+y[i]
    sxy=sxy+x[i]*y[i]
    sx2=sx2+x[i]**2
    sy2=sy2+y[i]**2
r=(N*sxy-sx*sy)/(math.sqrt(N*sx2-sx**2)*math.sqrt(N*sy2-sy**2))
print("The correlation cofficient of %0.3f"%r)
```
```python
byx=(N*sxy-sx*sy)/(N*sx2-sx**2)
xmean=sx/N
ymean=sy/N
print("The Regression line Y on X is ::: %0.3f + %0.3f (x-%0.3f)"%(ymean,byx,xmean))
plt.scatter(x,y)
def reg(x):
    return ymean+byx*(x-xmean)
x=np.linspace(0,80,51)
y1=reg(x)
plt.plot(x,y1,'r')
plt.xlabel('x-data')
plt.ylabel('y-data')
plt.legend(['Regression Line','Data points'])
```

# Output 

## input x and y array
![image](https://github.com/EASWAR17/Correlation_Regression/assets/94154683/593610b2-870a-44e0-9b14-f837ef72b8c4)

## correlation coefficient
![image](https://github.com/EASWAR17/Correlation_Regression/assets/94154683/32b53d9b-87d8-4656-9244-ff6a113c118e)

## regression lines and graph
![image](https://github.com/EASWAR17/Correlation_Regression/assets/94154683/fd321895-dede-4411-a559-13e3e46bf553)

# Result
The Correlation and regression for data analysis of objects from feeder using probability distribution are calculated
