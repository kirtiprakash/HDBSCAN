# HDBSCAN
A MATLAB implementation of the Hierarchical Density-based Clustering for Applications with Noise, ([HDBSCAN](http://joss.theoj.org/papers/b5c5dd4b7491890b711c06225dcc9649)), clustering algorithm. 

The HDBSCAN algorithm creates a nested hierarchy of density-based clusters, discovered in a non-parametric way from the input data. The hierarchies are akin to Single Linkage Clustering, however 
in HDBSCAN, an optimal clustering scheme is automatically inferred from the cluster hierarchy. The optimal clustering is analogous to a single run of the DBSCAN algorithm, but with possibly varying 
epsilon-values (see the role of epsilon in DBSCAN) for any given branch of the hierarchy. Thus, information from local neighborhoods is used to optimally cut the hierarchy at varying levels.

This MATLAB implementation of the HDBSCAN algorithm was created with peformance in mind, and is inspired by the excellent [python version](http://hdbscan.readthedocs.io/en/latest/). While this version is not as fast as the python implementation (in which highly optimized C code was compiled for iterating through the hierarchy), it is currently the fastest (and only?) available MATLAB implementation and is written in pure MATLAB code, meaning there is no dependency on compilation or external packages. 

See the [docs](docs) for interfacing and running HDBSCAN with your own data.

## Dependencies
- MATLAB version r2015a or greater

## References
- Campello et al. (2013): Density-Based Clustering Based on Hierarchical Density Estimates.
- Campello et al. (2015): Hierarchical density estimates for data clustering, visualization, and outlier detection  
