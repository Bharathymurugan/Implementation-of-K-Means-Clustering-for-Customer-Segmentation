# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the customer dataset containing annual income and spending score.
2. Select the required features and apply the K-Means clustering algorithm with the desired number of clusters.
3. Fit the K-Means model to the dataset and assign cluster labels to each customer.
4. Visualize the clusters with centroids using a scatter plot and display the clustered dataset.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Bharathy M
RegisterNumber:  212225040046
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = {
    'CustomerID': [1,2,3,4,5,6,7,8,9,10],
    'Gender': ['Male','Female','Female','Male','Female','Male','Male','Female','Female','Male'],
    'Age': [19,21,20,23,31,22,35,30,25,28],
    'Annual Income (k$)': [15,16,17,18,19,20,21,22,23,24],
    'Spending Score (1-100)': [39,81,6,77,40,76,6,94,3,72]
}

df = pd.DataFrame(data)

X = df[['Annual Income (k$)', 'Spending Score (1-100)']]

kmeans = KMeans(n_clusters=3, init='k-means++', random_state=42)

df['Cluster'] = kmeans.fit_predict(X)

plt.figure(figsize=(8,6))

for i in range(3):
    plt.scatter(
        X[df['Cluster']==i]['Annual Income (k$)'],
        X[df['Cluster']==i]['Spending Score (1-100)'],
        label=f'Cluster {i+1}'
    )

plt.scatter(
    kmeans.cluster_centers_[:,0],
    kmeans.cluster_centers_[:,1],
    s=200,
    c='yellow',
    label='Centroids',
    marker='X'
)

plt.title('Customer Segmentation (K-Means)')
plt.xlabel('Annual Income (k$)')
plt.ylabel('Spending Score (1-100)')
plt.legend()
plt.show()

print(df)
*/
```

## Output:
<img width="708" height="515" alt="Screenshot 2026-05-22 095204" src="https://github.com/user-attachments/assets/36df9e90-ff4b-432e-b83d-226abd859070" />

<img width="589" height="387" alt="image" src="https://github.com/user-attachments/assets/192fd7de-4e3c-47fc-8d1d-8c095d7a03a2" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
