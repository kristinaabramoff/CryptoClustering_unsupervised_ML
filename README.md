# Cryptocurrency Market Clustering Using K-Means and Principal Component Analysis (PCA)


## Overview
The **CryptoClustering** project analyzes cryptocurrency price changes over 24-hour and 7-day periods using unsupervised learning techniques. The primary objective is to identify distinct groups within the cryptocurrency market by applying clustering algorithms like K-means. The project also explores how data transformations, such as Principal Component Analysis (PCA), affect clustering outcomes.

## Software and Tools Used
- **Python**: The primary programming language for data analysis and machine learning.
- **Pandas**: Used for data manipulation and analysis.
- **Scikit-learn**: Utilized for machine learning algorithms and data scaling.
- **hvPlot**: For interactive data visualization.
- **Jupyter Notebook**: For interactive coding and analysis.

## Getting Started

### Repository Setup
1. **Create Repository**: A new GitHub repository named `CryptoClustering` is created.
2. **Clone and Setup**: The repository is cloned to the local machine, and initial files are set up.
3. **File Renaming**: The starter code file, `Crypto_Clustering_starter_code.ipynb`, is renamed to `Crypto_Clustering.ipynb`.

### Data Loading and Initial Analysis
1. **Data Import**: The data from `crypto_market_data.csv` is loaded into a DataFrame.
2. **Explore Data**: Initial data exploration is performed to understand the dataset's structure and characteristics.

## Data Preparation
1. **Standardization**: The data is normalized using `StandardScaler` from Scikit-learn to ensure all features are on a similar scale for accurate clustering.
2. **Scaled DataFrame**: A new DataFrame with the scaled data is created, with the "coin_id" retained from the original data as the index.

## Finding the Optimal Number of Clusters (k)

### Using Original Scaled Data
1. **Elbow Method**: The optimal number of clusters is identified by:
   - Generating potential k values ranging from 1 to 11.
   - Calculating inertia for each k value.
   - Plotting inertia values to find the "elbow" point that indicates the best k.

## Clustering with K-means (Original Scaled Data)
1. **Model Initialization**: The K-means model is initialized with the optimal k value found using the elbow method.
2. **Model Fitting**: The K-means model is fitted to the scaled data.
3. **Cluster Prediction**: Clusters are predicted, grouping cryptocurrencies accordingly.
4. **Data Visualization**: A scatter plot is created using hvPlot, with `price_change_percentage_24h` on the x-axis and `price_change_percentage_7d` on the y-axis. The data points are colored by predicted clusters, and "coin_id" is included in the hover tooltip.

## Optimizing Clusters with Principal Component Analysis (PCA)
1. **PCA Transformation**: PCA is applied to reduce the dataset to three principal components.
2. **Explained Variance**: The explained variance is analyzed to understand the information retained by the principal components.

## Using PCA Data for Clustering
1. **New DataFrame**: A new DataFrame with PCA-transformed data is created, using "coin_id" as the index.
2. **Elbow Method (PCA Data)**: The elbow method is applied to find the optimal k value using the PCA data.
3. **K-means Clustering (PCA Data)**: The K-means model is initialized and fitted using PCA data. The predicted clusters are stored in a new column.
4. **Data Visualization**: A scatter plot is generated using hvPlot, with "PC1" and "PC2" on the axes, and the data points colored by the K-means labels. "coin_id" is included in the hover tooltip.

## Example output

**Elbowcurve**
![elbowcurve](https://github.com/user-attachments/assets/ef837e45-566f-4b62-9bc3-fcf6b9fb5c3b)


**Cluster Plot**
![clustering_plot](https://github.com/user-attachments/assets/3e4c8608-79a5-4212-a263-495dea208fa0)



## Analysis and Conclusion
The project concludes with an evaluation of how reducing features using PCA impacts clustering performance. The results suggest that PCA can lead to more distinct clusters, highlighting the advantages of dimensionality reduction in clustering tasks.

For the full analysis, code, and visualizations, please refer to the `CryptoClustering.ipynb` notebook in the project repository.
