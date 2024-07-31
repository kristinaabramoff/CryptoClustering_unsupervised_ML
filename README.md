# CryptoClustering

## Overview
Welcome to the CryptoClustering project! This project delves into analyzing cryptocurrency price changes over 24-hour and 7-day periods using unsupervised learning techniques. Our main objective is to identify distinct groups within the cryptocurrency market by applying clustering algorithms like K-means. Additionally, we explore how data transformations such as Principal Component Analysis (PCA) impact clustering outcomes.

## Software and Tools Used
Python: The primary programming language for data analysis and machine learning.
Pandas: For data manipulation and analysis.
Scikit-learn: Used for machine learning algorithms and data scaling.
hvPlot: For data visualization.
Jupyter Notebook: For interactive coding and analysis.

#Getting Started
## Repository Setup
Create Repository: A new GitHub repository named CryptoClustering was created.
Clone and Setup: Clone the repository to your local machine and set up the initial files.
File Renaming: Rename the starter code file from Crypto_Clustering_starter_code.ipynb to Crypto_Clustering.ipynb.

# Data Loading and Initial Analysis
Data Import: Load the data from crypto_market_data.csv into a DataFrame.
Explore Data: Perform initial data exploration to understand the dataset's structure and characteristics.

## Data Preparation
Standardization: Normalize the data using StandardScaler from Scikit-learn to ensure all features are on a similar scale, which is essential for accurate clustering.
Scaled DataFrame: Create a new DataFrame with scaled data, keeping the "coin_id" from the original data as the index.

## Finding the Optimal Number of Clusters (k)
Using Original Scaled Data:
Elbow Method: Identify the optimal number of clusters by:
Generating potential k values ranging from 1 to 11.
Calculating inertia for each k value.
Plotting inertia to find the "elbow" point that indicates the best k.

## Clustering with K-means (Original Scaled Data)
Model Initialization: Initialize the K-means model with the optimal k value found using the elbow method.
Model Fitting: Fit the K-means model to the scaled data.
Cluster Prediction: Predict clusters and group cryptocurrencies accordingly.
Data Visualization: Create a scatter plot using hvPlot with "price_change_percentage_24h" and "price_change_percentage_7d" on the x and y axes. Points are colored by predicted clusters, with "coin_id" included in the hover tooltip.

## Optimizing Clusters with Principal Component Analysis (PCA)
PCA Transformation: Apply PCA to reduce the dataset to three principal components.
Explained Variance: Analyze the explained variance to understand the information retained by the principal components.

## Using PCA Data for Clustering
New DataFrame: Create a new DataFrame with PCA-transformed data, using "coin_id" as the index.
Elbow Method (PCA Data): Apply the elbow method to find the optimal k value using the PCA data.
K-means Clustering (PCA Data):
Initialize and fit the K-means model using PCA data.
Store predicted clusters in a new column.
Generate a scatter plot with hvPlot, using "PC1" and "PC2" as axes and coloring by K-means labels. "coin_id" is included in the hover tooltip.


## Analysis and Conclusion
The project concludes with an evaluation of how reducing features using PCA affects clustering performance. The results suggest that PCA can lead to more distinct clusters, highlighting the benefits of dimensionality reduction in clustering tasks.

For the full analysis, code, and visualizations, please refer to the CryptoClustering.ipynb notebook in the project repository.

