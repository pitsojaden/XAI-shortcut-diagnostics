# Explainable AI Under Shortcut Learning

## Overview
This repository contains an experimental notebook investigating the behavior of post-hoc attribution methods under shortcut learning. Specifically, it examines the divergence between predictive reliance and attribution mass when models exploit spurious or non-causal features.

The primary goal is to assess the epistemic reliability of attribution-based explanations in controlled shortcut scenarios.

## Scope
The experiments focus on:
- Convolutional neural networks trained on synthetic or controlled image data
- Parametrized shortcut strength injected during training
- Evaluation of classification performance versus attribution behavior
- Grad-CAM-based regional attribution analysis

This repository is intended as a diagnostic study rather than a benchmarking leaderboard.

## Notebook Contents
The main notebook (`XAI.ipynb`) includes:
- Dataset generation or preprocessing
- Model training under varying shortcut conditions
- Attribution extraction using Grad-CAM
- Quantitative and qualitative analysis of attribution mass

## Key Questions
- Do attribution maps faithfully reflect causal feature usage?
- How does shortcut strength affect attribution reliability?
- Can high-confidence explanations be misleading under shortcut learning?

## Requirements
Typical dependencies include:
- Python 3.8+
- PyTorch
- Torchvision
- NumPy
- Matplotlib

Exact versions may be specified within the notebook.

## Usage
Open and run the notebook sequentially:
```bash
jupyter notebook XAI.ipynb
```

Ensure GPU support is enabled if available, as training is computationally non-trivial.

## Limitations
This study is intentionally constrained:
- Synthetic or simplified data
- Single-model architecture focus
- Post-hoc methods only

Results should be interpreted as diagnostic evidence, not universal guarantees.

## Citation
If this repository is used for academic work, please cite it appropriately or contact the author.
