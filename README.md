# 2025-Y2-S1-KU-46-AI-ML
# Healthcare Stroke Prediction Pipeline

## 📋 Project Overview
This project implements a comprehensive data preprocessing pipeline for stroke prediction using a healthcare dataset. The pipeline performs data cleaning, feature engineering, and preparation for machine learning models to predict stroke occurrences based on patient health metrics.

## 🏥 Dataset Details
**Dataset:** `healthcare-dataset-stroke-data.csv`
- **Records:** 5,110 patient records
- **Features:** 12 clinical attributes
- **Target Variable:** `stroke` (binary classification)

### Key Features:
- **Demographic:** gender, age, hypertension, heart_disease, ever_married
- **Lifestyle:** work_type, Residence_type, smoking_status
- **Clinical:** avg_glucose_level, bmi
- **Identifier:** id

### Data Quality:
- 201 missing values in `bmi` column (handled via median imputation)
- Categorical variables requiring encoding
- Numerical outliers detected and removed

## 👥 Group Member Roles
*Note: Replace with actual team member names and responsibilities*

| Member | Role | Responsibilities |
|--------|------|------------------|
| Member 1 | Data Preprocessing | Handling missing values, outlier detection |
| Member 2 | Feature Engineering | Encoding categorical variables, feature selection |
| Member 3 | Pipeline Development | Scikit-learn pipeline implementation |
| Member 4 | Documentation | Code documentation, README preparation |

## 🚀 How to Run the Code

### Prerequisites
```bash
pip install seaborn matplotlib scikit-learn pandas numpy
```

### Execution Steps
1. **Mount Google Drive** (if using Colab) or adjust file paths for local execution
2. **Load the dataset** from `/content/drive/MyDrive/healthcare-dataset-stroke-data.csv`
3. **Run the pipeline cells sequentially**:
   - Step 0: Install and import libraries
   - Step 1: Load and explore dataset
   - Step 2: Handle missing values (median imputation for BMI)
   - Step 3: Encode categorical variables (OneHotEncoding)
   - Step 4: Detect and remove outliers (IQR method)
   - Step 5: Feature scaling and preparation for modeling

### Key Outputs
- **Original data shape:** (5110, 12)
- **After preprocessing:** (4383, 17) - 727 rows removed (14.23%) due to outliers
- **Visualizations:** Boxplots before/after outlier removal for age, glucose level, and BMI

## 📊 Pipeline Architecture

### Data Processing Steps:
1. **Missing Value Treatment**: Median imputation for numerical features
2. **Categorical Encoding**: OneHotEncoding for 5 categorical variables
3. **Outlier Handling**: IQR-based removal for numerical features
4. **Feature Scaling**: StandardScaler implementation (ready for ML models)

### Technical Stack:
- **Data Manipulation**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Machine Learning**: scikit-learn pipelines
- **Feature Engineering**: ColumnTransformer, SimpleImputer

## 🔮 Next Steps
This pipeline prepares the data for machine learning models. Potential next steps include:
- Implementing classification algorithms (Logistic Regression, Random Forest, etc.)
- Hyperparameter tuning and model evaluation
- Feature importance analysis
- Deployment of prediction model

## 📁 Project Structure
```
G46_pipeline/
├── G46_pipeline.ipynb          # Main pipeline notebook
├── healthcare-dataset-stroke-data.csv  # Dataset
├── Individual ipynb files
└── README.md                   # Project documentation
```

## ⚠️ Important Notes
- The dataset path needs adjustment for local execution
- Outlier removal removed ~14% of data - consider impact on model performance
- Categorical encoding created 17 final features for modeling
- Pipeline is designed for reproducibility and scalability

For questions or issues, please refer to the code comments or create an issue in the repository.
