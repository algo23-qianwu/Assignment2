# Eigenportfolios for statistical arbitrage
This analysis shows an application of Principal Component Analysis in order to develop a pairs trading strategy to capture statistical arbitrage in the Precious Metals Market.

## Data
- This dataset deals with the london fix spot prices for gold, silver, platinum, and palladium.
- In this analysis, we used the price data from 2008 to 2018. 
- The london fix has an AM and PM fix for gold, platinum, and palladium, while it only has 1 fix for silver.
- Since we need to treat the AM and PM fix as different events, we separate this so that each fix represents a row in the dataset. Since Silver only has one fix, we will duplicate its fix price for both the AM and PM value.

## PCA
- PCA is a popular technique used in data science to reduce the dimensionality of the data while retaining as much information of the data as possible.
- The principal components of the decomposition of the covariance matrix that capture the most information of the dataset whenever the dataset is projected onto that vector. 
   - The Eigenvalue that corresponds to that eigenvector is how strongly that eigenvector explains the variance of the data. 
   - The left singular vectors tell us how much each particular row accounts for the variance of the data,
   - while the right singular vectors tell us how much each particular column to the data.

## Interpretation of Eigenvalues and Eigenvectors
1. Matrix A: a basket of m stocks over n days
2. PCA: decomposition of the left principal components multiplied by the eigenvales multiplied by the right principal vectors.
   1. eigenvalues: how much of the variance of the dataset is captured in each "concept" of the dataset.
   2. left eigenvectors: how much the rows (a.k.a the stocks) correspond to each concept.
   3. right eigenvectors: how much the columns (a.k.a the daily prices) correspond to each concept.






