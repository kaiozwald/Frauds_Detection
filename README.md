# Credit Card Fraud Detection

## Project Overview
This project aims to detect fraudulent credit card transactions using machine learning techniques. The dataset used contains transactions made by European cardholders in September 2013 over two days. Since fraud cases account for only **0.172%** of all transactions, the dataset is highly imbalanced.

## Dataset
- **Source:** [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- **Total Transactions:** 284,807
- **Fraudulent Transactions:** 492 (0.172%)
- **Features:**
  - `Time`: Seconds elapsed between transactions
  - `Amount`: Transaction amount
  - `V1` - `V28`: Principal components obtained using PCA
  - `Class`: Target variable (1 = Fraud, 0 = Non-Fraud)

## Steps Taken
### 1. Data Preprocessing
- Checked for missing values and ensured data cleanliness
- Normalized `Amount` and `Time` features
- Addressed class imbalance using **SMOTE (Synthetic Minority Over-sampling Technique)**

### 2. Exploratory Data Analysis (EDA)
- Visualized distribution of transaction amounts
- Checked fraud vs. non-fraud transaction distributions
- Used **boxplots** and **histograms** to understand feature distributions

### 3. Model Training & Evaluation
#### Models Used:
- Gradient Boosting (Best Model)

#### Evaluation Metrics:
- **Precision-Recall Curve (AUC-PR)**: **0.9834**
- **Precision & Recall**:
  - Precision: 0.986
  - Recall: 0.986
- **ROC-AUC Score**: 0.99

### 4. Model Optimization
- Used **GridSearchCV** to optimize hyperparameters for Gradient Boosting
- Feature importance analysis to understand key contributing factors

### 5. Results Visualization
- **ROC & Precision-Recall Curves** for performance analysis
- **Confusion Matrix** for model evaluation

## Technologies Used
- **Python (Pandas, NumPy, Scikit-Learn, XGBoost, Matplotlib, Seaborn)**
- **Machine Learning Algorithms**
- **SMOTE for Handling Imbalance**
- **Hyperparameter Tuning with GridSearchCV**

## Conclusion
Our **Gradient Boosting model** achieved an **AUC-PR score of 0.9834**, making it highly effective in detecting fraudulent transactions. The project highlights the importance of handling class imbalance and selecting the right evaluation metrics for fraud detection problems.

## Future Improvements
- Experiment with deep learning models (LSTMs, Autoencoders)
- Implement real-time fraud detection pipelines
- Improve feature engineering techniques for better accuracy
