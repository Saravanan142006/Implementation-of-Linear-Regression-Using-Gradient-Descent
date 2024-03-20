# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: Saravanan M
RegisterNumber: 212223080050
import pandas as pd
import numpy as np
from sklearn.preprocessing import StandardScaler

def linear_regression(X1, y, learning_rate=0.01, num_iters=1000):
    X=np.c_[np.ones(len(X1)),X1]

    theta=np.zeros(X.shape[1]).reshape(-1,1)

    for _ in range(num_iters):
        predictions = (X).dot(theta).reshape(-1,1)

        errors =(predictions - y).reshape(-1,1)

        theta=theta-learning_rate*(1/len(X1))*X.T.dot(errors)

    return(theta)

data=pd.read_csv('50_startups.csv',header=None)

X=(data.iloc[1:,:-2].values)
X1=X.astype(float)
scalar=StandardScaler()
y=(data.iloc[1:,-1].values).reshape(-1,1)
X1_Scaled =scalar.fit_transform(X1)
Y1_Scaled =scalar.fit_transform(y)

theta=linear_regression(X1_Scaled, Y1_Scaled)

new_data=np.array([165349.2,136897.58,471784.1]).reshape(-1,1)
new_Scaled =scalar.fit_transform(new_data)
prediction=np.dot(np.append(1,new_Scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scalar.inverse_transform(prediction)
print(f"Predicted value : {pre}")
*/
```

## Output:
Predicted value : [[203866.53112104]]


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
