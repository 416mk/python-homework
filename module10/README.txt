MICK CHARBONNEAU-DINELLE
11/1/2023
MODULE 10 APPLICATION

SOURCES USED FOR CODING: MODULE6-7 FROM UTOR, BLACKBOX.IO AND CHATGPT-3.5
DID NOT COPY WORD FOR WORD ANY CODE JUST INSPIRED MYSELF WITH PASS WORK AND HAD GPT AND BLACKBOX PROBLEM SOLVE AND FIX SYNTAX ISSUES.

Module-10-Challenge
In this repository you will find a .ipynb file named Crypto Investments, in this file we assume the role of an advisor in one of the top five financial advisory firms in the world. The firm wants to assemble investment portfolios that are based on cryptocurrencies. Instead of basing my proposal on only returns and volatility, the board wants to include other factors that might impact the crypto market—leading to better performance of myy portfolio. My job is to create a prototype for submitting a crypto portfolio proposal to the company board of directors.

Part 1 Find the Best Value for k by Using the Original Data
We will use the elbow method to find the best value for k by using the original data. We will then code the elbow method algorithm to find the best value for k, using a range from 1 to 11. We will then plot a line chart of all the inertia values computed with the different values of k. Lastly answer the following question: What’s the best value for k?

Part 2 Cluster the Cryptocurrencies with K-Means by Using the Original Data
We will use the K-means algorithm along with the best value for k that we found by using the original data. We will then use them to cluster the cryptocurrencies according to the provided price changes of the cryptocurrencies. We will then initialize the K-means model with four clusters by using the best value for k. We will fit the K-means model by using the original data. We will predict the clusters for grouping the cryptocurrencies by using the original data. We will then create a copy of the original data, and then add a new column of the predicted clusters. Lastly we will create a scatter plot by using K-means and add the crypto names to identify the cryptocurrency that each data point represents.

Part 3 Optimize the Clusters with Principal Component Analysis
In this part we will perform PCA analysis and reduce the features to three principal components. We will then be able to obtain the explained variance to determine how much information can be attributed to each principal component. Lastly answer the following question: What’s the total explained variance of the three principal components?

Part 4 Find the Best Value for k by Using the PCA Data
Well start off by using the elbow method to find the best value for k by using the PCA data. We will code the elbow method algorithm, and use the PCA data to find the best value for k, using a range from 1 to 11. We will then visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. Lastly Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found when using the original data?

Part 5 Cluster the Cryptocurrencies with K-means by Using the PCA Data
In this section we will use the PCA data, the K-means algorithm, and the best value for k that we found using the PCA data. Specifically, we’ll use them to cluster the cryptocurrencies according to the principal components. Firstly we initialize the K-means model with four clusters by using the best value for k. Fit the K-means model by using the PCA data. Predict the clusters for grouping the cryptocurrencies by using the PCA data. Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters. Create a scatter plot with the labels that we found by using K-means. Then add the crypto names to identify the cryptocurrency that each data point represents.

Part 6 Visualize and Compare the Results
In this last part we will visually analyse the cluster analysis results by observing the outcome both with and without the use of optimisation techniques. We will create a composite plot to compare the elbow curve that we created from the original data with the one that we created from the PCA data. We will also create a composite plot to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data. Lastly answer the following question: Based on visually analysing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?

End of Module 10