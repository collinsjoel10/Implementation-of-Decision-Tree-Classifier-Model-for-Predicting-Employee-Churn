# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy.
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: JOEL P
RegisterNumber:  212222230057


import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```

## Output:
### Initial data set:

![272784342-4fdab09e-a67b-45ba-b6ea-1430530c1f44](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/db30aad4-cf20-42d0-9f7f-0309ffa304da)

### Data info:


![272784393-40bbf9f1-0b4b-4554-9398-67eb9f3e3a6c](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/504e7fcf-d92d-456d-9846-94eab476748e)

### Optimization of null values:

![272784411-130e597d-f5e9-42fa-96e7-5bcfb522f28a](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/730ce9e2-d1b0-46aa-8548-53e56aff31f0)

### Assignment of x values:

![272784425-b638f42f-9423-4dcd-81ce-d6af81aa7bc4](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/23273443-6f17-4776-9499-e2dc3df79fda)



### Assignment of y values:

![272784454-48b19d12-f586-4f21-8f4f-44a9e7562409](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/9773d4d8-2919-4591-aebc-ca10ab74a56b)


### Converting string literals to numerical values using label encoder:

![272784485-efd59b97-4b8e-4855-8f54-6194f2ec6d44](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/67e701af-5984-4c5e-baec-267c88b4dd57)

### Accuracy:
![273142795-126faecd-11de-4cdb-9637-e98c7bba520e](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/d4752254-e4e9-4e06-94cf-b2238bb68c5d)
### Prediction:

![272784517-655f10f8-8fff-4d48-9115-89736a07c6fb](https://github.com/AdhithyaMR/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118834761/20b00569-7d31-4850-b71a-03fd3c319e93)





## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
