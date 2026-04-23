# 🎯 Customer Purchase Propensity: Data Cleaning & Feature Engineering Pipeline

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Latest-success?style=for-the-badge&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange?style=for-the-badge&logo=scikit-learn)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A comprehensive data preprocessing and feature engineering project for predicting customer purchase propensity** 🚀

[Project Overview](#-project-overview) • [Features](#-features) • [Getting Started](#-getting-started) • [Project Structure](#-project-structure) • [Deliverables](#-deliverables)

</div>

---

## 📋 Project Overview

This is a **practical examination project** that demonstrates a complete data preprocessing and feature engineering pipeline for machine learning. As a Junior Data Analyst at an e-commerce company, you'll work with multiple raw data sources (CSV, JSON, SQL, and APIs) to create a clean, feature-engineered dataset for predicting customer purchase behavior.

### 🎓 Learning Objectives

By completing this project, you will demonstrate:

- ✅ **Understanding and planning** of a full data preprocessing workflow
- ✅ **Hands-on practice** with data cleaning, imputation, encoding, outlier handling, transformation, and feature scaling
- ✅ **Awareness** of how to handle different variable types for ML-ready datasets
- ✅ **Feature engineering skills** to create meaningful predictive features

---

## 🌟 Features

### 📊 Data Processing Techniques Implemented

| Technique | Purpose |
|-----------|---------|
| **Data Loading** | CSV, JSON, SQL, and API Integration |
| **EDA** | Univariate, Bivariate, Multivariate Analysis |
| **Missing Data Handling** | Simple, KNN, MICE, Complete Case Analysis |
| **Outlier Detection** | Z-score, IQR, Percentile, Winsorization |
| **Encoding** | Label, One-Hot, Ordinal, Binning |
| **Feature Scaling** | StandardScaler, MinMaxScaler, RobustScaler |
| **Feature Engineering** | Interaction Features, Transformations, Binning |

---

## 🚀 Getting Started

### Prerequisites

- 🐍 Python 3.10 or higher
- 📦 Required libraries (see requirements.txt)
- 💾 SQLite for database operations
- 🌐 Internet connection (for API data fetching)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Data_reprocessing_and_Feature_Engineering_Practical-Exam.git
   cd Data_reprocessing_and_Feature_Engineering_Practical-Exam
   ```

2. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook DataPreprocessing.ipynb
   ```

---

## 📁 Project Structure

```
📦 Data_reprocessing_and_Feature_Engineering_Practical-Exam/
├── 📂 data/
│   ├── 📄 customers.csv                  # Customer demographics
│   ├── 📄 transactions.json              # Transaction records
│   ├── 📄 products.sql                   # Product information
├── 📄 README.md                          # Project documentation
├── 📄 LICENSE                            # MIT License
├── 📄 requirements.txt                   # Python dependencies
├── 📔 DataPreprocessing.ipynb            # Main analysis notebook
├── 📄 processed_customer_data.csv    # Final output (generated)
└── 📊 pandas_profiling_report.html       # Automated EDA report
```

---

## 🔄 Implementation Workflow

### **Step 1️⃣: Project Planning & Problem Framing**
- Define Data Analysis concept
- Outline Data Science project lifecycle
- Frame as binary classification problem (Customer purchased: Yes/No)

### **Step 2️⃣: Data Import & Understanding**
- Load from multiple sources (CSV, JSON, SQL, API)
- Merge datasets using customer_id and product_id
- Explore with `.info()`, `.describe()`, `.head()`
- Integrate data from: https://dummyjson.com/users

### **Step 3️⃣: Exploratory Data Analysis (EDA)**
```python
📊 Univariate Analysis
   ├─ Distribution histograms
   ├─ Skewness identification
   └─ Pandas Profiling reports

📊 Bivariate Analysis
   ├─ Correlation with target (purchased)
   ├─ Mean comparisons
   └─ Relationship visualizations

📊 Multivariate Analysis
   ├─ Pairplots
   ├─ Heatmaps
   └─ Grouped statistics
```

### **Step 4️⃣: Handling Missing Data**
- ✨ Simple Imputer (mean/median)
- 🎯 Most Frequent Imputation
- 🚩 Missing Indicator + Random Sample
- 🤖 KNN Imputer
- 🔗 MICE Algorithm
- ❌ Complete Case Analysis

### **Step 5️⃣: Outlier Detection & Handling**
- 📐 Z-score Method (|z| > 3)
- 📦 IQR Method (Q1, Q3)
- 📊 Percentile Method (1st, 99th)
- ✂️ Winsorization (optional)

### **Step 6️⃣: Mixed & Date/Time Variables**
```python
# Date conversions and feature extraction
signup_date → datetime → days_since_signup
last_purchase_date → datetime → days_since_last_purchase

# Mixed variable handling (e.g., customer IDs with letters)
```

### **Step 7️⃣: Encoding Categorical Data**
- 🏷️ Label Encoding (ordinal variables)
- 🔥 One-Hot Encoding (nominal variables)
- 📊 Ordinal Encoding (ordered categories)
- 🎯 Numerical Feature Binning

### **Step 8️⃣: Feature Scaling**
```python
✨ StandardScaler       (mean=0, std=1)
📏 MinMaxScaler        (range 0-1)
🔌 MaxAbsScaler        (absolute max scaling)
🛡️ RobustScaler        (resistant to outliers)
📐 Normalizer          (L2 normalization)
```

### **Step 9️⃣: Feature Construction & Transformation**
```python
# Interaction Features
purchase_per_day = total_purchases / days_since_signup

# Transformations
📊 FunctionTransformer  (Log, Square Root, Reciprocal)
📈 PowerTransformer     (Box-Cox, Yeo-Johnson)

# Binning & Binarization
Equal-width binning → income groups
Binary conversion → frequent_buyer (threshold-based)
```

### **Step 🔟: Final Output & Summary**
- 💾 Export: `processed_customer_data.csv`
- 📝 Save pipeline: `feature_pipeline.py`
- 📊 Generate summary report

---

## 📊 Key Statistics & Insights

### Raw Data Characteristics:
- **Total Records**: Multiple datasets merged on customer_id
- **Data Types**: Numerical, Categorical, Date/Time, Mixed
- **Missing Values**: Handled with multiple imputation strategies
- **Outliers**: Detected and managed using 3+ techniques

### Data Quality Issues:
- 🔴 Missing values in income, purchase history
- 🔴 Skewed distributions in purchase frequency
- 🔴 Outliers in spending amounts
- 🔴 Inconsistent date formats

---

## 📦 Dependencies

Core libraries used in this project:

```txt
pandas                 # Data manipulation
numpy                  # Numerical computing
matplotlib             # Visualization
seaborn                # Statistical visualization
scikit-learn           # ML tools & preprocessing
pandas-profiling       # Automated EDA
requests               # API calls
sqlite3                # Database operations
```

See `requirements.txt` for the complete list.

---

## 📊 Deliverables

This project includes the following deliverables:

| 📦 Deliverable | 📝 Description |
|---|---|
| 📔 **DataPreprocessing.ipynb** | Complete preprocessing pipeline with explanations |
| 📄 **processed_customer_data.csv** | Final cleaned & feature-engineered dataset |
| 📋 **Summary_Report.md** | Techniques used, findings, and recommendations |
| 📊 **pandas_profiling_report.html** | Automated exploratory analysis report |
| 📚 **README.md** | This documentation file |
| 📜 **LICENSE** | MIT License |

---

## 🎯 How to Use This Project

1. **Review the Planning** 📋
   - Read the theory section in the notebook
   - Understand the problem framing

2. **Execute the Pipeline** ▶️
   - Run cells sequentially in the notebook
   - Observe transformations at each step
   - Check data quality improvements

3. **Analyze Results** 📊
   - Review EDA visualizations
   - Examine feature correlations
   - Compare imputation techniques

4. **Apply to Your Data** 🚀
   - Adapt the pipeline for your datasets
   - Modify parameters as needed
   - Export processed data

---

## 🎓 Learning Resources

This project covers essential data science concepts:

- 📚 [Pandas Documentation](https://pandas.pydata.org/docs/)
- 🔬 [Scikit-learn Guide](https://scikit-learn.org/stable/)
- 📊 [Pandas Profiling](https://pandas-profiling.ydata.ai/)
- 🎯 [Feature Engineering Techniques](https://www.analyticsvidhya.com/)

---

## 📈 Project Outcomes

Upon completion, you will have:

✅ A fully preprocessed dataset ready for ML modeling
✅ Reusable preprocessing pipeline code
✅ Understanding of data quality issues and solutions
✅ Experience with multiple transformation techniques
✅ Documentation of decisions and rationale

---

## 🤝 Contributing

This is a student project submitted for examination. However, suggestions and improvements are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit changes (`git commit -m 'Add improvement'`)
4. Push to branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍🎓 Author

**Student Name**: Prath Udhnawala
**Institution**: Red & White Multimedia Institute
**Exam**: Practical Examination - Data Preprocessing & Feature Engineering | Set A
**Date Submitted**: 23rd April 2024

---

## 📞 Contact & Questions

For questions or clarifications about this project:
- 🐙 GitHub: Prath-Digital

---

## 🙏 Acknowledgments

- 🎓 Special thanks to the faculty for the comprehensive project requirements
- 📚 Thanks to the open-source data science community
- 🛠️ Built with Python, Pandas, Scikit-learn, and Jupyter

---

<div align="center">

**Made with ❤️ for data preprocessing excellence**

⭐ If this project helped you, please give it a star! ⭐

</div>