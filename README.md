# KMeans Customer Segmentation

This project focuses on segmenting customers based on their purchasing behavior and income levels using the KMeans clustering algorithm. The goal is to identify meaningful customer groups that can be useful for business decision-making such as targeted marketing or personalized offers.

The implementation is done using Python and scikit-learn, with proper preprocessing, visual analysis, and export of the segmented data.

---

## Dataset

**Mall Customer Segmentation Dataset**

The dataset contains customer-level information such as:
- Customer ID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1–100)

Only the features relevant for clustering are used in the model.

---

## Tools & Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

---

## Project Workflow

1. Loaded and explored the dataset
2. Dropped non-informative columns
3. Applied feature scaling for balanced distance calculation
4. Used the Elbow method to determine the optimal number of clusters
5. Trained a KMeans model with the chosen number of clusters
6. Visualized customer segments using scatter plots
7. Added cluster labels back to the dataset
8. Exported the segmented dataset as a CSV file

---

## Visual Outputs

- Elbow plot to analyze optimal cluster count

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/e27f9ee6-1acf-44ee-96f8-8a7d8d1d2cc9" />


- Cluster visualization showing customer groups based on income and spending score
<img width="618" height="470" alt="image" src="https://github.com/user-attachments/assets/faf9b992-5917-4040-baa8-e2667b914c23" />

---



## What I Learned

Clustering is basically about grouping similar data points together without having predefined labels. Instead of telling the model what is right or wrong, we let it discover patterns on its own based on similarity.

Scaling turns out to be really important in KMeans because the algorithm relies on distance calculations. If one feature has much larger values than another, it can dominate the distance and bias the clustering, which is why standardization helps keep things balanced.

Inertia represents how compact the clusters are. It measures the sum of squared distances between data points and their assigned cluster centers, so lower inertia generally means tighter and more meaningful clusters.

The Elbow method is a visual way to decide how many clusters make sense. By plotting inertia for different values of K, you can spot a point where the improvement starts slowing down, which usually indicates a good balance between simplicity and performance.

KMeans does have its limitations. It struggles with non-spherical clusters, is sensitive to outliers, and requires the number of clusters to be chosen in advance. It can also give different results depending on the initial placement of centroids.
