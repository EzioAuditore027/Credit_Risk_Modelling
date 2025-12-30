# Credit Risk Modeling

This repository contains a comprehensive data analysis pipeline designed to predict credit risk using the **Lending Club dataset** (2007–2018). The project focuses on cleaning massive financial datasets, performing Exploratory Data Analysis (EDA), and preparing data for machine learning models by identifying "Good" vs. "Bad" loans.

## 🚀 Key Features

* **Data Handling**: Efficiently processes a large dataset (over 2 million records) by implementing sampling strategies.
* **Data Cleaning**:
    * Automated removal of columns with excessive missing values (>20%).
    * **Leakage Prevention**: Identifies and removes features that would not be available at the time of loan application (e.g., `total_pymnt`, `recoveries`).
* **Feature Engineering**:
    * **Target Variable Creation**: Classifies loans into binary "Good" (Fully Paid) and "Bad" (Charged Off, Default, etc.) categories.
    * **Regional Analysis**: Maps US states to broader geographical regions to handle high-cardinality location data.
    * **Transformation**: Converts categorical employment data (`emp_length`) into numerical formats.
* **Advanced Imputation**: Fills missing values using region-specific modes (for categorical data) and means/medians (for numerical data).
* **Outlier Detection**: Utilizes **Isolation Forest** to identify and handle statistical outliers in financial data.

## 🛠️ Technologies Used

* **Python**
* **Pandas & NumPy**: For high-performance data manipulation.
* **Matplotlib & Seaborn**: For visualizing loan distributions and correlations.
* **Scikit-Learn**: For outlier detection (Isolation Forest) and preprocessing.

## 📂 Data Source

**Note:** The dataset used in this project is too large to be hosted directly on GitHub.

1.  Download the dataset from Kaggle: [Lending Club Loan Data](https://www.kaggle.com/wordsforthewise/lending-club)
2.  Extract the file `accepted_2007_to_2018Q4.csv`.
3.  Place it in a folder named `data/` inside this project directory.

## 📊 Usage

1.  Clone the repository.
2.  Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Ensure the data file is placed correctly as described above.
4.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook main.ipynb
    ```