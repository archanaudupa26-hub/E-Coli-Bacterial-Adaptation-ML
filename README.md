# Predicting Bacterial Adaptation Signalling Networks via Machine Learning and Genomic Topology Analysis

## Project Overview
This study implements an integrated bioinformatics and machine learning pipeline to resolve high-dimensional transcriptomic noise and identify key regulatory drivers governing bacterial stress adaptation in *Escherichia coli*. 

Utilizing transcriptomic metadata from the NCBI Gene Expression Omnibus (GEO) across multiple environmental stress conditions (oxidative stress, nitrosative stress, heat shock, cold shock, and antibiotic exposure), Differentially Expressed Genes (DEGs) were systematically analyzed.

## Performance Highlights
* **Top Performer:** An optimized **Random Forest Regression** model deployed within Google Colab outperformed baseline architectures.
* **Accuracy:** Achieved a verification **R² score exceeding 0.84**, successfully compressing the input search space down to the top 50 high-impact driver genes.
* **Downstream Discovery:** Network topology analysis using the STRING database and Cytoscape isolated a central functional cluster of the top 10 most highly connected hub genes (*cheW, cheZ, cheB, ycgR, motA, motB, fliT, yhjH, ycfJ, and ygaC*).

## Project Structure
* `E. Coli adaptation ML pipeline.ipynb`: Complete Python data pipeline containing preprocessing, Random Forest training, and benchmarking baselines.
* `Cytoscape session.cys`: Fully interactive network session containing localized structural graph layouts and node-edge connectivity maps.

## Key Network Visualization
Below is the isolated central functional hub network displaying prominent interactive density concentrated inside specific gene sub-families:

![Top 10 Hub Networks](networks%20of%20hub%20top%2010.png)

## Workspace & Environment Configuration
* **Language:** Python 3.10
* **Core Libraries:** NumPy (v1.25.2), Pandas (v2.0.3), Scikit-learn (v1.2.2), SciPy (v1.11.2)
* **Graph Analysis Software:** Cytoscape (NetworkAnalyzer plugin), ShinyGO API
