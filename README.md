# Depth Analysis in Graph Convolutional Networks

## Overview

This project investigates how increasing depth affects performance and representation structure in Graph Convolutional Networks (GCNs). The primary objective is to empirically examine representation dynamics and assess whether oversmoothing emerges as depth increases.

The study evaluates GCN architectures ranging from 2 to 10 layers and analyzes both performance metrics and embedding geometry.

---

## Research Question

Does increasing depth in GCNs necessarily lead to representation collapse (oversmoothing), or does depth interact with dataset structure and optimization dynamics in more nuanced ways?

---

## Methodology

**Dataset**
- MUTAG (graph classification benchmark)

**Architectures Evaluated**
- 2-layer GCN
- 4-layer GCN
- 6-layer GCN
- 8-layer GCN
- 10-layer GCN

**Evaluation Metrics**
- Test Accuracy
- Embedding Variance (dispersion across feature dimensions)
- Average Pairwise Cosine Similarity
- PCA-based embedding visualization

All models were trained under consistent settings to ensure controlled comparison across depths.

---

## Key Observations

- Performance does not degrade monotonically with depth.
- Embedding variance fluctuates rather than consistently decreasing.
- Cosine similarity does not uniformly increase as depth grows.
- Representation dynamics appear conditional rather than purely depth-driven.

These findings suggest that oversmoothing is not an inevitable or strictly monotonic consequence of increasing depth in small-scale graph classification settings. Instead, representation behavior reflects an interaction between structural mixing, feature transformation, and dataset characteristics.

---

## Tools and Frameworks

- PyTorch
- PyTorch Geometric
- scikit-learn
- NumPy
- Matplotlib

---

## Reproducibility

To run the experiment locally:

```bash
pip install -r requirements.txt
```
Then execute:
gcn_depth_experiment.ipynb

---
## Author

Yash Solanki
