# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 1. Load the Dataset: Use pandas to load the dataset (CSV, Excel, etc.) into a DataFrame.
2. Handle Missing Values: Identify and fill or drop missing values.
3. Encode Categorical Variables: Use label encoding or one-hot encoding for categorical data (e.g., department, gender).
4. Split the Dataset: Divide the dataset into features (X) and target (y), then split into training and testing sets.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: NITHIN BILGATES C
RegisterNumber:2305001022  
*/
```import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt

df=pd.read_csv("/content/Employee_EX6.csv")
data=df.copy()
data.describe()

df

le=LabelEncoder()
data['salary']=le.fit_transform(data['salary'])
data

X=data.drop(['Departments','left'],axis=1)
Y=data['left']

plt.figure(figsize=(80,80))
plot_tree(clf,feature_names=X.columns,class_names=['LEFT','NOT LEFT'],filled=True)
plt.show()

clf=DecisionTreeClassifier()
clf.fit(X,Y)

```
## Output:
![image](https://github.com/user-attachments/assets/5199a8f4-7a52-40f8-bf4a-b9679d9d9ccd)
![image](https://github.com/user-attachments/assets/fa44fbc9-068b-4784-b51f-7d862b6f78d5)
![image](https://github.com/user-attachments/assets/bd7bf0aa-43d7-4f0f-9e38-ca754bdd6d21)
![image](https://github.com/user-attachments/assets/e976144d-b5b2-4df2-a9ba-0eb347f7b9ec)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
