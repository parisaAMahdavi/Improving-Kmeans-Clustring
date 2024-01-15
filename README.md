
![Example Image](images/example.png)
# Improving K-means Clustering Performance on GPT-Related Reddit Comments

$\color{Orange}{\textsf{Introduction}}$

K-means clustering is a widely used unsupervised machine learning algorithm for partitioning datasets into K-distinct, non-overlapping clusters. In this notebook, we aim to apply K-means clustering to Reddit comments discussing GPT.

- Our exploration involves two text vectorization methods: TF-IDF, a simpler approach based on word frequencies, and BERT, a deep learning-based model known for capturing rich context and semantics. The primary goal is to compare the performance of these methods on our dataset.

- Additionally, we perform an alternative test by employing Principal Component Analysis (PCA) and Uniform Manifold Approximation and Projection (UMAP) to reduce the dimensionality of features derived from BERT. This step is crucial as BERT often produces high-dimensional feature sets, making it challenging for K-means to analyze effectively. By reducing dimensionality, we aim to enhance K-means' ability to cluster the data effectively based on the reduced feature space.

- In another approach, we aim to select initial centroids by leveraging the principal components. This method involves using the principal components obtained through PCA to initialize the centroids for the K-means clustering algorithm. By utilizing these principal components as starting points for centroids, we aim to potentially enhance the convergence and performance of the clustering process, allowing for a more optimized arrangement of clusters in the feature space.

$\color{Orange}{\textsf{Text Vectorization Methods}}$

1. **TF-IDF Vectorization**
2. **BERT Embeddings**

$\color{Orange}{\textsf{Dimensionality Reduction strategies:}}$
1. **PCA**
2. **UMAP**

$\color{Orange}{\textsf{Centroid Initialization Techniques:}}$
1. **K-means++ Initialization**
2. **Principal Component Initialization**

So this notebook compares different approaches for unsupervised clustering text data including:

1. Clustering based on TF-IDF features.
2. Clustering based on BERT features.
3. Clustering on TF-IDF features reduced using Truncated Singular Value Decomposition (TSVD).
4. Clustering on BERT features reduced using Principal Component Analysis (PCA).
5. Clustering on BERT features reduced using Uniform Manifold Approximation and Projection (UMAP).
6. Clustering with PCA-reduced BERT features using PCA initialization.

$\color{Orange}{\textsf{Evaluation and Results}}$
Our benchmark measures the performance of the clustering obtained via different metrics:
1. Inertia
2. Davies-Bouldin
3. Calinski-Harabasz
4. Silhouette Coefficient
