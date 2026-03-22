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
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import matplotlib.pyplot as plt
x=list(map(int,input("Enter the x values:").split()))
y=list(map(int,input("Enter the y values:").split()))
print(x,y)
L=len(x)
xmean=sum(x)/L
ymean=sum(y)/L
nr=sum([(x[i]-xmean)*(y[i]-ymean) for i in range(L)])
dr=sum([(x[i]-xmean)**2 for i in range(L)])
m=nr/dr
b=ymean-(m*xmean)
ypred=[(m*x[i])+b for i in range(L)]
print(m,b)
print(ypred)
plt.scatter(x,ypred)
plt.plot(x,y,color="red")
plt.show()

```
## Output
![alt text](<Screenshot 2026-03-22 173321.png>)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
