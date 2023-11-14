# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the required libraries .
2.Read the data frame using pandas.
3.Get the information regarding the null values present in the dataframe.
4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5.Determine training and test data set.
6.Apply k means clustering for customer segmentation.


## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: VELAN D
RegisterNumber: 212222040176

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss=[]   #Within-Cluster Sum of Squares.

for i in range(1,11):
    kmeans=KMeans(n_clusters=i, init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
    
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("ELBOW METHOD GRAPH")
plt.show()
km = KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="green",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="purple",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="gold",label="cluster4")
plt.legend()
plt.title("Customer Segments")
 
*/
```

## Output:

data.head()

![282255345-4aa0e648-c55c-482b-8a9e-e7045dcc1cb0](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/ae9e74ce-a3f2-4319-be5d-5417d1b7355b)

data.info()

![282255418-5b7c6adb-09cd-4f8f-b2e1-48f88e1ace52](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/e2376c6c-5383-4de1-9f67-129b39089c15)

data.isnull().sum()

![282255426-93abcc5d-b598-4dc6-8465-cbcaaa45d671](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/1cc0b48d-25c5-4ff1-97db-c304aa236755)

Elbow Method Graph

![282255435-ed032d5e-830d-4725-938b-45795022d44a](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/9d6b98df-bb8a-4e55-a414-9de79cde1aec)

KMeans Clusters

![282255443-d37f64a4-47eb-4d9c-9758-b6ca015e312f](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/78af28b1-bc66-4c4a-9c30-1aec5bc8a8a3)

Y_pred

![282255447-e962be05-290c-4d7c-ae5f-64ae5f73290b](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/b3530240-7825-4017-b175-bd256307adbe)

Customers Segments Graph

![282255464-0c0ade5b-fe1d-4afe-958c-5a99ae2d1af3](https://github.com/VELANDHANANJAYAN/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119405038/357dbad0-d98f-4fcf-a8af-0671a6cbab37)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
