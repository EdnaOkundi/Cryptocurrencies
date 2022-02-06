# Cryptocurrencies

Overview:
In this challenge, I was to create an analysis for clients who are preparing to get into the cryptocurrency market. 
The analysis includes cryptocurrencies on the trading market and how they could be grouped to create a classification system. 
To reduce overfitting, I used Principal Component Analysis (PCA).
The following deliverables were to be met and the results are based one each delivarable:

1. Preprocessing the Data for PCA
2. Reducing Data Dimensions Using PCA
3. Clustering Cryptocurrencies Using K-means
4. Visualizing Cryptocurrencies Results.

Results:

1.Preprocessing the Data for PCA
I loaded the dataset from the source file and did transformations to prepare the data for PCA.
Used pandas to reduce dataset to enable it be used for machine learning. I filtered dataset by removing 
all currencies that are not trading, removing all currencies with no mined coins, 
and any records with null values. Dataset also reduced to four fields of algorithm type, proof type, 
total coins mined and total coin supply.I then made necessary transformations to prepare remaining data into scaled data.

2.Principle Component Analysis
I used SKLearn to reduce the scaled data to three components for three dimensional modeling.

3.Clustering Cryptocurrencies using K-Means.
I used SKLearn Kmeans to produce an elbow curve that shows the value of '5' will serve best as the K value in the KMeans model.
Created and ran the KMeans function on the scaled and transformed data to generate a class of five clusters. And, 
created a combined dataset of the original filtered data with the scaled data and the cluster class values for visualization purposes.

4.Visualizations
A three dimensional Plotly Express scatter plot showing the clusters with markers identifying Coin name and Algorithm.
An hvplot table containing Coin Name, Algorithm, ProofType, Total Coin Supply and class. 
This data set can be used for additional analysis and visualizations by the five clusters.
A scatter plot using hv.plot presenting total coins mined and total coins supplied was created.

Conclusions
Bitcoin is in a class by itself. This is obvious in both the three dimensional cluster modeling and the scatterplot. 
This is obviously useful as Bitcoin can be studied as an exemplar.
It would be very instrumental to run this analysis again without the Bitcoin data, so see if the elbow curve finds 
a different optimal cluster value and so that we can see the distribution of the data better in the three dimensional plot. 
Essentially there are two classes, Bitcoin and all others. We can use these findings to compare all cryptocurrencies against Bitcoin, 
and to re-run the unsupervised machine learning without Bitcoin to more fully understand the rest o