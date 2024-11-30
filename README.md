# Classification Task: Predicting Diabetes Risk

## Overview

This project demonstrates the use of machine learning models to predict whether an individual is at risk of diabetes based on key health indicators. By following this tutorial, you will learn how to preprocess data, build predictive models, and evaluate their performance using standard metrics. The dataset used is the **Pima Indians Diabetes Dataset**, sourced from the UCI Machine Learning Repository.

---

## Objectives

The primary objectives of this project are to:
1. Preprocess and explore the dataset to identify patterns and relationships.
2. Build and evaluate predictive models using:
   - **Logistic Regression**
   - **Random Forest**
   - **Support Vector Machine (SVM)**
3. Understand model performance using metrics such as:
   - Accuracy
   - Precision
   - Recall
   - F1-Score
   - AUC (Area Under the ROC Curve)
4. Gain insights into the strengths and limitations of each model.

---

## Dataset

### **Source**
The dataset is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/diabetes).

### **Features**
| Feature Name              | Description                               | Type    |
|---------------------------|-------------------------------------------|---------|
| Pregnancies               | Number of pregnancies                    | Numeric |
| Glucose                   | Plasma glucose concentration (mg/dL)     | Numeric |
| BloodPressure             | Diastolic blood pressure (mm Hg)         | Numeric |
| SkinThickness             | Triceps skinfold thickness (mm)          | Numeric |
| Insulin                   | 2-hour serum insulin (mu U/ml)           | Numeric |
| BMI                       | Body Mass Index (kg/m²)                  | Numeric |
| DiabetesPedigreeFunction  | Diabetes pedigree function               | Numeric |
| Age                       | Age (years)                              | Numeric |
| Outcome                   | Diabetes status (1=Positive, 0=Negative) | Target  |

---

## Methodology

### **1. Data Exploration**
- Analyze the dataset for missing or improbable values (e.g., zero glucose levels).
- Visualize feature distributions and pairwise relationships using histograms and scatter plots.
- Use correlation matrices to identify significant relationships between features and the target variable.

### **2. Data Preprocessing**
- Replace zero or missing values in critical columns (e.g., `Glucose`, `BloodPressure`) with column medians.
- Split the dataset into:
  - **Training Set (80%)**: For model building.
  - **Testing Set (20%)**: For performance evaluation.
- Normalize features using **StandardScaler** to ensure comparability, especially for SVM.

### **3. Model Building**
- Train three models on the preprocessed data:
  - **Logistic Regression**: A simple, interpretable baseline model.
  - **Random Forest**: An ensemble model combining multiple decision trees.
  - **SVM**: Optimizes decision boundaries in high-dimensional space.

### **4. Model Evaluation**
- Use the following metrics to evaluate model performance:
  - **Accuracy**: Overall correctness of predictions.
  - **Precision**: Correctness of positive predictions.
  - **Recall**: Ability to identify all positive cases.
  - **F1-Score**: Harmonic mean of precision and recall.
  - **AUC**: Measures the area under the ROC curve.
- Visualize results using confusion matrices and ROC curves for each model.

### **5. Insights**
- Summarize model performance to compare strengths and weaknesses.
- Highlight feature importance for interpretability, especially for Random Forest.

---

## Results and Insights

### **Key Findings**
1. **Logistic Regression**:
   - Effective as a baseline model.
   - Struggled with capturing non-linear relationships in the data.
2. **Random Forest**:
   - Achieved high recall, making it suitable for imbalanced datasets.
   - Provided feature importance insights.
3. **SVM**:
   - Captured complex patterns effectively.
   - Required scaling to perform optimally.


## How to Run

### Step 1: Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/sab110/Classification-Task-Diabetics.git
cd Classification-Task-Diabetics

```

### Step 2: Install Dependencies
Install the required Python libraries using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### Step 3: Run the Script
Run the Python script to execute the workflow:
```bash
python diabetes_prediction.py
```

### Step 4: Explore the Results
The script includes outputs such as:
- Confusion matrices for model performance evaluation.
- ROC curves for visualizing the models' ability to distinguish between classes.
- Classification reports detailing accuracy, precision, recall, and F1-scores.

---

## Tools and Libraries

- **Programming Language**: Python
- **Libraries**:
  - `pandas`, `numpy`: Data manipulation and analysis.
  - `matplotlib`, `seaborn`: Data visualization.
  - `scikit-learn`: For model training, evaluation, and preprocessing.

---

## Future Work

1. **Explore Advanced Models**:
   - Implement Gradient Boosting or XGBoost to potentially improve performance.
2. **Handle Imbalanced Data**:
   - Use oversampling techniques like SMOTE to address class imbalance.
3. **Hyperparameter Tuning**:
   - Optimize parameters for each model to further enhance performance.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Author

This project was developed to help learners understand key concepts in classification and machine learning, with a focus on healthcare-related datasets. For any questions or suggestions, feel free to reach out.
```
