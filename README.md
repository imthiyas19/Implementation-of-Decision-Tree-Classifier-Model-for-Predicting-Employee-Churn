# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1.import pandas module and import the required data set.

2.Find the null values and count them.

3.Count number of left values.

4.From sklearn import LabelEncoder to convert string values to numerical values.

5.From sklearn.model_selection import train_test_split.

6.Assign the train dataset and test dataset.

7.From sklearn.tree import DecisionTreeClassifier.

8.Use criteria as entropy.

9.From sklearn import metrics.

10.Find the accuracy of our model and predict the require values.

## Program:
```ruby
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

Developed by: MOHAMMED IMTHIYAS .M
RegisterNumber: 212222230083
```

```python
import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)


from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:

### Data Head:



![datahead](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/5f27304c-4df0-4b4a-b8d7-511eba6c0929)




### Data Info:


![datainfo](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/d4067def-0dae-4afa-9e05-74f9e576da6a)




### Isnull() and Sum():



![isnull_sum](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/e63d63e6-df32-425e-97dd-8b30547baae9)





### Data ValueCounts:


![valuecounts](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/f4c0c8e1-e72b-41a9-8794-78d771f2cdfc)





### Data Head for SALARY:




![salaryhead](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/997dfe4b-cb85-467e-8f21-4fe99fb5487d)



### X Data:


![xhead](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/fe74363b-3151-4971-85ce-affa8c902722)





### Accuracy Value:


![accuracy](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/3ddd4bce-9533-4dfe-b416-c3a26d7aacc0)





### Predict Value [0.5,0.8,9,260,6,0,1,2]:


![predict](https://github.com/imthiyas19/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/120353416/d086e68f-8048-458d-9f24-727b5b83066f)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
