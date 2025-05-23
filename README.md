# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import dataset and print head,info of the dataset
2. check for null values
3. Import kmeans and fit it to the dataset
4. Plot the graph using elbow method
5. Print the predicted array
6. Plot the customer segments

## Program:
```
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Kamalesh y
RegisterNumber:  212223243001
```
```
import pandas as pd
import numpy as np
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]
plt.scatter(X['Annual Income (k$)'], X['Spending Score (1-100)'])
plt.xlabel('Income')
plt.ylabel('Score')
plt.show()
kmeans=KMeans(n_clusters=5)
kmeans.fit(X)
labels=kmeans.labels_
centers=kmeans.cluster_centers_
colors = ['r', 'g', 'b', 'c', 'm']
for i in range(5):
    plt.scatter(X[labels==i]['Annual Income (k$)'], X[labels==i]['Spending Score (1-100)'], color=colors[i])
plt.scatter(centers[:,0], centers[:,1], color='black', s=200, label='Centroids')
plt.xlabel('Income')
plt.ylabel('Score')
plt.legend()
plt.show()
```
## Output:
![K Means Clustering for Customer Segmentation](sam.png)
![Screenshot 2025-05-13 085249](https://github.com/user-attachments/assets/132947b1-be7a-44e9-97dc-43fec2b20fb1)

![Screenshot 2025-05-13 085332](https://github.com/user-attachments/assets/00f59554-f58a-4535-8e37-597e76aa4547)

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
