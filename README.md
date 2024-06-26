# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1. Import the necessary packages using import statement.

2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Import KMeans and use for loop to cluster the data.
5. Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: R GOKUL SHARAN
RegisterNumber:  212223040052
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Anu Varshini M B
RegisterNumber: 212223240010

import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers (1) (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []  #Within-Cluster sum of square. 
for i in range(1,11):
  kmeans=KMeans(n_clusters = i,init = "k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
```
## Output:
![image](https://github.com/Gokztechz/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/117667038/197daab0-2bf3-4690-81c2-f2ddefe9fe29)
```
data.isnull().sum()
```
## Output:
![image](https://github.com/Gokztechz/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/117667038/86c92352-0ab5-420c-b689-ed6971855dbb)
```
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
```
## Output:
![image](https://github.com/Gokztechz/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/117667038/0ae273e1-0f69-4d57-bffd-29ba5f5b3387)
```
km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

y_pred = km.predict(data.iloc[:,3:])
y_pred
```
## Output:
![image](https://github.com/Gokztechz/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/117667038/be4ce632-e131-4a20-939e-f154ae14a0be)
```
data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
```
## Output:
![image](https://github.com/Gokztechz/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/117667038/cc1fd0d2-d2ec-4857-8e9c-50871c4a219a)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
