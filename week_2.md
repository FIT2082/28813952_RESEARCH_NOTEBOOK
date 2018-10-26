# Week 2

The two main tasks for this week were beginning a literature review into current dimensionality reduction techniques for high dimensional data, and to have the Microscopium program running on a new dataset on my personal laptop. 
The literature review covered mainly the three following dimensionality reduction rechniques: Principal Component Analysis (PCA), t-Distributed Stochastic Neighbour Embedding (t-SNE), and Uniform Manifold Approximation and Projection.
Dimensionality reduction is important because:
    - It finds latent features in your data
    - often, "A lot of dimensionality is redundant"
    - It helps visualise data (2 or 3 dimentions can be easiy interpreted by a human)
As it stands, there are two main methods for dimensionality reduction:
    - Matrix Factorisation (PCA, NonNegative matrix Factorisation)
    - Neighbour Graphs (Laplacian Eigenmaps, t-SNE, UMAP)

PCA is the prototypical matrix factorisation method, and t-SNE is considered the current gold standard for the neighbour graph method. UMAP is a relatively new method but is quickly gaining note due to its strong grounding in mathematics to justify results, as well as its superior performance to t-SNE.

The Microscopium software is written in python3 and relies heavily on a number of packages for pre-processing, analysis and visualisation.
In order to have the Microscopium software visualising the our data, the data must first go through a series of pre-preocessing steps. These steps are simiar for all high content screening data, but vary in key areas depending on the subject of an image. For example, a biologist may want to screen cells, wheres a physicist may want to screen non-organic materials, perhaps light. For this reason, the pre processing step is difficult to entirely automate, and has been informed by the expert knowlege of Juan and Genevieve.
We will be using the Broad Bioimage Benchmark Collection (BBBC) BBBC021 HCS dataset to test the Microscopium app on our personal devices.
The dataset can be found at: https://data.broadinstitute.org/bbbc/BBBC021/
