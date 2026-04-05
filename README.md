# Diabetes Risk Prediction Using 5 Machine Learning Models

## Repository Outline

This repository contains all files used throughout the data analysis, model development, and deployment process for predicting diabetes risk using machine learning.

README.md – Main project documentation
Diabetes.ipynb – Notebook for model training and evaluation
Diabetesinf.ipynb – Notebook for model inference using the best-performing model

```
deployment/
├── src/
│ ├── streamlit_app.py - Entry point for the Streamlit application
│ ├── eda.py - Exploratory Data Analysis (EDA) page
│ └── predict.py - Diabetes risk prediction page
├── model_files/
│ └── best_diabetes_model.pkl - Best model obtained from training
├── data/
│ └── diabetes_binary_health_indicators_BRFSS2015.csv
├── requirements.txt - List of required libraries
└── Dockerfile - Configuration for deployment using Docker
```

url.txt – Contains URLs for the dataset, model, and deployment

---

## Problem Background

Diabetes is a chronic disease whose prevalence continues to increase and can lead to various serious complications if not detected early. Therefore, a data-driven approach is needed to help identify individuals who may be at risk of diabetes at an earlier stage.

This project aims to build a machine learning model capable of predicting diabetes risk based on health indicators and lifestyle factors. The model can potentially be used as an early screening tool in public health contexts.

---

## Project Output

* A machine learning model for diabetes risk classification
* A Streamlit-based web application that provides:

  * Exploratory Data Analysis (EDA)
  * Diabetes risk prediction for new individual data
* Model deployment accessible through HuggingFace Spaces

---

## Data

The dataset used in this project comes from the **Behavioral Risk Factor Surveillance System (BRFSS) 2015**, which contains health-related indicators associated with diabetes.

Dataset characteristics:

* Number of observations: more than **200,000 rows**
* Number of features: **21 input features and 1 target variable**
* Target variable: diabetes status (**binary classification**)
* Most features are **numerical and discrete categorical variables**
* The dataset is **imbalanced**, with the non-diabetes class being more dominant
* Duplicate data were removed to maintain data quality and unique observations

---

## Method

This project applies a **Supervised Learning approach** for a classification task.

Main stages of the project:

1. Exploratory Data Analysis (EDA)
2. Feature Engineering:

   * Train-test split with stratification
   * Outlier handling using **Winsorization**
   * Feature scaling using **RobustScaler**
3. Model development using several algorithms:

   * K-Nearest Neighbors (KNN)
   * Support Vector Machine (SVM)
   * Decision Tree
   * Random Forest
   * Gradient Boosting
4. Model evaluation using **Cross Validation**
5. Hyperparameter tuning on the best-performing model
6. Model inference using new data
7. Model deployment using **Streamlit** and **Docker**

The main evaluation metric used is **Recall**, considering the importance of minimizing **false negatives** in healthcare-related predictions.

---

## Tech Stack

Programming Language:

* Python

Libraries:

* pandas
* numpy
* scikit-learn
* imbalanced-learn
* matplotlib
* seaborn
* plotly
* streamlit

Tools & Platforms:

* Jupyter Notebook
* Docker
* HuggingFace Spaces

---

## References

* BRFSS 2015 Dataset
* Streamlit Documentation: https://docs.streamlit.io/develop/api-reference
* Pandas Documentation: https://pandas.pydata.org/docs/user_guide/index.html
* Scikit-Learn Documentation: https://scikit-learn.org/stable/index.html
* Imbalanced-Learn Documentation: https://imbalanced-learn.org/stable/

Additional Resources:

Deployment URL:
https://huggingface.co/spaces/J1nTomank/Diabetes_Model

Dataset URL:
https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset/data?select=diabetes_binary_health_indicators_BRFSS2015.csv

Model Files:
https://drive.google.com/drive/folders/1_7nywyeDbhK7r0lvdCKXTNzOolk2APgc?usp=drive_link

---

## Notes

No additional notes.
