# CryptoClustering
Module 19

![image](https://github.com/user-attachments/assets/ca582456-e78b-4856-8075-37bcbbfcf385)


# CryptoClustering

Using Python and unsupervised machine learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

# Prepare the Data

Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.


## Overview of the Analysis

In this repository you will find how an unsupervised learning Machine Learning model was applied to cluster cryptocurrencies. The purpose of the analysis was to find the best way to cluster such currencies and to evaluate how inertia and the number of features affect the analysis.

The data were prepared for the analysis, and the following method was run twice:

Creating a Pandas DataFrame with the data to be analysed, finding the best value for 'k', clustering the cryptocurrencies with the K-means component of Sci-kit Learn, and plotting the results with hvPlot.
It was run twice because two different datasets were used: first, the original dataset, and second, the same dataset, but optimised with a principal compenent analysis (PCA).

# Description
Part 1
  - Scale the given cryptocurrency dataset with StandardScaler
  - Find the best value for k (number of clusters) using the elbow method (Best value found: k=4)

    <img width="368" alt="image" src="https://github.com/user-attachments/assets/c6d936e0-266a-4fc0-94dc-775ee4e614c4">

  - Use KMeans to cluster the scaled data (with the optimum k value found in the previous step)

    <img width="367" alt="image" src="https://github.com/user-attachments/assets/1aaa0fb1-1acd-450b-b303-703c09a59210">

Part 2
  - Use PCA to turn the original scaled dataset into a new DataFrame with 3 components
  - Find the best value for k (number of clusters) using the elbow method (Best value found: k=4)

     <img width="367" alt="image" src="https://github.com/user-attachments/assets/56769152-af32-47c3-a686-0a4a9a696af7">

  - Use KMeans to cluster the scaled data (with the optimum k value found in the previous step)

     <img width="355" alt="image" src="https://github.com/user-attachments/assets/ab100eb7-dada-4b0f-8bb2-7d79e6eed1fc">

 
# Q&As
As you will see in the Jupyter Notebook within this repository, the following 5 questions were answered as the analysis was conducted:

 1. What is the best value for k?
    Answer: Based on the elbow curve graph, k=4 seems to be the best choice to start the analysis.
 2. What is the total explained variance of the three principal components?
    Answer: 89.4% is the total explained variance using just these 3 components. i.e., We dropped 10.6% of the variability by dropping 4 of the 7 components.
 3. What is the best value for k when using the PCA data?
    Answer: 4
 4. Does it differ from the best k value found using the original data?
    Answer: Both data show 4
 5. What is the impact of using fewer features to cluster the data using K-Means?
    Answer: The inertia decreased and the data points seem to be less dispersed. Having fewer features to cluster the data seems to reduce ambiguity, which leads to a better interpretation of the results. The best value for k is the same in both cases. The impact of using fewer features to cluster the data produces tighter clusters.



