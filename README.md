# 🧬 DNA-Based Multi-Class Cancer Classification Using Machine Learning

## 📌 Overview

This project uses machine learning to classify cancer types based on DNA/gene-expression features.

The dataset contains **390 samples, 44 gene features, and 5 cancer classes**. Two machine learning models were developed and compared:

* Logistic Regression
* Random Forest

The **Random Forest model achieved 93.59% accuracy** on the held-out test set and was selected as the final model.

---

## 🎯 Objectives

* Analyze DNA/gene-expression data.
* Perform exploratory data analysis.
* Build machine learning models for cancer classification.
* Compare Logistic Regression and Random Forest.
* Evaluate model performance using classification metrics and confusion matrices.
* Identify important gene features.
* Save the trained model for future predictions.

---

## 📊 Dataset

| Property          | Value |
| ----------------- | ----: |
| Samples           |   390 |
| Gene features     |    44 |
| Cancer classes    |     5 |
| Samples per class |    78 |
| Training samples  |   312 |
| Test samples      |    78 |

The dataset is balanced, with **78 samples in each class**.

### Target Classes

```text
1, 2, 3, 4, 5
```

---

## 🔬 Methodology

```text
DNA Dataset
     ↓
Data Exploration
     ↓
Data Preprocessing
     ↓
80/20 Stratified Split
     ↓
 ┌─────────────────────┐
 │                     │
Logistic Regression   Random Forest
 │                     │
 └──────────┬──────────┘
            ↓
       Model Evaluation
            ↓
      Model Comparison
            ↓
       Best Model
            ↓
      Saved Model
            ↓
      New Prediction
```

---

## 🤖 Machine Learning Models

### Logistic Regression

Used as the baseline linear classification model.

**Test Accuracy: 92.31%**

### Random Forest

A non-linear ensemble learning algorithm was used for the final classification model.

Configuration:

```python
RandomForestClassifier(
    n_estimators=300,
    random_state=42,
    class_weight="balanced"
)
```

**Test Accuracy: 93.59%**

---

## 📈 Results

| Model               | Test Accuracy |
| ------------------- | ------------: |
| Logistic Regression |        92.31% |
| **Random Forest**   |    **93.59%** |

Random Forest performed better by approximately **1.28 percentage points** on the held-out test set.

### Random Forest Performance

* Accuracy: **93.59%**
* Macro Precision: **0.94**
* Macro Recall: **0.93**
* Macro F1-score: **0.94**

---

## 🧬 Feature Importance

The Random Forest model was used to identify the gene features that contributed most strongly to its predictions.

### Top Features

| Rank | Gene    | Importance |
| ---: | ------- | ---------: |
|    1 | gene_30 |   0.078824 |
|    2 | gene_28 |   0.069694 |
|    3 | gene_18 |   0.065760 |
|    4 | gene_44 |   0.063459 |
|    5 | gene_46 |   0.060185 |
|    6 | gene_45 |   0.057126 |
|    7 | gene_3  |   0.051300 |
|    8 | gene_36 |   0.047875 |
|    9 | gene_26 |   0.046761 |
|   10 | gene_39 |   0.040161 |

> **Note:** These are model-derived feature importance values and should not be interpreted as clinically validated cancer biomarkers.

---

## 📊 Evaluation

The project includes:

* Confusion matrix analysis
* Classification report
* ROC-AUC analysis
* Model comparison
* Feature importance analysis
* Prediction probability analysis

The Logistic Regression model achieved a multiclass **ROC-AUC of 0.9933** using the One-vs-Rest approach.

---

## 💾 Saved Model

The final Random Forest model is saved as:

```text
dna_cancer_random_forest.pkl
```

The required gene feature order is saved as:

```text
dna_gene_features.pkl
```

These files allow the trained model to be loaded without retraining.

---

## 🛠️ Technologies Used

**Programming Language**

* Python

**Libraries**

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib

**Machine Learning**

* Logistic Regression
* Random Forest
* StandardScaler
* Confusion Matrix
* ROC-AUC
* Feature Importance

---

## 📁 Project Files

```text
dna-cancer-classification-ml/
│
├── README.md
├── cancer detection.ipynb
├── DNA_Dataset_Normalized.csv
├── dna_cancer_random_forest.pkl
├── dna_gene_features.pkl
└── requirements.txt
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/dna-cancer-classification-ml.git
```

### 2. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib jupyter
```

### 3. Open the notebook

Open:

```text
cancer detection.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model development process.

---

## ⚠️ Limitations

* The dataset contains 390 samples.
* Evaluation uses a single stratified 80/20 train-test split.
* The model is intended for educational and research purposes.
* Predictions should not be considered medical diagnoses.
* Feature importance does not establish biological causation.

---

## 🔮 Future Scope

* Apply k-fold cross-validation.
* Perform hyperparameter optimization.
* Compare additional machine learning algorithms.
* Apply advanced feature-selection techniques.
* Test the model on independent datasets.
* Investigate biologically validated gene markers.

---

## 👩‍💻 Author

**Shreya G**

Computer Science Engineering

---

⭐ If you find this project useful, consider giving the repository a star!
