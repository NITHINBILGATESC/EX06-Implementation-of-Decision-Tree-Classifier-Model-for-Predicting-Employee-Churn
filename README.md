# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import necessary libraries
2. Load the dataset
3. Data Preprocessing
4. Train the Decision Tree Classifier

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: NITHIN BILGATES C
RegisterNumber:2305001022  
*/
```
import pandas as pd
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
## Output:
![image](https://github.com/user-attachments/assets/997552a8-424e-45c6-b135-685688002632)
![image](https://github.com/user-attachments/assets/fe8a1c97-2e8e-4ac7-a763-a959ee959de9)
![image](https://github.com/user-attachments/assets/570c94cc-a6f7-44a0-a141-51dc6849d847)
![image](https://github.com/user-attachments/assets/a1e67e40-e676-49c0-a3fe-8d9e440f9d55)
![image](https://github.com/user-attachments/assets/60617b3b-612c-451b-8932-62604d6bc4b5)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
