# 🎭🎬  Movie-Recommendation-tool
uses a predefined dataset of Amazon prime movie title and genres to recommend movies of similar genres using K-means algorithm
# ✏️ Goals
To develop a movie and TV Show recommendation function, the user has the need to search for a movie or TV Show based on its name and receive recommendations and be able to choose the amount of recommendations.
# 🌳Environments
In this project I used:

Pandas: To be able to analyze my dataset and also be able to manipulate .
Numpy: To use some array resources.
Sk-Learn: To take advantage of the K-Means algorithm and be able to apply it to this project.
Yellowbrick: To use your visualization tool and apply in K-Means analysis.
Dataset: I used the dataset from "Amazon Prime Movies and TV Shows". Where I found it on the Kaggle platform.
GPU: I had to use the GPU t4 x2 option, due to the need for high processing.
# 💪 Elbow method
This method aims to determine a numerical value for the clusters. If we need to have a grouping of 3 clusters, 4 clusters, 30 clusters and so on. Well here, as I want to have more ideal clusters for my set of "group_dummies", I'm going to play very high values to know what the ideal value for K is. Here you won't see all the plots I made to evaluate. I will present what was chosen and what I evaluated best. But you can check it out in the link that I'll leave there at the end for you to view in the repository.

Well for this evaluation I used a very good Python library called Yellowbrick, this library has several features. One of them is for "Elbow method".

It has three types of metrics for evaluation as shown in the documentation:

distortion: mean sum of squared distances to centers

silhouette: mean ratio of intra-cluster and nearest-cluster distance

calinski_harabasz: ratio of within to between cluster dispersion

Of all the ones I tested, the one that pleased the most and brought the best number of "K", was that it is already the default for the "distortion" function.
