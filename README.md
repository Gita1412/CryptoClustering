# Crypto Clustering Project

## Files
Download the following files to help you get started:
- Module 19 Challenge files (external link).

## Instructions
1. **Rename the File**
   - Rename `Crypto_Clustering_starter_code.ipynb` as `Crypto_Clustering.ipynb`.

2. **Load the Data**
   - Load `crypto_market_data.csv` into a Pandas DataFrame.
   - Get the summary statistics and visualize the data.

## Prepare the Data
- Use `StandardScaler()` from `scikit-learn` to normalize the data.
- Create a new DataFrame with the scaled data and set `coin_id` as the index.
- Verify that the first five rows of the scaled DataFrame are correctly formatted.

## Find the Best Value for k Using the Scaled DataFrame
- Use the elbow method to find the best k value:
  1. Create a list of k-values from 1 to 11.
  2. Compute the inertia for each k value.
  3. Store the inertia values and plot an elbow curve.
  4. Visually identify the optimal k value.
  5. Answer: **What is the best value for k?**

## Cluster Cryptocurrencies with K-Means Using the Scaled DataFrame
- Initialize the K-Means model with the best k value.
- Fit the model using the scaled DataFrame.
- Predict cluster labels and add them to a new column.
- Create a scatter plot using `hvPlot`:
  - x-axis: `price_change_percentage_24h`
  - y-axis: `price_change_percentage_7d`
  - Color points based on K-Means labels.
  - Add `coin_id` to the hover parameter for identification.

## Optimize Clusters with Principal Component Analysis (PCA)
- Perform PCA on the original scaled DataFrame.
- Reduce features to three principal components.
- Retrieve explained variance and answer:
  **What is the total explained variance of the three principal components?**
- Create a new DataFrame with the scaled PCA data, setting `coin_id` as the index.

## Find the Best Value for k Using the PCA DataFrame
- Use the elbow method on the PCA DataFrame:
  1. Compute inertia for k-values from 1 to 11.
  2. Store and plot inertia values in an elbow curve.
  3. Identify the optimal k value.
  4. Answer:
     - **What is the best value for k when using the scaled PCA DataFrame?**
     - **Does it differ from the best k value found using the original scaled DataFrame?**

## Cluster Cryptocurrencies with K-Means Using the PCA DataFrame
- Initialize the K-Means model with the best k value for PCA data.
- Fit the model and predict cluster labels.
- Add predicted clusters to a new column in the PCA DataFrame.
- Create a scatter plot using `hvPlot`:
  - x-axis: `PC1`
  - y-axis: `PC2`
  - Color points based on K-Means labels.
  - Add `coin_id` to the hover parameter.

## Answer the Following Question
- **What is the impact of using fewer features to cluster the data using K-Means?**


instructions source : courses.bootcampspot.com
