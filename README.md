# GraphEmbeddingComparison

# Repository Overview
This repository contains code for evaluating and comparing graph embeddings and clustering techniques on various benchmark datasets. The primary focus is on understanding the effectiveness of different embedding methods and how edge weighting schemes influence clustering performance. The analysis is conducted through two main scripts:

## Comparison 1: Graph Embeddings and Clustering
# Objective:
This script aims to evaluate and compare different graph embedding methods and their combinations for clustering nodes in graph datasets. The primary goal is to understand how well various embeddings can represent nodes in a way that facilitates effective clustering.

Description:

Dataset Preparation:

The script loads several benchmark graph datasets:
Karate Club (karate_club_graph from NetworkX)
Dolphin Network (soc-dolphins.txt)
American Football (American_football.txt)
Book Crossing (book.txt)
Graph Representation:

For each dataset, the script constructs the graph's adjacency matrix and computes node positions using the spring layout.
Embedding Methods:

The following embedding methods are utilized:
Node2Vec: Uses random walks and Skip-gram model to create node embeddings.
HOPE: Generates embeddings using High-Order Proximity Embedding through matrix factorization.
SDNE: Employs a neural autoencoder to learn embeddings that capture local and global structures.
Embedding Combinations:

Various combinations of embeddings are tested, including:
Additive
Multiplicative
Minimum
Maximum
Clustering:

K-means clustering is applied to each type of embedding and combination. The performance is assessed based on modularity.
Results:

For each dataset, the script records:
Best cluster labels
Modularity of clusters
Performance metrics of clustering

Comparison 2: Extended Graph Embeddings with Similarity Measures
Objective:
This script extends the analysis by incorporating edge weighting schemes based on similarity measures. It aims to investigate how these similarity measures impact the quality of embeddings and clustering outcomes.

Description:

Dataset Preparation:

Same datasets as Comparison 1 are used.
Similarity Measures:

The following similarity measures are used to weight the edges:
Jaccard Coefficient: Computes similarity based on node neighbors.
Adamic-Adar Index: Uses node degree information for edge weighting.
Preferential Attachment: Weights edges based on the product of node degrees.
Embedding Methods:

Embeddings are recalculated using:
Node2Vec: With weighted edges
HOPE
SDNE
Various combinations of these embeddings
Clustering:

K-means clustering is applied to the embeddings generated from weighted graphs. Clustering performance is evaluated similarly to Code 1.
Results:

For each dataset and similarity measure, the script records:
Best cluster labels
Modularity of clusters
Performance metrics of clustering
