#  Breast Cancer Classification with Neural Network

A deep learning project that classifies breast cancer tumors as **Malignant** or **Benign** using a simple Neural Network built with TensorFlow/Keras, trained on the sklearn Breast Cancer Wisconsin dataset.

---

##  Project Overview

Breast cancer is one of the most common cancers worldwide. Early and accurate detection can significantly improve patient outcomes. This project demonstrates how a simple feedforward neural network can achieve high classification accuracy on clinical tumor measurements, enabling automated prediction of tumor malignancy.

---

## 📂Project Structure

```
├── main.ipynb        # Main Jupyter Notebook with full pipeline
└── README.md         # Project documentation
```

---

##  Dataset

- **Source:** [Sklearn Breast Cancer Wisconsin Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
- **Samples:** 569
- **Features:** 30 numerical features (e.g., radius, texture, perimeter, area, smoothness, etc.)
- **Target Classes:**
  - `0` → Malignant
  - `1` → Benign

---

##  Tech Stack

| Library | Purpose |
|---|---|
| `NumPy` | Numerical computations |
| `Pandas` | Data manipulation & EDA |
| `Matplotlib` | Visualization |
| `Scikit-learn` | Dataset, preprocessing, train-test split |
| `TensorFlow / Keras` | Neural network model building & training |

---

##  Workflow

### 1. Data Collection & Preprocessing
- Loaded the Breast Cancer dataset from `sklearn.datasets`
- Converted to a Pandas DataFrame with feature names
- Added target labels
- Performed EDA: `.info()`, `.describe()`, null checks, class distribution, group means

### 2. Train-Test Split
- 80% training / 20% testing
- `random_state=42` for reproducibility

### 3. Feature Standardization
- Applied `StandardScaler` to normalize feature values for better neural network convergence

### 4. Model Architecture

```
Input Layer  →  30 features
Hidden Layer →  20 neurons, ReLU activation
Output Layer →  2 neurons, Softmax activation (binary classification)
```

### 5. Model Training
- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **Epochs:** 10
- **Validation Split:** 10% of training data

### 6. Evaluation & Visualization
- Plotted training vs. validation **accuracy** and **loss** curves
- Evaluated final model accuracy on the test set

### 7. Prediction on New Data
- Accepts raw tumor measurement input
- Standardizes input using the fitted scaler
- Outputs prediction: **Malignant** or **Benign**

---

##  Results

| Metric | Value |
|---|---|
| Training Accuracy | ~97–99% |
| Validation Accuracy | ~95–97% |
| Test Accuracy | ~95–98% |

> *Exact values may vary slightly across runs due to stochastic training.*

---

## 🔍 Sample Prediction

```python
input_data = (11.76, 21.6, 74.72, 427.9, 0.08637, ...)

# Output
# → The tumor is Benign
```

---

##  How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas matplotlib scikit-learn tensorflow
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook main.ipynb
   ```

4. **Run all cells** in order from top to bottom.

---

## 📋 Requirements

```
numpy
pandas
matplotlib
scikit-learn
tensorflow
jupyter
```

---

##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to open a pull request or raise an issue.

---

##  License

This project is open-source and available under the [MIT License](LICENSE).

---

##  Author
Kushal Bhattarai

**Your Name**
- GitHub: [kushal1142](https://github.com/kushal1142)

