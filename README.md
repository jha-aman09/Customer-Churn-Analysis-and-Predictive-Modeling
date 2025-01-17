# Customer Churn Analysis and Predictive Modeling

This repository contains the code and resources for a **Customer Churn Analysis** project. The project involves data preprocessing, feature engineering, and building a predictive model to identify customers likely to churn. 

---

## 📂 Project Structure

```plaintext
.
├── feature_engineering.py         # Script for feature engineering
├── predictive_modeling.py         # Script for predictive modeling
├── data/
│   ├── clean_data_after_eda.csv   # Cleaned dataset after exploratory data analysis
│   ├── price_data.csv             # Pricing dataset with temporal features
│   ├── data_for_predictions.csv   # Dataset used for predictive modeling
├── results/
│   ├── engineered_features.csv    # Transformed dataset with engineered features
│   └── evaluation_metrics.txt     # Key evaluation results of the predictive model
└── README.md                      # Project documentation
```
---

## 🚀 Project Workflow

### 1. **Feature Engineering**
The **`feature_engineering.py`** script performs the following steps:
- **Data Loading**: Reads raw datasets and parses date columns.
- **Data Cleaning**: Removes irrelevant columns.
- **Feature Creation**:
  - Extracts temporal features (e.g., year, month, day of the week).
  - Computes derived features like price variation ratio, durations, and average price.
- **Data Merging**: Combines datasets (`clean_data_after_eda.csv` and `price_data.csv`) to create a unified dataset.
- **Output**: Saves the transformed dataset to `engineered_features.csv`.

### 2. **Predictive Modeling**
The **`predictive_modeling.py`** script builds and evaluates a Random Forest Classifier:
- **Data Preparation**: Splits data into training and testing sets.
- **Model Training**: Trains a Random Forest Classifier with:
  - `n_estimators=100`
  - `max_depth=None`
  - `random_state=42`
- **Evaluation Metrics**:
  - Accuracy Score
  - Precision, Recall, and F1-score
  - Confusion Matrix (visualized as a heatmap)

---

## ⚙️ How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/churn-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd churn-prediction
   ```
3. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the feature engineering script:
   ```bash
   python feature_engineering.py
   ```
5. Run the predictive modeling script:
   ```bash
   python predictive_modeling.py
   ```

---

## 📊 Results

- **Feature Engineering**:
  - Temporal and derived features were successfully created and saved to `engineered_features.csv`.
- **Model Performance**:
  - Achieved **85% accuracy** in predicting customer churn.
  - Generated comprehensive classification reports and confusion matrices for further analysis.

---

## 🔑 Key Insights

1. Temporal features like `duration_activ_to_end` and price variation metrics were instrumental in predicting churn.
2. The Random Forest Classifier provided robust predictions, but additional improvements could be achieved through hyperparameter tuning and handling class imbalance.

---

## 🛠️ Potential Improvements

- Perform hyperparameter tuning using `GridSearchCV`.
- Address potential class imbalances with techniques like SMOTE or weighted loss functions.
- Experiment with alternative models such as Gradient Boosting (XGBoost, LightGBM).

---

## 🧑‍💻 Author  
- **LinkedIn**: [Aman Jha](https://www.linkedin.com/in/aman--jha/)  
- **GitHub**: [Aman Jha](https://github.com/jha-aman09)  
