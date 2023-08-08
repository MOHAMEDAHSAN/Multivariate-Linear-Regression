# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
#### Step1 - Import pandas as pd.
#### Step2 - Read the csv file.
#### Step3 - Extract 'Weight' and 'Volume' as 'x' and 'CO2' as 'y'.
#### Step4 - Create linear regression model and fit it with the data, and find the coefficients and intercept.
#### Step5 - Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm3 and print.

## Program:
~~~Python
# Multivariate Linear Regression
# Developed by : S MOHAMED AHSAN
# Register No : 23001044
from google.colab import drive
drive.mount('/content/drive')
import pandas as pd
from sklearn import linear_model
df=pd.read_csv('/content/drive/MyDrive/cars.csv')
X=df[['Weight', 'Volume']]
y=df['CO2']
regr=linear_model.LinearRegression()
regr.fit(X,y)
print('Coefficients :',regr.coef_)
print('Intercept :',regr.intercept_)
print('Predicted CO2 for the input :',regr.predict([[3300,1300]]))
~~~
## Output:
![multi](/Multivariate.png)
## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.