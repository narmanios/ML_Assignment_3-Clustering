# Overview of ML Assignment 3, Option 2

## Assignment Description

KMeans was used [KMeans](http://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) to cluster a set of images **based on their metadata.** The measure of success was subjective; the right features and number of clusters used was decided upon when viewing the images in each cluster and determining whether they "seemed" to belong together.

### The Images

These images represent more than 400 works of fine art from museum collections and galleries across several countries, curated and analyzed for inspiration and information on effective ways to visually communicate uncertainty, ambiguity, and vulnerability. The selected artworks were chosen for their unique ability to convey ***uncertainty*** using a range of approaches and techniques. The images were used to inspire better design of visual representations of uncertainty in data, as [traditional methods and techniques were not working very well](https://hbr.org/2016/11/why-its-so-hard-for-us-to-visualize-uncertainty).


#### Detailed Code Explanation

The provided code snippet demonstrates how the KMeans clustering was implemented to organize a set of images based on selected metadata features. Here is a detailed breakdown of each component of the code:

```python
# Subset of metadata features used for clustering
X = data[['primary_medium', 'representation', 'representation_semi', 'spatial_dimension']]

## Description

This line defines the subset of features from the dataset that are used for clustering. X is assigned a DataFrame consisting of four columns:

# primary_medium: This could refer to the material or technique used in the artworks.
# representation: Likely indicates the style or genre of the artwork.
# representation_semi: Could denote a more detailed classification within the broader representation category.
# spatial_dimension: Pertains to the dimensions or scale which might affect the perception of the artwork.

These features are presumably pivotal in influencing how artworks are grouped together, reflecting similarities in material, style, and scale.

#### Code Explanation

Included in the provided code snippet:

# The number of clusters in the final model was set to 22
my_n_clusters = 22

# Looping through each cluster to display a limited number of image thumbnails
for i in range(0, max(km.labels_)+1):
    # Code omitted for brevity. This part initialized the cluster display and set a limit for images displayed per cluster.
