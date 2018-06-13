# Spark MLlib: Clustering Analysis of Chicago Crime Locations Dataset

Using as input data the crime of Chicago dataset, we have developed a Jupyter notebook that perform a clustering of the locations (latitude, longitude) after asking for the number of clusters and using two of the clustering algorithms in **SparkML**:
- Kmeans Model
- Bisection Kmeans Model

the Chicago Dataset can be located in: [data.cityofchicago.org](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2).

The results plot include a 2D chart the centroids and the points of each cluster. These information has been also plotted on top of a map of Chicago.


**Summary of results**

- Result Scores for Kmeans with k=6:

![results_scores](./pictures/image5_kmeans.JPG)

- Result Scores for bisection Kmeans with k=6:

![results_scores](./pictures/image4_bisection.JPG)

- Location of all the clusters by colors in a 2D Map with kmeans:

![results_scores](./pictures/image1.JPG)

- Location of all the clusters by colors in a chicago Map with kmeans(blue) and bisection(green):
The radious of the circle is scaled by size of the cluster

![results_scores](./pictures/image2.JPG)

- Location of all the clusters by colors in a chicago Map with kmeans(blue) and bisection(greens):
The radious of the circle is scaled by size of the cluster

![results_scores](./pictures/image3.JPG)

