# Predict_Customer_Churn

📓 eda.ipynb

1. Setup & Config
   1.1 Imports
   1.2 Global Config (paths, random seed, display settings)

2. Data Loading
   2.1 Load Train / Test / Sample Submission
   2.2 Shape & Basic Info

3. Exploratory Data Analysis
   3.1 Data Information - dtypes, non-null counts, memory usage
   3.2 Target Balance - value_counts, bar plot, pie chart
   3.3 Numerical & Categorical Feature Inventory - hangi kolonlar numerical, hangi kolonlar categorical listesi
   3.4 Missing Value Analysis - her kolon için missing count & %, heatmap
   3.5 Duplicate Row Check
   3.6 Numerical Feature Distributions - histogram + KDE her numerical kolon için
   3.7 Categorical Feature Distributions - bar chart her categorical kolon için
   3.8 Numerical Distribution by Target - boxplot / violin plot (target'a göre ayrılmış)
   3.9 Categorical Feature vs Target - stacked bar / grouped bar
   3.10 Correlation Heatmap - numerical kolonlar arası Pearson
   3.11 Outlier Analysis - IQR yöntemi, her kolon için outlier sayısı

4. Key Findings & Notes
   - Markdown hücresi, EDA'dan çıkan bulgular

📓 train.ipynb

1. Setup & Config
   1.1 Imports
   1.2 Global Config - paths, random seed - model hyperparameters - CV stratejisi (fold sayısı vs.) - RUN_FULL_TRAIN flag

2. Data Loading
   2.1 Load Train / Test / Sample Submission
   2.2 Shape & Sanity Check

3. Data Preprocessing
   3.1 Drop / Keep Kolon Kararları
   3.2 Missing Value Imputation - numerical: median / mean - categorical: mode / "Unknown"
   3.3 Encoding - Label Encoding - One-Hot Encoding - Target Encoding (varsa)
   3.4 Outlier Handling (gerekiyorsa)
   3.5 Feature Scaling (gerekiyorsa)

4. Feature Engineering
   4.1 Yeni Kolon Türetme
   4.2 Interaction Features (gerekiyorsa)
   4.3 Final Feature Listesi

5. Modeling
   5.1 X / y / test Split Tanımı
   5.2 Cross-Validation Setup (StratifiedKFold vs.)
   5.3 Training on Fixed Parameters - CV loop - fold bazında metrik kayıt - out-of-fold (OOF) prediction

6. Model Evaluation
   6.1 OOF Metric (overall)
   6.2 Fold Bazında Metrik Tablosu
   6.3 Confusion Matrix (classification ise)
   6.4 Feature Importance Plot

7. Submission Generation
   7.1 Test Prediction (CV fold ortalaması)
   7.2 Sample Submission ile Merge
   7.3 submission.csv Export
