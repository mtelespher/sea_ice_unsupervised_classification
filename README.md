# Unsupervised classification of Satellite imagery to classify Sea ice or Leads

## Introduction
This repository contains the file 'Unsupervised_Learning_Methods.ipynb where this unsupervised classification implementation is carried out. 

### Project set up:

The satellite images used in this unsupervised learning application are from the Copernicus browser, a free online tool which allows users to access the imagery captured by the Sentinel satellite constellations via https://browser.dataspace.copernicus.eu/.

Prerequisites include the installation of the following packages, which can be done by running the following code:

```
pip install netCDF4
```

```
pip install basemap
```
```
pip install cartopy
```

We use Google Colab to execute the Jupyter notebook attached, this platform offers connectivity to Google Drive, where the files for this application are stored. To access Google Drive through Colab,  mount it to the Colab instance using:

```
from google.colab import drive
drive.mount('/content/drive')
```

## Unsupervised classification methods

Two unsupervised learning methods are utilised in this machine learning application, K means and Gaussian Mixture Model (GMM).

### K means

K-means clustering is an unsupervised learning algorithm used to partition a dataset into k clusters, where k is a pre-defined number of groups. The algorithm works by defining k centroids and assigning each data point to the nearest centroid, aiming to minimize the size of the centroids.

Why K-means for Clustering?

- Unknown Data Structure: Ideal for exploratory data analysis when the data distribution is not known.
- Simplicity and Scalability: Easy to implement and handle large datasets efficiently.

Process:

	1.	Choosing K: The number of clusters must be specified beforehand.
	2.	Centroid Initialization: Initial placement of centroids influences the final clusters.
	3.	Assignment Step: Data points are assigned to the nearest centroid using squared Euclidean distance.
	4.	Update Step: Centroids are updated to the mean of assigned data points.
  
Advantages of K-means

- Efficiency: Computationally fast and effective.
- Interpretability: The results are easy to understand and explain.

# GMM

Gaussian Mixture Models (GMM) are probabilistic models used to represent normally distributed subpopulations within a larger population. The model assumes that the data is generated from a mixture of several Gaussian distributions, each characterized by its own mean and variance. GMMs are widely utilized for clustering and density estimation, allowing complex distributions to be represented through combinations of simpler Gaussian components.

Why Use Gaussian Mixture Models for Clustering?
	•	Soft Clustering: Unlike K-means, GMM provides the probability of each data point belonging to each cluster, offering a soft classification and insights into data uncertainties.
	•	Flexible Cluster Covariance: GMMs allow clusters to have different sizes and shapes, capturing true data variance more effectively.

Key Components of GMM
	1.	Number of Components: Similar to K in K-means, this represents the number of Gaussian distributions (clusters) in the model.
	2.	Expectation-Maximization (EM) Algorithm: An iterative process that improves the likelihood of the data fitting the model.
	3.	Covariance Type: Determines the shape, size, and orientation of the clusters (e.g., spherical, diagonal, tied, or full covariance).

 The Expectation-Maximization (EM) Algorithm in GMM
	•	Expectation Step (E-step): Calculates the probability that each data point belongs to each cluster.
	•	Maximization Step (M-step): Updates the parameters of the Gaussian components (mean, covariance, and mixing coefficients) to maximize data likelihood.
	•	The process repeats until convergence, when parameters stabilize between iterations.

Advantages of GMM
	•	Soft Clustering: Provides a probabilistic framework for understanding uncertainties in data assignments.
	•	Cluster Shape Flexibility: GMMs adapt to ellipsoidal cluster shapes due to their flexible covariance structure.

## Contact details

Contact me on michael.telespher.24@ucl.ac.uk for further questions around this project.

## Acknowledgements

This project was completed as part of my education at UCL. It forms part of the module 'Artificial Intelligence for Earth Observations' taught by Dr Michel Tsamadados, large portions of this code have been adapted from previous work.
