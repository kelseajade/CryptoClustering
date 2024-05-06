# CryptoClustering
 In this challenge, CryptoCLustering, normalize the data from the provided CSV file using the StandardScaler() module from scikit-learn. After loading the data into a DataFrame, the data is normalized. The scaled data is then stored in a new DataFrame, with the original "coin_id" index set as the index for the new DataFrame.

The elbow method is used to determine the optimal number of clusters (k) for K-means clustering. A range of k values from 1 to 11 is considered, and the inertia values (sum of squared distances) are computed for each k value. A line chart is plotted to visualize the inertia values against the k values.

K-means clustering is performed on the original scaled data using the best value for k determined from the elbow method. The data is clustered, and each cryptocurrency is assigned to a cluster. A scatter plot is then created to visualize the clusters, with the x-axis representing one principal component (PC1) and the y-axis representing another principal component (PC2). Cryptocurrency names are included in the hover information for identification. The determined K value is 4.

Principal Component Analysis is applied to the original scaled data. The explained variance of each principal component is retrieved. The variance is 0.8950. A new DataFrame is created with the PCA data, and the "coin_id" index is set.

Similar to the process with the original scaled data, the elbow method is employed on the PCA data to find the optimal value for k. The inertia values are computed for different k values, and a line chart is plotted to identify the elbow point, determining the best value for k when using the PCA data.

K-means clustering is performed on the PCA data using the best value for k determined from the elbow method. The value for k is still 4. The data is clustered, and a scatter plot is created to visualize the clusters. However, this time, the scatter plot uses different features and includes cryptocurrency names for identification.

Using fewer features to cluster the data using K-means changes the clustering results. It reduces the dimensionality of the data while retaining most of the variance. This can lead to more efficient computation and visualization of clusters but can also have loss of information.
