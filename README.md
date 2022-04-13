# K-means-Clustring
Logistic Regression Model of Wine Quality Dataset

• About the model:
The model in this assignment is k-means clustering model that aims to separate groups with similar traits
and assign them into k clusters in which each observation belongs to the cluster with the nearest mean.
The model will divide the different features that affect the ALSFRS slope, and the reason of dividing
them is to understand what patient phenotypes can be surly specified and used to predict the future
changes of the ALSFRS slope.

• Dataset:
This dataset is clinical dataset that has many clinically observation changes that has correlation
coefficients with ALSFRS slope. This dataset has 2223 rows and 101 columns. The source of this data is
DREAM-Phil Bowen ALS Prediction Prize4Life Challenge data, most of which are from the Pooled
Resource Open-Access ALS Clinical Trials Database (PRO-ACT) archive.

• Data pre-processing:
Before starting to work on the model, we must make sure that data is clean. The dataset is clean, so we
need to explore and analyze the data for better understanding. As we can see in figure 1 all data types in
this dataset are numerical which is useful because we will not need to any transformation of categorical
data. I wanted to discover data statistically. Notice that the range of some columns is too
high which means that we will need to normalize them before starting to work on the model.

Also, I wanted to check which features has strongest bond with ALSFRS slope. ALSFRS slope has strong correlation with ALSFRS total min.
Trunck min, mouth min, and hands min also has a good degree of correlation with ALSFRS slope. Notice that trunk range and ALSFRS total
range has almost no correlation with ALSFRS slope.

• Data visualizations:
Following up on data exploring data, we need to visualize data to better analyzing. I wanted
to explore the age range of patients with the ALSFRS slope. Notice that range of patients is between 20
and 80. Most patients has ALSFRS slope between 0.5 and -2. Also, no patients under 30 have ALSFRS
slope between -4 and -3 or between 0.5 and 1.

The relationship between Trunk min and ALSFRS slope. I chose to visualize them
because of the strong relations between them that we notice during exploring data. Notice that with
increasing the trunk min the ALSFRS slope is also increased. Also, the trunk min values that between 0
and 4 has ALSFRS slope range from 0-4.8 to 1.2. However, with increasing trunk min, we noticed that
ALSFRS slope range became smaller which is between 0.8 and -2.
Final step of exploring data is that before starting to work on the model I should drop columns that has no
effect on data such as ID and subject ID.

• Splitting the data:
Data was already splatted into training and testing. However, beside splitting data, we need to prepare
data for the clustering model. Because we found in exploring data that we have huge differences
between ranges of values, we need to normalize them. I have normalized data using
StandardScaler( ). Notice that range of data has been minimized.
One problem left before building the clustering model which is that we have many dimensions that will
be difficult to deal with. As a result, we need the PCA model that can help reducing the dimensionality
of datasets and increasing interpretability.

• Applying the model:
First of all, which k is best for this dataset is what I was wondering about. Using elbow method helps me
to decide that 4 and 3 clusters is the best for the k-means model of this dataset.
Finally, I built two models with k-means. One with 3 clusters and the other 4 clusters.

• Evaluation and test scores:
The visualization of the k-means clustering model, model seems
working good because that the data groups are divided appropriately. We can see that data apart from
each other and clearly distinguished. Based on elbow method, we are not quite sure if 4 or 3 clusters is
better, so we need Silhouette Score which is a metric used to calculate the goodness of a clustering
technique. The Silhouette Score of 4 clusters is 0.34 and 0.35 for the 3 clusters. Even though, it’s small
difference, 3 clusters model works better than 4 clusters model.
The other and common way to evaluate the data is using the testing dataset to test the work of the model.
I used the model with 3 clusters to predict the testing dataset

• Results:
The result of the model is good we can see that in (The visualization of the three-clustering
model with testing dataset). It is clear that results are similar to the visualization of the training model.
The visualization is apart, and the data groups are divided appropriately in the testing model.
Also, based on the elbow method and Silhouette Score “3 k-means” clustering is the best k clustering for
this dataset.

• Conclusion:
After making sure that data is clean, I explored the data, and I notice that data needs some preparation
before building the model. For example, the differences in the ranges of values are high, and the
dimensions of the data is also high. As a result, I have applied normalization and PCA model. Then I
built two k-means clustering model one with 3 clusters and the other with 4 clusters based on elbow
method results. I evaluated the model using the testing dataset, and the results were good based on the
visualization which shows that data are divided appropriately. However, I wasn’t quite sure which
model is better, so I used the Silhouette Score to evaluate the model. The results shows that 3 clusters
model in better than 4 clusters model, and the model works appropriately.
