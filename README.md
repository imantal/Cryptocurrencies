# Cryptocurrencies

## Overview of the Analysis
<div align="justify"> 

The purpose of this project was to create a report that includes what cryptocurrencies were on the trading market and how they could be grouped to create a classification system for the new investment. The provided data was not ideal, so it needed to be processed to fit the machine learning models. Since there was no known output, it was decided to use unsupervised machine learning. 

## Data overview and preparation
The original data had about 7 columns and 1,250 rows and included information such as coin name, total coin minded and total coin supply. The data cleaning and preparation included removing the cryptocurrencies that were not being traded, rows with null values and keeping only rows for the coins that had been minded. The text features were converted to numerical variables and then StandardScaler was used to standardize the features. Principal component analysis (PCA) algorithm was used to reduce the dimensions of the features to three components. 

## Clustering cryptocurrencies using K-means 
The K-means algorithm clusters data by trying to separate samples in K groups of equal variance, minimizing a criterion known as the inertia or within-cluster sum-of-squares. This algorithm requires the number of clusters to be specified.  An easy method for determining the best number for K is the elbow curve. Inertia is one of the most common objective functions to use when creating an elbow curve. The inertia objective function measures the amount of variation in the dataset. Figure 1 shows the elbow curve created for this study. Four number of clusters, K=4, is used for this study. The K-means model with 4 clusters and 3 PCA components were used to cluster the cryptocurrencies. 

 <div align="center">
 
![image](https://user-images.githubusercontent.com/103223944/184576825-638a1761-6776-4ff7-b589-73e38facfc44.png)

Figure 1: Elbow curve
  
<div align="left">  

## Visualization of the clustering results 
Using Plotly Express and hvplot, the 4 distinct groups that corresponded to the 3 principal components were visualized as shown in Figure 2. Hvplot table function was used to create a table for all the currently tradable cryptocurrencies as shown in Figure 3. Hvplot was also used to plot the TotalCoinsMined minded vs. TotalCoinSupply after they were scaled as shown in Figure 4.

 <div align="center">
 
!![image](https://user-images.githubusercontent.com/103223944/184576860-58b152fc-fab3-4c9e-b934-c340d12ddc87.png)

Figure 2:  Clustering visualization

![image](https://user-images.githubusercontent.com/103223944/184576921-5166db48-762a-4ac6-a4a4-ebd88cd37b1b.png)

Figure 3:  Tradable cryptocurrencies

![image](https://user-images.githubusercontent.com/103223944/184576786-c2391a58-18de-4e4e-8a9d-9d15c8f61007.png)
 
Figure 4:  TotalCoinSupply vs. TotalCoinsMinded



