# Building a Hierarchical Agglomerative Clustering(HAC) Model

## [Demo](https://nbviewer.org/github/tyrantdavis/Hierarchical-Clustering-Model/blob/main/hierarchical-clustering-moons.ipynb)

---

## Introduction
In an ongoing pursuit to identify logical data groupings through clustering techniques, a new unsupervised dataset characterized by well-defined separations has been acquired. Given the nature of this data, the conventional k-means clustering algorithm might not be the most suitable option. Therefore, a k-means model will be used to train  on this dataset and subsequently compare its outcomes with those generated by a hierarchical agglomerative clustering (HAC) model. The distinct methodology employed by the HAC model may prove to be more effective for this particular dataset. Furthermore, there will be an assessment aimed at determining the optimal number of clusters for the HAC model.


This examination will allow the clustering of moons.

This project will scope, analyze, prepare, plot data, and seek to explain the findings from the analysis.

**Feature Information**

- Col1—Unique identifier for each house sold.
- Col2—Date of the house's most recent sale.

  
Here are a couple of questions that this project seeks to answer:

- How does the k-means model separation support compare to the hierarchical agglomerative clustering (HAC) model?
- What is the termination point indicated by the cutoff line?
- What is the optimal number of clusters for the HAC model?



**Data Sources:**
- [Sklearn - Make Moons](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_moons.html)



## Project Goals
The objective is to categorize or cluster moons by analyzing the similarities in their characteristics.

#### Why use a k-means clustering algorithm?
K-means clustering is effective in various situations, but it is not universally applicable. Some datasets and analytical challenges may be better suited for hierarchical clustering techniques. The k-means algorithm struggles with overlapping data and is most effective with spherical distributions. When data does not conform to this shape, calculating centroids can be problematic, and the resulting clusters may fail to accurately represent similar data points, even as the means begin to converge. In essence, k-means clustering is less effective for circular or spiral data, which is distinctly separated, highlighting the advantages of hierarchical clustering methods.

As its name suggests, hierarchical clustering organizes data into a hierarchy of groups based on similarity. This method can be approached in two primary ways: hierarchical agglomerative clustering (HAC) and hierarchical divisive clustering (HDC). Only HAC will be addressed in this project. 

In HAC, each data point initially exists as an individual cluster, and the algorithm progressively merges the two closest clusters, continuing this process until a predetermined stopping point is reached. This "bottom-up" strategy effectively constructs a hierarchy of clusters, allowing for a more nuanced understanding of data relationships.


## Data
A dataset about moons that can be used to train the machine-learning model has been found. 


## Conclusions


- How does the k-means model separation support compare to the hierarchical agglomerative clustering (HAC) model?
  
    A k-means clustering model generated two separate clusters. However, these clusters do not seem to provide a clear distinction between the crescents, as they merely divide the entire feature space into two equal parts instead of effectively isolating the crescents.

    In contrast, a hierarchical agglomerative clustering (HAC) model was utilized to form two distinct clusters. This method appears to significantly improve the differentiation between the crescents, thereby enhancing the clarity of the separation among the identified groups.
  
- What is the cutoff and the optimal number of clusters for the HAC model?

    - According to the dendrogram, 3 clusters are optimal.
    - The 3-cluster model shows minimal differences when compared to the 2-cluster model.
