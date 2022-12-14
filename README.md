# Cryptocurrencies

## Overview of the Project

* We are creating an analysis for our clients who are preparing to get into the cryptocurrency market.

* Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked us to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

* The data we will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what we are looking for, we have decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm. We’ll use data visualizations to share our findings with the board.

## Results

### 1: Preprocessing the Data for PCA.

First we’ll preprocess the dataset in order to perform PCA.

The data is setup for the unsupervised learning model:

A. Unnecessary columns are removed. Null values are handled.

B. Only numerical data is input to the model.

C. Values are scaled.

### 2: Reducing Data Dimensions Using PCA(Principle Component Analysis).

PCA is a statistical technique to speed up machine learning algorithms when the number of input features is too high.

Using PCA, we’ll reduce the dimensions of the clean and scaled DataFrame to three principal components and place these dimensions in a new DataFrame.

![image](https://user-images.githubusercontent.com/111020934/207523767-f1a0e8a8-919d-407e-aeb4-6d16651aaac2.png)

### 3: Clustering Cryptocurrencies Using K-means.

Using K-means algorithm, we’ll create an elbow curve using hvPlot to find the best value for K from the DataFrame created in Deliverable 2. Then, we’ll run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

Clustering is a type of unsupervised learning that groups data points together. This group is called a cluster. The most popular way to cluster is by using K-Means algorithm. 

This algorithm groups data into K clusters. K is the number of cluster.

The easy method for determining the number of K is the elbow curve. For an elbow curve we'll plot the number of clusters on the x-axis and inertia values on the y-axis.

![image](https://user-images.githubusercontent.com/111020934/207525373-260275c9-5411-42f0-9f79-a10519350421.png)

We run K-Means algorithm with k=4. Then create a new DataFrame including predicted clusters and cryptocurrencies features.

![image](https://user-images.githubusercontent.com/111020934/207525944-92f94996-a4fa-4465-8889-66eeae8e776a.png)

### 4: Visualizing Cryptocurrencies Results.

We create scatter plots with Plotly Express and hvplot and visualize the distinct groups that correspond to the three principal components we created in Deliverable 2, then we’ll create a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

Creating a 3D-Scatter with the PCA data and the clusters:

![image](https://user-images.githubusercontent.com/111020934/207526472-0f4a8bfc-77ac-4ec0-b429-b9c16df4bc29.png)


Creating a table with tradable cryptocurrencies:

![image](https://user-images.githubusercontent.com/111020934/207526629-0a8d7875-c483-4087-86b6-fcc450763714.png)

Creating the 2D scatter plot with tradable cryptocurrencies:

![image](https://user-images.githubusercontent.com/111020934/207527042-7544ffef-4481-4b13-aa86-88e272168aa8.png)

## Summary 

All the tradable cryptocurrencies on the trading market could be best grouped into 4 classes or clusters to create a classification system for this new investment.







