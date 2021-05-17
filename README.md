# Clustering_Bank
K-Means clustering of a Portuguese bank's clients.

The data is related to direct marketing campaign direct marketing campaigns of a Portuguese banking institution. The dataset has bank client data, data related with the last contact of the current campaign and, social and economic context attributes.

## K-MEANS
```
cost = []
for num_clusters in list(range(1,5)):
    kmode = KModes(n_clusters=num_clusters, init = "Cao", n_init = 4, verbose=1)
    kmode.fit_predict(bank_lab)
    cost.append(kmode.cost_)
```
#### The optimal number of clusters is 2 as shown by elbow method.
```
y = np.array([i for i in range(1,5,1)])
plt.plot(y,cost);
```

![Screenshot 2021-05-17 at 19 36 03](https://user-images.githubusercontent.com/71548024/118532320-210d1a80-b747-11eb-89ad-2e4cafb4eb91.png)


## Results
As it can be observed, each cluster has considerable differences in terms of job positions of the clients, although that's not the only feature that defines each cluster. 

### Cluster 1

![Screenshot 2021-05-17 at 19 33 22](https://user-images.githubusercontent.com/71548024/118531985-c1167400-b746-11eb-94d6-54d3cf08733c.png)


### Cluster 0

![Screenshot 2021-05-17 at 19 34 35](https://user-images.githubusercontent.com/71548024/118532156-ed31f500-b746-11eb-9f1b-ef684ae0855d.png)

We can now export both clusters' dataframe to proceed with other analyses for a better targeting.

