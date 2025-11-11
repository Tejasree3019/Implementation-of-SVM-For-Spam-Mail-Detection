# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import pandas.

2.Define CSV file path.

3.Read CSV into DataFrame, specifying detected encoding.

4.Display first few DataFrame rows and information.

5.Check for missing values in the DataFrame.

6.Split data into training and testing sets, train SVC model, predict labels, and calculate accuracy score.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Tejasree.K
RegisterNumber: 212224240168

import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

*/
```

## Output:

data.head()

<img width="1252" height="380" alt="image" src="https://github.com/user-attachments/assets/684f9b6b-c52f-4ae5-9c16-c43d7233d7a4" />

data.info()

<img width="854" height="411" alt="image" src="https://github.com/user-attachments/assets/b4e34f25-91d5-41f4-ac2e-75a605b1b42c" />

data.isnull().sum()

<img width="369" height="450" alt="image" src="https://github.com/user-attachments/assets/88b0e6da-4d89-463b-a5fa-5cc8f633d986" />

y_pred

<img width="1061" height="501" alt="image" src="https://github.com/user-attachments/assets/1367b01e-3e8e-463d-89c7-810835a8fc4b" />

accuracy

<img width="827" height="167" alt="image" src="https://github.com/user-attachments/assets/9bf93182-6885-4850-a0a9-7ab4310b0a9d" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
