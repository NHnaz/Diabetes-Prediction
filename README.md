# Diabetes Prediction

## Project Overview

This project uses machine learning classification algorithms to predict whether a person is likely to have diabetes based on medical information. The model is trained using the Pima Indians Diabetes Dataset and evaluated using different performance metrics.

The main goal is to compare multiple machine learning algorithms and identify which one performs best in predicting diabetes.

## Dataset

**Pima Indians Diabetes Dataset**

- **Source (that we used in our project):** [Pima Indians Diabetes Dataset](https://github.com/jbrownlee/Datasets)
- **Link to the CSV file (Kaggle):** https://www.kaggle.com/datasets/kumargh/pimaindiansdiabetescsv
- **Total Records:** 768
- **Input Features:** 8
- **Target Variable:** Outcome

The dataset contains medical information such as:

- Pregnancies
- Glucose
- Blood Pressure
- Skin Thickness
- Insulin
- BMI
- Diabetes Pedigree Function
- Age

The `Outcome` column represents the prediction target:

- `0` – No diabetes
- `1` – Diabetes

## Machine Learning Algorithms

Three classification algorithms are implemented and compared:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**

## Data Preprocessing

The following preprocessing steps were performed:

- Checked the dataset for missing values and data types.
- Replaced invalid zero values in selected medical columns with missing values.
- Handled missing values using median imputation.
- Applied feature scaling for Logistic Regression.
- Split the dataset into training and testing sets using an 80:20 ratio.
- Used stratified splitting to maintain the class distribution.

## Libraries Used

The following Python libraries were used in this project:

| Library | Purpose |
|---|---|
| Pandas | Data loading, manipulation, and analysis |
| NumPy | Numerical operations |
| Matplotlib | Data visualization and plotting |
| Seaborn | Statistical visualization and correlation heatmaps |
| Scikit-learn | Data preprocessing, model training, cross-validation, and evaluation |

## Model Evaluation

The models were evaluated using the following performance metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score

Five-fold stratified cross-validation was also used to compare model performance.

### Test Set Results

| Algorithm | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.7338 | 0.6032 | 0.7037 | 0.6496 | 0.8126 |
| Decision Tree | 0.7273 | 0.6111 | 0.6111 | 0.6111 | 0.7706 |
| Random Forest | 0.7338 | 0.6102 | 0.6667 | 0.6372 | 0.8215 |

### Cross-Validation Results

Based on the average F1-score from five-fold cross-validation:

| Algorithm | Mean F1-Score |
|---|---:|
| Logistic Regression | 0.6724 |
| Decision Tree | 0.6588 |
| Random Forest | 0.6811 |

Random Forest achieved the highest average cross-validation F1-score and was selected as the best model based on that criterion.

## Project Outputs

The project includes:

- Dataset exploration and visualization.
- Correlation heatmap.
- Model training and comparison.
- Confusion matrices.
- Random Forest feature importance analysis.
- Cross-validation results.
- Sample patient prediction.
- Saved trained model and model comparison results.

## Important Notes

- The dataset contains 768 records and 8 input features.
- Invalid zero values in selected medical columns are treated as missing values during preprocessing.
- The dataset is divided into training and testing sets using an 80:20 ratio.
- Five-fold stratified cross-validation is used to compare the models.
- Random Forest was selected as the best model based on its highest average cross-validation F1-score.
- Logistic Regression achieved a slightly higher test-set F1-score and recall than Random Forest.
- The sample patient prediction is based on the trained model and should not be considered a medical diagnosis.

## Limitations

- The dataset contains only 768 records.
- The dataset represents a specific population, so the results may not generalize to everyone.
- The models are trained using a limited number of medical features.
- The predictions should not be treated as medical diagnoses.

## Conclusion

This project demonstrates how different machine learning classification algorithms can be used to predict diabetes using medical data. Among the three models, Random Forest achieved the highest cross-validation F1-score, while Logistic Regression achieved a slightly higher test-set F1-score and recall than Random Forest.

The comparison shows how different algorithms perform on the same dataset and why multiple evaluation metrics are important when selecting a classification model.

---

**Disclaimer:** This project is for educational purposes only. It is not intended to replace professional medical advice, diagnosis, or treatment.
