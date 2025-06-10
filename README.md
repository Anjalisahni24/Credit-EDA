# Credit Card Dataset - Exploratory Data Analysis (EDA)

This repository contains an in-depth Exploratory Data Analysis (EDA) project conducted on the **Home Credit Default Risk** dataset from Kaggle. The project is part of my Data Science training at **Personify (OneStop AI)**. The goal is to understand the key characteristics and relationships in the data that might affect a client's ability to repay a loan.

---

## 📂 Dataset

- **Source**: [Kaggle - Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk/data)
- **File used**: `application_data.csv`

This dataset contains financial and demographic information on loan applicants.

---

## 🛠️ Tools & Libraries

- Python 3.x
- Jupyter Notebook
- Libraries used:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`

---

## 📊 Project Workflow

### 1. **Data Loading and Initial Exploration**
- Loaded `application_data.csv` and displayed basic structure with `.head()` and `.info()`.
- Set pandas display options to view all columns.

### 2. **Missing Value Treatment**
- Calculated percentage of missing values for all columns.
- Dropped columns with more than **47% missing data** using a dynamic threshold.
- For important columns with lower null percentages (e.g., `OCCUPATION_TYPE` and `EXT_SOURCE_3`), missing values were handled separately:
  - Categorical values like `OCCUPATION_TYPE` were filled with "Others".
  - Continuous variables like `EXT_SOURCE_3` were treated with median imputation.

### 3. **Data Visualization**
- Plotted boxplots and histograms to examine outliers and distributions.
- Used `seaborn` to visualize relationships between numeric variables and potential risk indicators.

### 4. **Feature Understanding**
- Analyzed and described features with high importance:
  - `EXT_SOURCE_3` (external risk score)
  - `OCCUPATION_TYPE`
- Used descriptive statistics and value counts for categorical and numerical variables.

---

## 📈 Key Insights

- Several columns had over 40% missing data; thoughtful thresholds were applied to retain useful features.
- Certain occupations and risk scores showed distribution skews which may impact credit risk modeling.
- Visualizations provided clear evidence of how applicants differ across demographic and financial features.

---

## 📁 Files in this Repository

| File                   | Description                                    |
|------------------------|------------------------------------------------|
| `Credit EDA.ipynb`     | Main Jupyter Notebook with full analysis       |
| `README.md`            | Project documentation                          |
| `requirements.txt`     | Python dependencies for running the notebook   |

---

## ⚙️ How to Run This Project

1. Clone this repository:
   ```bash
   git clone https://github.com/Anjalisahni24/credit-EDA.git
   cd credit-eda
