# CryptoClustering

## Overview

For this project, I analyzed data on cryptocurrencies to predict whether or not they are affected by 24-hour or 7-day price changes. I used unsupervised learning (clustering) to make these predictions.

You can find my code and all plots in Crypto_Clustering.ipynb.

### Clustering with the Original Scaled DataFrame

I scaled the original dataframe and used it to plot the elbow curve in order to determine the ideal number of clusters, 4. I then build a K-means model to create and visualize these four clusters. Clusters 0 and 2 were substantial. Cluster 0 seemed to portray a mix of values around 0 for both 24-hr and 7-day price changes, while cluster 2 portrayed data points with higher 7-day price changes and lower 24-hour price changes, which could indicate cryptocurrencies that are less volatile and better for long-term investments. Clusters 1 and 3 contained only one value each.

### Clustering with a ScaledPCA DataFrame

I created a PCA model to reduce the original scaled DataFrame to three principal components, which together had an explained variance of 6.422. I used Kmeans to plot the elbow curve and determine the ideal number of clusters, which was also 4. When I plotted the clusters for the PCA DataFrame, I noticed similar patterns to the original scaled DataFrame. There were still 2 substantial clusters, 0 and 2, though they were much more compact and less variable. Clusters 1 and 3 still only had 1 data point each. Using fewer features to cluster the data in the PCA DF reduced the amount of variability and "noise" that ocurred in the Original Scaled DF. 