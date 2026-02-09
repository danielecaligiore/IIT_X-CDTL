# Importance Inversion Transfer (IIT) and X-CDTL Framework

This repository contains the official Python implementation of the **Explainable Cross-Domain Transfer Learning (X-CDTL)** framework and the **Importance Inversion Transfer (IIT)** mechanism.

This code supports the paper: 
> **"Importance Inversion Transfer reveals universal topological principles for cross-domain learning"** 
> *Daniele Caligiore (CNR, Italy), 2026.*

## 1. Overview
The X-CDTL framework identifies universal structural patterns (structural anchors) that allow knowledge transfer between very different scientific domains, such as social networks, molecules, proteins, and language. 

The core innovation is the **IIT mechanism**, which uses Explainable AI to find the most stable features for transferring information, even when data is scarce or noisy.

## 2. Repository Structure
The analysis is divided into 5 sequential Jupyter Notebooks:

*   **Module 1**: Data loading, feature extraction, and identification of the universal **Structural Anchors** using the IIT score.
*   **Module 2**: Visualization of how the topological features are distributed across the four domains (Boxplots).
*   **Module 3**: The actual Transfer Learning experiments. It uses GPU acceleration to align different domains and detect anomalies.
*   **Module 4**: Predictive validation. It generates the regression plots showing how well our IIT score predicts the real transfer performance.
*   **Module 5**: Final statistical analysis and performance curves under different levels of noise and data scarcity.

## 3. How to use this code
1.  **Requirements**: You need Python installed. We recommend using a virtual environment.
2.  **Install Libraries**: Run the following command in your terminal to install all necessary tools (PyTorch, NetworkX, Scikit-learn, etc.):
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the Notebooks**: Open the notebooks in order (from 1 to 5) to reproduce the results and figures presented in the paper.

## 4. Hardware
All experiments were tested using:
- **CPU**: Standard workstation.
- **GPU**: NVIDIA RTX 4090 / A100 (for fast manifold alignment and model training).

## 5. Data Availability
This code uses public datasets:
- **Social**: Facebook ego-networks (SNAP).
- **Molecular**: QM9 dataset.
- **Proteins**: PROTEINS dataset (TUDataset).
- **Linguistic**: Brown Corpus (NLTK).

## 6. Contact
**Daniele Caligiore**  
National Research Council of Italy (CNR)  
Email: daniele.caligiore@istc.cnr.it