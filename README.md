# Credit Card Approval Predictor

![Credit card being held in hand](credit_card.jpg)  

This project builds a machine learning model to automatically predict credit card approvals. It replicates the process used by commercial banks to analyze applications, helping reduce human error and save time.

## Dataset
- **Source:** [UCI Machine Learning Repository – Credit Card Approval dataset](https://archive.ics.uci.edu/ml/datasets/credit+approval)  
- **Size:** 690 applications  
- **Target Variable:** Whether a credit card is approved (`+`) or rejected (`-`)  
- **Features:** Numeric (e.g., income, loan balance) and categorical (e.g., gender, employment status)

## Steps Taken

1. **Data Cleaning**
   - Replaced missing values (`?`) with the most frequent value.  
   - Confirmed no remaining missing values.

2. **Encoding Categorical Variables**
   - Converted categorical variables to dummy/indicator variables using one-hot encoding.

3. **Splitting the Data**
   - Train-test split: 70% training, 30% testing  
   - Stratified split to preserve the class distribution

4. **Data Scaling**
   - Standardized features using `StandardScaler` for better model performance.

5. **Modeling**
   - Logistic Regression with hyperparameter tuning using `GridSearchCV`.  
   - Hyperparameters tested: `C` (regularization strength), `solver` (`liblinear` and `lbfgs`)

6. **Results**
   - **Best Hyperparameters:** `{'C': 0.0001, 'solver': 'lbfgs'}`  
   - **Cross-Validation Accuracy:** 0.917
   - **Test Accuracy:** 0.918

## How to Run
1. Clone the repository:  
   ```bash
   git clone <https://github.com/MohamedElwan15/credit-card-approval>
