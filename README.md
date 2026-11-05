# UCI Machine Learning Practical

## Project Overview

This project contains five machine learning classification experiments using datasets from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/).

The main objective is to explore datasets, perform data preprocessing, train different classification algorithms, evaluate their performance and compare the results.

The experiments were developed using Python, Anaconda and Jupyter Notebook.

## Datasets Used

| No. | Dataset | UCI ID | Records | Input Features | Target | Classification |
|---:|---|---:|---:|---:|---|---|
| 1 | Drug Consumption (Quantified) | 373 | 1,885 | 12 | Cannabis | Multiclass |
| 2 | Fertility | 244 | 100 | 9 | Diagnosis | Binary |
| 3 | Student Performance on an Entrance Examination | 582 | 666 | 11 | Performance | Multiclass |
| 4 | Breast Cancer Wisconsin (Diagnostic) | 17 | 569 | 30 | Diagnosis | Binary |
| 5 | Wine Recognition | 109 | 178 | 13 | Class | Multiclass |

## Project Structure

```text
UCI_Machine_Learning_Practical/
│
├── 01_Drug_Consumption/
│   └── Drug_Consumption.ipynb
│
├── 02_Fertility/
│   └── Fertility.ipynb
│
├── 03_Student_Performance/
│   └── Student_Performance.ipynb
│
├── 04_Breast_Cancer/
│   └── Breast_Cancer.ipynb
│
├── 05_Wine_Recognition/
│   └── Wine_Recognition.ipynb
│
├── results/
│   ├── fertility_model_comparison.csv
│   ├── student_performance_model_comparison.csv
│   ├── breast_cancer_model_comparison.csv
│   └── wine_recognition_model_comparison.csv
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Machine Learning Workflow

Each dataset was studied using the following general workflow:

1. Import the required Python libraries.
2. Load the dataset from the UCI Machine Learning Repository.
3. Explore the dataset using descriptive statistics and visualizations.
4. Check missing values and duplicate records.
5. Separate input features and target variables.
6. Split the data into training and testing sets, generally using a 70:30 ratio.
7. Apply suitable preprocessing and feature scaling.
8. Train classification algorithms.
9. Evaluate model performance.
10. Compare the results and write conclusions.

For the Student Performance dataset, a group-aware split was used to keep identical input-feature combinations together between training and testing data.

## Machine Learning Algorithms

Four classification algorithms were implemented:

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine (SVM)

## Evaluation Metrics

The following evaluation metrics were used:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Macro-averaged precision, recall and F1-score were used for model comparisons where appropriate, particularly for datasets with imbalanced classes.

## Best Model Results

The following table highlights the best-performing model by macro F1-score in each experiment, except where the Drug Consumption experiment is noted separately.

| Dataset | Selected Model | Accuracy | Macro F1-score |
|---|---|---:|---:|
| Drug Consumption | Balanced Random Forest | 36.22% | 31.00% |
| Fertility | Support Vector Machine | 73.33% | 52.00% |
| Student Performance | Random Forest | 50.25% | 50.00% |
| Breast Cancer | Support Vector Machine | 98.25% | 98.12% |
| Wine Recognition | Random Forest | 100.00% | 100.00% |

**Note:** For Drug Consumption, the original SVM achieved the highest accuracy of 41.70%, while the balanced Random Forest achieved the highest macro F1-score. For Fertility, Random Forest had the highest accuracy (76.67%), but SVM had the highest macro F1-score. The selected models emphasize macro F1-score rather than accuracy alone.

The reported results are based on individual train-test splits. They are educational experimental results and may vary with different splits or validation methods.

## Technologies Used

- Python
- Anaconda
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- ucimlrepo

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/UCI-Machine-Learning-Practical.git
```

### 2. Open the project directory

```bash
cd UCI-Machine-Learning-Practical
```

### 3. Create the Conda environment

```bash
conda create -n uci_ml python=3.11
```

### 4. Activate the environment

```bash
conda activate uci_ml
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Register the Jupyter kernel

```bash
python -m ipykernel install --user --name uci_ml --display-name "Python (UCI ML)"
```

### 7. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open any of the five notebooks and select the **Python (UCI ML)** kernel.

## Dataset Sources and Acknowledgements

The datasets were obtained from the UCI Machine Learning Repository:

1. [Drug Consumption (Quantified) – UCI ID 373](https://archive.ics.uci.edu/dataset/373/drug-consumption-quantified)
2. [Fertility – UCI ID 244](https://archive.ics.uci.edu/dataset/244/fertility)
3. [Student Performance on an Entrance Examination – UCI ID 582](https://archive.ics.uci.edu/dataset/582/student+p)
4. [Breast Cancer Wisconsin (Diagnostic) – UCI ID 17](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)
5. [Wine Recognition – UCI ID 109](https://archive.ics.uci.edu/dataset/109/wine)

Please refer to the original UCI dataset pages for dataset citations and licensing information.

## Important Note

This repository is an academic machine learning practical project. The results are intended for learning and experimentation. They should not be used as clinical diagnoses, medical advice or definitive predictions about individuals.

## Author

**Your Name**

Master of Computer Applications (MCA)

Machine Learning Practical Project
