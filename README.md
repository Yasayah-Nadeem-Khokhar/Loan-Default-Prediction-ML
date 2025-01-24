# Loan Default Prediction Using Machine Learning  

## Project Overview  
This project aims to predict loan defaults using machine learning techniques. The objective is to classify whether a loan will default or not, leveraging both supervised and unsupervised learning methods. The key challenge lies in addressing the imbalanced dataset, which impacts the models' ability to accurately predict the minority class (loan defaults).

---

## Dataset Description  
- **Size**: 165,865 entries with 22 features.  
- **Features**:  
  - **Personal Information**: Loan ID, Name, Email, Phone, City, Age, Marital Status, Employment Type, and Education.  
  - **Financial Information**: Income, Loan Amount, Credit Score, Monthly Employment Duration, and Debt-to-Income Ratio (DTIRatio).  
  - **Loan Information**: Loan Term, Interest Rate, Loan Purpose, Mortgage Status, Dependents, and presence of a Co-Signer.  
- **Target Variable**:  
  - `Default` (1: Loan Default, 0: No Default).  

---

## Models Used  
### Supervised Learning Models:  
1. Logistic Regression  
2. Decision Tree  
3. Random Forest  
4. Support Vector Machines (SVM)  
5. XGBoost  
6. K-Nearest Neighbors (KNN)  
7. Naive Bayes  

### Unsupervised Learning Models:  
1. K-Means Clustering  
2. Hierarchical Clustering  

---

## Results  
### Supervised Learning:  
- **Logistic Regression**:  
  - Accuracy: 78%, F1-score (Default = 1): 0.27  
- **Decision Tree**:  
  - Accuracy: 79%, Moderate performance for the minority class.  
- **Random Forest**:  
  - Accuracy: 88%-89%, Best accuracy but poor recall for defaults.  
- **SVM**:  
  - Accuracy: 88%, Zero recall for defaults.  
- **XGBoost**:  
  - Accuracy: 89%, Balanced performance but suboptimal for defaults.  
- **KNN**:  
  - Accuracy: 87%, Poor performance for defaults.  
- **Naive Bayes**:  
  - Accuracy: 88%, Zero recall for defaults.  

### Unsupervised Learning:  
- **K-Means Clustering**: Silhouette Score: 0.035 (Weak cluster separability).  
- **Hierarchical Clustering**: Silhouette Score: 0.019 (Poor clustering performance).  

---

## Exploratory Data Analysis (EDA)  
### Key Insights:  
1. **Correlation Analysis**:  
   - Most features have weak correlations, with low off-diagonal values in the heatmap.  
   - Target variable (`Default`) has weak correlations with predictors like `CreditScore` and `Income`.  

2. **Education Distribution**:  
   - Master's and Bachelor's degrees are the most common.  
   - PhD has the smallest representation.  

---

## Conclusion  
- **Best Model**: Random Forest achieved the highest accuracy (88%-89%), but it failed to effectively predict defaults.  
- **Key Challenges**: Imbalanced datasets impacted model performance on the minority class (defaults).  
- **XGBoost** showed promise with a better balance between precision and recall.  
- Clustering techniques (K-Means and Hierarchical) provided poor insights due to weak silhouette scores.  

---

## Future Recommendations  
1. Address class imbalance using:  
   - SMOTE (Synthetic Minority Oversampling Technique).  
   - Undersampling.  
   - Cost-sensitive learning.  
2. Explore advanced ensemble methods: Boosting and Stacking.  
3. Enhance feature selection and engineering for better clustering and predictive performance.  

---

## Project Structure  
- `data/`: Contains the dataset used for the project.  
- `notebooks/`: Jupyter Notebooks for EDA, model training, and evaluation.  
- `models/`: Saved trained models for future use.  
- `reports/`: Detailed analysis and visualizations.  
- `README.md`: Project overview and instructions.  

---

## How to Use  
1. Clone the repository:  
   ```bash
   git clone https://github.com/Yasayah-Nadeem-Khokhar/Loan-Default-Prediction-ML.git
