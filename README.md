# task8

step 1: Load Dataset

We use the Mall_Customers.csv dataset. It contains features like:

CustomerID

Gender

Age

Annual Income (k$)

Spending Score (1-100)

These features help in segmenting customers into meaningful groups.

 Step 2: Preprocessing
 
Drop CustomerID: Not useful for clustering.

Convert Gender to numeric: Machine learning algorithms can’t handle text, so we map 'Male' to 0 and 'Female' to 1.

Scale the Data: Features like income and age are on different scales, so we standardize them using StandardScaler for better performance of K-Means (which uses Euclidean distance).

Step 3: Dimensionality Reduction (PCA)

We reduce features to 2 dimensions using PCA so we can visualize clusters on a 2D graph.

Step 4: Elbow Method to Find Optimal K

We run K-Means for different values of K (1 to 10) and plot inertia (sum of distances to centroids) for each.

Elbow Point: The point where the decrease in inertia slows down indicates the optimal number of clusters (K).

Step 5: Train K-Means

Use the chosen K (e.g., 5) to fit K-Means.

fit_predict() assigns a cluster to each customer.

Add this cluster label to the original data.

Step 6: Visualize Clusters

We use the 2D PCA result and plot each data point color-coded by its cluster. This helps visualize how well K-Means separated different groups.

Step 7: Silhouette Score

Measures how similar a data point is to its own cluster vs other clusters.

Range: -1 (bad) to 1 (good)

A higher score means better-defined clusters.

