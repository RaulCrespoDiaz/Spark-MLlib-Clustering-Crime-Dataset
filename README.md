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
The radious of the circle is scaled by size of the cluster with this function:

```python
#This function scale a point x in (in_min,in_max)-> y in (out_min,out_max))
#we will use this function to scale the radious with the list of predictions
def remap(x, in_min, in_max, out_min, out_max):
  return (x - in_min) * (out_max - out_min) / (in_max - in_min) + out_min
```

and called here:

```python
#Painting the markers and circles in the map
#for Kmeans clustering
i=0
for center in centers:
    folium.Marker(
        location = center,
        popup="Centroid:"+str(i),
        icon=folium.Icon(color='blue')).add_to(m)
    
    folium.Circle(
        radius=remap(list_prediction[i],in_min,in_max,out_min,out_max),
        location=center,
        color='#3186cc',
        fill=True,
        fill_color='#3186cc'
    ).add_to(m)
    
    i+=1
```




- Location of all the clusters by colors in a chicago Map with kmeans(blue) and bisection(greens):
The radious of the circle is scaled by size of the cluster

![results_scores](./pictures/image2.JPG)

![results_scores](./pictures/image3.JPG)

