# Iris Dataset Clustering Analysis

## Overview
This project demonstrates the application of **unsupervised machine learning** techniques on the **Iris dataset** using **K-Means Clustering** and **Hierarchical Clustering**. To visualize the clustering results, **Principal Component Analysis (PCA)** is used to reduce the dataset from four dimensions to two dimensions.

---

## Objective
The objective of this assignment is to:

- Load and preprocess the Iris dataset.
- Apply K-Means Clustering.
- Apply Hierarchical Clustering.
- Visualize clusters using PCA.
- Compare the performance and characteristics of both clustering algorithms.

---

## Dataset
The project uses the **Iris dataset** available in the **Scikit-learn** library.

### Dataset Information
- **Total Samples:** 150
- **Features:**
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width
- **Target Classes (Reference Only):**
  - Setosa
  - Versicolor
  - Virginica

Since clustering is an unsupervised learning technique, the target labels are removed before training the models.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Loaded the Iris dataset using Scikit-learn.
- Converted the dataset into a Pandas DataFrame.
- Inspected the dataset using:
  - `head()`
  - `shape`
  - `info()`
  - `describe()`
- Checked for missing values.
- Removed duplicate records.
- Dropped the target (species) column.
- Standardized all numerical features using **StandardScaler**.

Feature scaling ensures that each feature contributes equally during distance calculations.

---

## K-Means Clustering

### Algorithm
K-Means partitions the dataset into a predefined number of clusters by minimizing the distance between data points and their corresponding cluster centroids.

### Configuration
- Number of Clusters: **3**
- Random State: **42**

### Visualization
Principal Component Analysis (PCA) was used to reduce the dataset to two dimensions for visualization.

### Observation
- Three distinct clusters were formed.
- One cluster is clearly separated.
- Two clusters show slight overlap due to similarities between flower species.

---

## Hierarchical Clustering

### Algorithm
Hierarchical Clustering builds a hierarchy of clusters by iteratively merging the closest clusters until the desired number of clusters is reached.

### Configuration
- Number of Clusters: **3**
- Linkage Method: **Ward**

### Visualization
PCA was used to visualize the clustered data.

A dendrogram was also generated to display the hierarchical relationships among observations.

### Observation
- Three meaningful clusters were obtained.
- Results closely resemble those produced by K-Means.
- The dendrogram confirms that selecting three clusters is appropriate for the Iris dataset.

---

## Comparison

| Feature | K-Means | Hierarchical Clustering |
|----------|----------|-------------------------|
| Method | Centroid-Based | Tree-Based |
| Cluster Initialization | Random | No Initialization Required |
| Number of Clusters | Predefined | Can be inferred from Dendrogram |
| Speed | Fast | Slower |
| Visualization | PCA Scatter Plot | PCA Scatter Plot + Dendrogram |

---

## Results

- Successfully preprocessed the Iris dataset.
- No missing values were found.
- Duplicate records were removed.
- Numerical features were standardized.
- PCA effectively reduced the dataset for visualization.
- K-Means identified three meaningful clusters.
- Hierarchical Clustering also identified three natural groups.
- The dendrogram validated the clustering structure.

---

## Conclusion

This project successfully demonstrates the use of **K-Means Clustering** and **Hierarchical Clustering** on the Iris dataset. Proper preprocessing, including duplicate removal and feature scaling, improved clustering performance. PCA provided an effective way to visualize high-dimensional data.

Both clustering algorithms successfully identified the natural grouping of Iris flowers. K-Means offers a fast and efficient clustering solution, while Hierarchical Clustering provides additional insights into cluster relationships through the dendrogram.

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy

---

## Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from sklearn.datasets import load_iris
from sklearn.preprocessing import StandardScaler
from sklearn.cluster import KMeans, AgglomerativeClustering
from sklearn.decomposition import PCA

from scipy.cluster.hierarchy import dendrogram, linkage
```

---

## Project Structure

```
Assignment 08/
│
├── Assignment 08.ipynb
├── README.md
└── Report.pdf (Optional)
```

---

## Author

**Athul C Ravindran**

Machine Learning Assignment – Clustering Analysis using the Iris Dataset.
