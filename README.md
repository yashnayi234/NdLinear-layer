# NdLinear-layer

## NdLinear vs. Linear Layer - ML Ensemble Core

This project explores and compares performance between a traditional neural network model using `nn.Linear` and an enhanced variant using `NdLinear`. Built using the MNIST dataset, this notebook demonstrates model setup, training, and evaluation for multiple CNN configurations, including baseline and parameter-scaled variants.

## 📚 Overview

The notebook implements:
- Loading and preprocessing of the MNIST dataset.
- Two primary model types:
  - **Baseline CNN** using `nn.Linear`
  - **NdLinear CNN** replacing `nn.Linear` layers with `NdLinear`
- Experiments across models with different parameter scales (Base, 1M, 5M).
- Comparative analysis based on accuracy and training dynamics.

## 🛠️ Installation

Make sure the following libraries are installed:

```bash
pip install torch torchvision matplotlib
```
```bash
git clone https://github.com/ensemble-core/NdLinear.git
cd NdLinear
pip install . 
```

You may also need `NdLinear` module if it's custom or external.

## 🚀 Usage

Run the notebook step-by-step to:

1. **Load and preprocess** MNIST data.
2. **Define CNN architectures** using `nn.Conv2d` and either `nn.Linear` or `NdLinear`.
3. **Train** and evaluate models.
4. **Compare** performance metrics (accuracy, loss, parameters).

You can start with:

```python
# Load and preprocess
from torchvision import datasets, transforms
```

Then follow through the notebook cells to build and run experiments.

## 📊 Model Variants

| Model Version | Description                      | Approx. Parameters |
|---------------|----------------------------------|--------------------|
| Base Model    | CNN with standard layers         | ~XXX K             |
| 1M Model      | Enhanced with larger dense layers| ~1 Million         |
| 5M Model      | Further scaled dense layers      | ~5 Million         |

## 📈 Results

| Model Type     | Params     | Accuracy | GFLOPs | Memory (MB) |
|----------------|------------|----------|--------|-------------|
| Baseline Base  | 291,466    | 90.02%   | 6.49   | 1084.39     |
| NdLinear Base  | 136,648    | 87.64%   | 6.43   | 1084.39     |
| Baseline 1M    | 291,466    | 89.68%   | 6.49   | 1084.38     |
| NdLinear 1M    | 136,648    | 88.87%   | 6.43   | 1084.38     |
| Baseline 5M    | 7,090,314  | 90.45%   | 35.19  | 1206.98     |
| NdLinear 5M    | 798,900    | 88.23%   | 35.25  | 1206.98     |

---

## 📂 Files

- `NdLinear_ML-Ensemble-core.ipynb`: Main experiment notebook.
