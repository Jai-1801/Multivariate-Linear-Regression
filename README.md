# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas as pd.

### Step2
Read the csv file.

### Step3
Get the value of X and y variables

### Step4
Create the linear regression model and fit.

### Step5
Predict the CO2 emission of a car where the weight is 3300kg, and the volume is 1300cm3.

## Step 6
Print the predicted output

## Program:
```
#Developed by: Jai Surya
#Register number: 23002572


import pandas as pd
from sklearn import linear_model 

df = pd.read_csv("cars.csv")

x = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(x,y)


print('Coefficient:',  regr.coef_)
print('Intercept', regr.intercept_)


predictedCO2 = regr.predict([[3300,1300]])
print("Predicted co2 for the inputs is",predictedCO2)

```
## Output:
![output](/output02.png)

##  Insert your output:

Coefficient: [0.00755095 0.00780526]

Intercept 79.69471929115939

Predicted co2 for the inputs is [114.75968007]

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.