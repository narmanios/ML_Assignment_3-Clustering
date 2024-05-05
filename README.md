# Overview of ML Assignment 3, Option 2

## Assignment Description

[KMeans](http://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) was used to cluster a set of images **based on their metadata.** The success of the clustering was determined subjectively; the right features and number of clusters were decided upon by visually inspecting whether images in each cluster appeared to belong together. The optimal number of clusters, chosen based on the highest average silhouette score (0.9813282942974106), was 22.

### The Images

These images represent over 400 works of fine art from museum collections and galleries across several countries. They were curated and analyzed to provide inspiration on how to effectively communicate uncertainty, ambiguity, and vulnerability through visual representations. 
### Detailed Code Explanation

The provided code snippet outlines how the KMeans clustering was implemented to organize a set of images based on selected metadata features. Here is a detailed breakdown of each component of the code:

```python
# Subset of metadata features used for clustering
X = data[['primary_medium', 'representation', 'representation_semi', 'spatial_dimension']]

## Description:
# X is assigned a DataFrame consisting of four columns:
# - 'primary_medium': This could refer to the material or technique used in the artworks.
# - 'representation': Likely indicates the style or genre of the artwork.
# - 'representation_semi': Could denote a more detailed classification within the broader 'representation' category.
# - 'spatial_dimension': Pertains to the dimensions or scale which might affect the perception of the artwork.

These features are pivotal in influencing how artworks are grouped together, reflecting similarities in material, style, and scale.
