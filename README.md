# Uncovering Musical Topology: A Content-Based Recommendation Engine using Deep Autoencoders

**Author:** Elijah Konkle  
**Institution:** Belmont University, Data Science  

## Overview
Standard streaming algorithms rely heavily on collaborative filtering, creating popularity bias and echo chambers. By recommending what other users listen to, the DNA of the actual audio is often ignored. The objective of this project is to build a content-based recommendation engine that isolates the mathematical DNA of music using deep learning. This architecture allows for accurate similarity matching without relying on user history.

## Methodology
The development of this recommendation engine followed a mathematical pipeline:
* **Data Ingestion:** Processed over 100,000 tracks utilizing RapidAPI and Kaggle datasets.
* **Feature Engineering:** Extracted dense audio features and engineered custom evaluation metrics, specifically the `energy_valence_ratio`.
* **Dimensionality Reduction:** Built a multi-layer Deep Autoencoder using PyTorch to compress the dataset into a non-linear latent space.
* **Architectural Evaluation:** Mathematically determined the optimal number of K-Means clusters (k=5) using Silhouette and Elbow optimization. These validation metrics proved that the Deep Autoencoder significantly outperformed a linear Principal Component Analysis baseline.
* **Recommendation Deployment:** Calculated a global user taste centroid to deploy Cosine Similarity within the continuous latent space, successfully returning mathematically matched recommendations.

## Key Findings
* **Deep Learning Victory:** The multi-layer Deep Autoencoder outperformed the PCA baseline, achieving a superior Silhouette Score of 0.277 versus 0.166. The neural network successfully mapped complex, non-linear audio relationships that linear compression failed to capture.
* **Topographical Discovery:** While K-Means was strictly used as a proxy evaluation metric, it proved that the dataset naturally organizes into exactly five distinct musical super-clusters.
* **Global Profile Matching:** Calculating a singular user centroid successfully mapped a listener's average taste profile directly into the continuous latent space. This generated high-similarity track recommendations based purely on mathematical audio features.

## Recommended Songs
The first two songs in the playlist are the songs that created my centroid. The next 5 songs are my favorite songs that I was recommended.
Click [here](https://open.spotify.com/playlist/1wo4f1Ujmn7rzAuC7pnsgt?si=4f4070ebd0144c8d) to go to the playlist.

## Points
Neural Net: 1.5
Online Database / API Query code: 0.5
PCA: 1
tSNE / UMAP: 1
