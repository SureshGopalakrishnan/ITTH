# Assignment : Customer Churn Classification

This is a Python code (`Classification.py`) for building and evaluating multiple machine learning models to predict **customer churn** in a banking dataset.

## Overview
The code demonstrates how to:
- Load and preprocess customer churn data
- Train multiple classification models
- Evaluate models using key metrics
- Compare results across models
- Visualize churn patterns across different customer features

## Models Implemented
- Logistic Regression
- Logistic Regression (Balanced)
- Decision Tree
- Decision Tree (Fine Tuned)
- Random Forest
- Random Forest (Fine Tuned)
- Gradient Boosting
- XGBoost
- K-Nearest Neighbors (KNN)

## Evaluation Metrics
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**
- **Classification Report**

## Code Structure

The script is organized into the following main sections:

1. **Initial Setup**
   - Install dependencies (e.g., `lifelines`)
   - Import required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`, `xgboost`, etc.)
   - Configure pandas and numpy display options
   - Upload the dataset (`Banking_churn_prediction.csv`)

2. **Load Data**
   - Read dataset into pandas DataFrame
   - Display shape, size, and info
   - Identify missing data in features (`gender`, `dependents`, `occupation`, `city`)

3. **Statistical Details**
   - Summary statistics with `describe()`
   - Extended descriptive statistics for categorical and numerical variables

4. **Exploratory Data Analysis (EDA)**
   - Distribution analysis (e.g., age, balance, transactions)
   - Churn distribution by customer attributes (e.g., occupation, branch, net worth category)
   - Visualizations with Plotly and Seaborn
   - Percentage-based churn comparisons for better insight

5. **Observations & Insights**
   - Occupation-wise churn trends
   - Branch-level and net worth category churn distribution
   - Key insights into customer behavior

6. **Feature Engineering & Preprocessing**
   - Label encoding categorical variables
   - Handling missing values
   - Feature scaling using `StandardScaler`
   - Train-test split for model building

7. **Model Training & Evaluation**
   - Train multiple classifiers (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, XGBoost, KNN)
   - Fine-tuning Decision Tree and Random Forest with hyperparameters
   - Evaluate models using accuracy, precision, recall, F1-score
   - Print classification reports
   - Generate confusion matrices

8. **Model Comparison**
   - Consolidated comparison of accuracy scores across models
   - Visualization of model performance
