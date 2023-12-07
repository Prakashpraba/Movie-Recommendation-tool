# 🎭🎬  Movie-Recommendation-tool
uses a predefined dataset of Amazon prime movie title and genres to recommend movies of similar genres using K-means algorithm
# ✏️ Goals
To develop a movie and TV Show recommendation function, the user has the need to search for a movie or TV Show based on its name and receive recommendations and be able to choose the amount of recommendations.
# 🌳Environments
In this project I used:

* Pandas: To be able to analyze my dataset and also be able to manipulate .
* Numpy: To use some array resources.
* Sk-Learn: To take advantage of the K-Means algorithm and be able to apply it to this project.
* Yellowbrick: To use your visualization tool and apply in K-Means analysis.
* Dataset: I used the dataset from "Amazon Prime Movies and TV Shows". Where I found it on the Kaggle platform.
* GPU: I had to use the GPU t4 x2 option, due to the need for high processing.
# 💪 Elbow method
This method aims to determine a numerical value for the clusters. If we need to have a grouping of 3 clusters, 4 clusters, 30 clusters and so on. Well here, as I want to have more ideal clusters for my set of "group_dummies", I'm going to play very high values to know what the ideal value for K is. Here you won't see all the plots I made to evaluate. I will present what was chosen and what I evaluated best. But you can check it out in the link that I'll leave there at the end for you to view in the repository.

Well for this evaluation I used a very good Python library called Yellowbrick, this library has several features. One of them is for "Elbow method".

It has three types of metrics for evaluation as shown in the documentation:

* distortion: mean sum of squared distances to centers

* silhouette: mean ratio of intra-cluster and nearest-cluster distance

* calinski_harabasz: ratio of within to between cluster dispersion

Of all the ones I tested, the one that pleased the most and brought the best number of "K", was that it is already the default for the "distortion" function.
# 🎭🎬 Recommend movies and TV shows
. Now with the whole set ready, let's create the function that will receive the client's data. Notice in the function that I input the prepared data set. It wouldn't be necessary to be like this, because in a possible situation this set would not be with the client, I added it so you can understand the context of the steps that are passed. I used the dataclass to simulate a situation of a request, where JSON will be received. Which is pretty much like a Python dictionary. But as the focus here is not on creating an API, using the requests library. It was that simple.

The "QueryRecommends" class has the following data:

* *dataset*: The data we have from movies and TV Shows
* *name*: The name of the movie that the user will choose
* *top_n*: The amount of results, whether the client wants top 10 movies or top 20.

Now entering the function, I do an internal search of the data set by performing a filter between the title and the name of the movie that the customer chose. Then I transform the text so that we don't have a problem with the client entering, this point can be better worked on. But as we are testing this functionality, it was pleasant that way. Then I restart my index, because the filter result will come with the index of the input set. Then I use the "at" method to capture the value of my "clusters_genre" column, which I will then perform a new filter from that result to obtain other similar values, then I choose the output columns that are "title " and "gender_type" and then the number of outputs you want.
- - - -
