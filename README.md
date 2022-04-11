# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 
# ALGORITHM
### STEP 1
Create a new file in jupyter notebook.
### STEP 2
Upload the given csv file.
### STEP 3
Write codes for Data Analysis (EDA).
### STEP 4
Plot the result in various formats.
### STEP 5
End the program.

# CODE
```
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()
sns.displot(df["Age"])
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
```

# OUPUT
![162117686-ae5cd94a-9736-4b27-9bee-3d74f079c86c](https://user-images.githubusercontent.com/93427278/162769013-0644e5f2-c086-4d9a-9703-48ae890ff837.png)
![162117710-21e804e1-5cbd-427f-9929-fc3e2c1a9c68](https://user-images.githubusercontent.com/93427278/162769053-460a28cb-bfdd-4e34-8495-fa2ef472812a.png)
![162117741-39c2019b-617e-482f-9b02-8ee8fe93a7f3](https://user-images.githubusercontent.com/93427278/162769084-b18a4220-1376-403d-849a-725a355f400e.png)
![162117764-fbcf630b-626c-46c0-92a1-6bcbf16540d9](https://user-images.githubusercontent.com/93427278/162769116-48603df1-375b-43fa-b98c-d4a73f18f808.png)
![162117783-e5b42f79-4319-4879-8635-30a888a7fca6](https://user-images.githubusercontent.com/93427278/162769167-8f76d392-7a97-42b5-93b2-2c922971324d.png)
![162117814-5574cf0a-e78b-450a-b52a-ea90fc828e91](https://user-images.githubusercontent.com/93427278/162769191-e90c4f55-735e-4952-9a17-7e40c4519c13.png)
![162117832-6887be9f-e365-4465-8a98-92b1c08003b5](https://user-images.githubusercontent.com/93427278/162769235-587e19d7-437f-4667-9965-67fed715f22b.png)
![162117846-69fd3263-7b84-4767-b2e9-1facde20a60a](https://user-images.githubusercontent.com/93427278/162769277-53db60c2-feae-4631-bec1-c0d276a1fd10.png)
![162117862-80601ef5-a51b-49a3-a59d-58f97c4701a3](https://user-images.githubusercontent.com/93427278/162769332-156b688d-e618-469f-a074-845589517419.png)

# RESULT
Thus the data of the dataset is analyzed using Exploratory data analysis.
