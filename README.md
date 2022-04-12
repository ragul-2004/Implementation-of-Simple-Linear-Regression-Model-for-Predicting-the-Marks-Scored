# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to implement the linear regression using gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. To implement the linear regression using the standard libraries in the python.

2. Use the .isnull() function to check the empty.

3. Use the default function.

4. Open the head() function.

5. Use the loop function for a linear equation.

6. Predict the value for the y.

7. Print the program.

8. Plot the graph by using scatters keyword.

9. End the program.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: Ragul.A.C
RegisterNumber:  212221240042
*/

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("student_scores.csv")
data.head()
data.isnull().sum()
x=data.Hours
x.head()
y=data.Scores
y.head()
n=len(x)
m=0
c=0
l=0.001
loss=[]
for i in range(10000):
    ypred=m*x+c
    mse=(1/n)*sum((ypred-y)*2)
    dm=(2/n)*sum(x*(ypred-y))
    dc=(2/n)*sum(ypred-y)
    c=c-l*dc
    m=m-l*dm
    loss.append(mse)
print(m,c)


y_pred=m*x+c
plt.scatter(x,y,color="blue")
plt.plot(x,y_pred)
plt.xlabel("study hours")
plt.ylabel("scores")
plt.title("Study hours vs scores")

plt.plot(loss)
plt.xlabel("iterations")
plt.ylabel("loss")

```


## Output:
![linear regression using gradient descent](o1.png)
![linear regression using gradient descent](o2.png)

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
