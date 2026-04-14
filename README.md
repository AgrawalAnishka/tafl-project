# tafl-project

This repository contains two projects:

1. **CFG → CNF & GNF Converter** — a browser-based tool (see `try2.html`)
2. **Machine Learning & Deep Learning Project** — a collection of Jupyter notebooks covering classical ML and DL algorithms using real Kaggle datasets (see `notebooks/`)

---

# Machine Learning & Deep Learning Project

A complete, hands-on ML/DL project demonstrating the most important algorithms and frameworks using real datasets sourced directly from Kaggle.

## Notebooks

| # | Notebook | Algorithm | Kaggle Dataset |
|---|---|---|---|
| 1 | `01_ml_libraries_intro.ipynb` | Libraries overview | Iris (built-in) |
| 2 | `02_linear_regression.ipynb` | Linear / Ridge / Lasso / ElasticNet / Polynomial | [House Prices](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) |
| 3 | `03_logistic_regression.ipynb` | Logistic Regression | [Heart Disease](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) |
| 4 | `04_deep_learning_frameworks.ipynb` | TensorFlow / Keras / PyTorch MLP & CNN | [Fashion-MNIST](https://www.kaggle.com/datasets/zalando-research/fashionmnist) |
| 5 | `05_decision_tree_brain_stroke.ipynb` | Decision Tree | [Stroke Prediction](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) |
| 6 | `06_naive_bayes.ipynb` | Gaussian / Multinomial / Bernoulli NB | [Heart Disease](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) + [SMS Spam](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) |
| 7 | `07_svm_brain_tumor.ipynb` | SVM (Linear / RBF / Poly / Sigmoid) | [Brain Tumor Features](https://www.kaggle.com/datasets/jakeshbohaju/brain-tumor) |

---

## Quick Start

### 1. Clone the repository

```bash
git clone https://github.com/AgrawalAnishka/tafl-project.git
cd tafl-project
```

### 2. Create a virtual environment and install dependencies

```bash
python -m venv venv
source venv/bin/activate          # Windows: venv\Scripts\activate
pip install numpy pandas matplotlib seaborn scikit-learn scipy \
            tensorflow torch torchvision xgboost jupyter kaggle
```

### 3. Set up Kaggle API

1. Go to https://www.kaggle.com/settings → **API** → **Create New Token**
2. Download `kaggle.json` and place it at `~/.kaggle/kaggle.json`
3. Set permissions: `chmod 600 ~/.kaggle/kaggle.json`

### 4. Download datasets (run once)

```bash
# House Prices
kaggle competitions download -c house-prices-advanced-regression-techniques \
  -p notebooks/data/house_prices --unzip

# Heart Disease
kaggle datasets download -d johnsmith88/heart-disease-dataset \
  -p notebooks/data/heart_disease --unzip

# Fashion-MNIST  (also auto-downloaded by Keras)
kaggle datasets download -d zalando-research/fashionmnist \
  -p notebooks/data/fashion_mnist --unzip

# Brain Stroke
kaggle datasets download -d fedesoriano/stroke-prediction-dataset \
  -p notebooks/data/stroke --unzip

# SMS Spam
kaggle datasets download -d uciml/sms-spam-collection-dataset \
  -p notebooks/data/sms_spam --unzip

# Brain Tumor (tabular features)
kaggle datasets download -d jakeshbohaju/brain-tumor \
  -p notebooks/data/brain_tumor --unzip
```

> **Offline / no-Kaggle mode:** Every notebook includes a synthetic data fallback — it will auto-generate a representative dataset if the Kaggle CSV is not found. This lets you run and learn from the code immediately.

### 5. Launch Jupyter

```bash
jupyter notebook
```

Open the `notebooks/` folder and run each notebook in order.

---

## Project Structure

```
tafl-project/
├── try2.html                          # CFG → CNF/GNF web tool
├── README.md
└── notebooks/
    ├── 01_ml_libraries_intro.ipynb
    ├── 02_linear_regression.ipynb
    ├── 03_logistic_regression.ipynb
    ├── 04_deep_learning_frameworks.ipynb
    ├── 05_decision_tree_brain_stroke.ipynb
    ├── 06_naive_bayes.ipynb
    ├── 07_svm_brain_tumor.ipynb
    └── data/                          # (created after downloading datasets)
        ├── house_prices/
        ├── heart_disease/
        ├── fashion_mnist/
        ├── stroke/
        ├── sms_spam/
        └── brain_tumor/
```

---

## Algorithms Covered

### Classical ML (scikit-learn)
| Algorithm | Notebook |
|---|---|
| Simple / Multiple Linear Regression | 02 |
| Ridge Regression (L2) | 02 |
| Lasso Regression (L1) | 02 |
| ElasticNet Regression | 02 |
| Polynomial Regression | 02 |
| Logistic Regression | 03 |
| Decision Tree | 05 |
| Gaussian Naïve Bayes | 06 |
| Multinomial Naïve Bayes | 06 |
| Bernoulli Naïve Bayes | 06 |
| SVM (Linear / RBF / Poly / Sigmoid) | 07 |

### Deep Learning
| Framework | Architecture | Notebook |
|---|---|---|
| TensorFlow / Keras | MLP (Sequential API) | 04 |
| TensorFlow / Keras | CNN (Functional API) | 04 |
| PyTorch | MLP | 04 |

---

## Requirements

```
numpy>=1.21
pandas>=1.3
matplotlib>=3.4
seaborn>=0.11
scikit-learn>=1.0
scipy>=1.7
tensorflow>=2.8
torch>=1.10
torchvision>=0.11
xgboost>=1.5
jupyter>=1.0
kaggle>=1.5
```

---

## References / Dataset Sources

| Dataset | Citation |
|---|---|
| House Prices | Kaggle Competition — *House Prices: Advanced Regression Techniques* |
| Heart Disease | Janosi, Steinbrunn, Pfisterer, Detrano (1988). UCI ML Repository |
| Fashion-MNIST | Xiao H., Rasul K., Vollgraf R. (2017). *Fashion-MNIST: a Novel Image Dataset for Benchmarking Machine Learning Algorithms* |
| Stroke Prediction | fedesoriano (2021). Kaggle |
| SMS Spam Collection | Almeida T., Gómez J. (2011). UCI ML Repository |
| Brain Tumor Features | Jakesh Bohaju (2020). Kaggle |

---

# CFG → CNF & GNF Converter

<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/39f987b4-8d26-4a13-a8a8-c8ceefffa1b5" />

A browser-based tool (`try2.html`) that converts a Context-Free Grammar (CFG) into:
- Chomsky Normal Form (CNF)
- Greibach Normal Form (GNF)

Open `try2.html` directly in any modern browser — no installation needed.

**Tech used:** HTML · CSS · JavaScript

