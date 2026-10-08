# Lab 3: Clustering Analysis Using K-Means and K-Medoids Algorithms

## Purpose

The purpose of this lab is to apply and compare K-Means and K-Medoids clustering algorithms using the Wine dataset from the scikit-learn library. The dataset was standardized using z-score normalization before clustering so that differences in feature scales would not influence the clustering results.

Both algorithms were configured to create three clusters because the Wine dataset contains three known classes. Their performance was evaluated using the Silhouette Score and Adjusted Rand Index (ARI).

## Key Insights

K-Means produced stronger clustering results than K-Medoids on the standardized Wine dataset. K-Means achieved a Silhouette Score of 0.2849 and an Adjusted Rand Index of 0.8975, while K-Medoids achieved a Silhouette Score of 0.2676 and an Adjusted Rand Index of 0.7411.

These results show that K-Means produced slightly better-defined clusters and had a stronger agreement with the actual Wine class labels. The visualizations also showed that both algorithms identified three general groups, although their cluster centers and some cluster assignments differed.

## Challenges and Decisions

One important decision was to standardize all features before clustering because the Wine dataset contains features measured on different numerical scales.

A challenge occurred when using the scikit-learn-extra package for K-Medoids because of a compatibility issue with the installed Python libraries. To complete the lab, K-Medoids was implemented directly using pairwise distances and actual observations as medoids.

For the two-dimensional visualization, the first two standardized Wine features were used so that the K-Means and K-Medoids results could be compared consistently.