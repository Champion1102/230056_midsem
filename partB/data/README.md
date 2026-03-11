# Dataset Information

## Datasets Used

### 1. Two Moons Dataset (Primary Toy Dataset)
- **Source**: Generated using `sklearn.datasets.make_moons`
- **Size**: 1000 samples, 2 features
- **Type**: Binary classification
- **Usage**: Used for reproduction (Task 2) and ablation studies (Task 3)
- **Why chosen**: Classic semi-supervised learning benchmark with non-linear decision boundary; same type as used in the paper (2-moon dataset in Table 1)

### 2. Digits Dataset (Supplementary)
- **Source**: `sklearn.datasets.load_digits`
- **Size**: 1797 samples, 64 features
- **Type**: Multi-class classification (10 classes, subsets used)
- **Usage**: Used in ablation study and failure mode analysis
- **Why chosen**: Similar to USPS digits dataset used in the paper; allows testing multi-class scenarios

## How to Load

All datasets are loaded directly via scikit-learn within the notebooks. No manual download or external files are required.

```python
from sklearn.datasets import make_moons, load_digits
```

## Preprocessing

- Features are standardized using StandardScaler where applicable
- For semi-supervised setup: only a small fraction of labels are kept; remaining labels are masked (-1)
- Random seeds are set for reproducibility
