# 🌸 Iris Dataset Clustering using K-Means

## Introduction
In earlier projects, we explored **supervised learning**, where models are trained using labeled data.  
In this project, we focus on **unsupervised learning**, where the model does **not use labels** and learns patterns using only the feature values.

Here, we perform **clustering**, a key unsupervised learning technique.

---

## What is Clustering?
Clustering is the process of **grouping similar data points together**.  
The goal is to place data points with similar characteristics into the same group, called a **cluster**.

In this project, clustering is performed using the **K-Means algorithm**.

---

## K-Means Clustering
K-Means works by:

1. Selecting **K cluster centers (centroids)**
2. Assigning each data point to the **nearest centroid**
3. Recomputing the centroid as the **mean of all points assigned to it**
4. Reassigning points if another centroid is closer
5. Repeating the process until the centroids no longer change

This results in the dataset being divided into **K distinct clusters**.

---

## K-Means++
To improve clustering performance, **K-Means++** is used for centroid initialization.

- Initial cluster centers are chosen such that they are **far apart from each other**
- This leads to **better initial placement**
- Results in **faster convergence** and more stable clusters

The `KMeans` implementation in scikit-learn uses **K-Means++ by default**.

---

## Dataset
The **Iris dataset** from scikit-learn is used in this project.

- Contains numerical measurements of iris flowers
- Commonly used for machine learning demonstrations
- Although labels exist, they are **not used during training**, as clustering is unsupervised

---

## Feature Scaling
K-Means is a **distance-based algorithm**, making feature scaling essential.

- Features with larger ranges can dominate distance calculations
- Scaling ensures **equal importance** for all features

Therefore, the data is scaled before applying K-Means clustering.

---

## Feature Selection
The following features are used:
- **Petal length**
- **Petal width**

These features were chosen because they:
- Form well-defined and interpretable clusters
- Provide clear separation between data points
- Are effective for visualization

---

## Conclusion
This project demonstrates how **unsupervised learning** can be used to discover patterns in data.  
By applying **K-Means clustering** on the Iris dataset with appropriate **feature scaling and feature selection**, meaningful clusters are formed without using any labels.
