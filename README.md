# Google Play Store Exploratory Data Analysis (EDA) Project

This repository features an end-to-end Exploratory Data Analysis (EDA) pipeline evaluating mobile software attributes from the Google Play Store app ecosystem. By engineering raw dataset parameters, addressing unstructured text fields, and applying data profiling techniques, this project maps critical store trends, software sizing optimization paths, and premium developer pricing strategy thresholds.

---

## 📂 Repository Components

* **`gplay.csv`**: The master raw dataset containing 10,841 record observations spanning 10 key variable features[cite: 4, 5].
* **`gplay_prject.ipynb`**: The foundational Jupyter Notebook containing Python source scripts for preprocessing, null imputation, feature formatting, and initial charts[cite: 4, 5].
* **`gplay_eda_report.pdf`**: A polished, executive-ready PDF report presenting summary statistics, structured monetization insights, and professional data tables.
* **`gplay_eda_report.html`**: The semantic HTML layout blueprint utilized to generate the final analytical print document[cite: 5].

---

## 📊 Core Analytical Insights

* **Monetization Architecture**: Free applications entirely dominate market volume on the platform[cite: 4, 5]. Out of 10,840 complete rows, **10,039 applications are Free (~92.6%)**, compared to just **800 Paid applications**, establishing that freemium tiers, subscription modules, or in-app ad structures dictate the ecosystem[cite: 4, 5].
* **Premium Vertical Valuation**: Among applications utilizing upfront paid conversion models, specific categories exhibit distinct pricing leadership[cite: 4, 5]. **FINANCE** leads with an average premium listing cost of **\$7.93**, followed by **LIFESTYLE (\$6.18)** and **MEDICAL (\$3.11)**, highlighting profitable spaces for professional utility and specialized b2b tools[cite: 4, 5].

---

## 🛠️ Data Engineering & Cleaning Pipeline

The raw data fields inside `gplay.csv` required extensive cleaning to enable quantitative processing[cite: 4, 5]. The data cleaning pipeline in `gplay_prject.ipynb` covers the following operations:

1. **Structural Cleansing & Filtering**: Removed uninformative system artifacts (such as `Unnamed: 0`)[cite: 4, 5]. Rows containing isolated missing cells in strictly categorical variables (`Type` and `Content Rating`) were dropped[cite: 4, 5].
2. **Missing Rating Imputation**: The `Rating` field presented 1,474 null variables[cite: 4]. These were handled systematically by computing and imputing the statistical column mean, preventing data volume decay[cite: 4, 5].
3. **Unified Sizing Metrics (`cleansize`)**: The `Size` feature contained variable string indicators including Kilobytes (`k`), Megabytes (`M`), and `"Varies with device"` text[cite: 4, 5]. A custom preprocessing mapping function was built to clean suffix markers and map all app weights into a uniform floating-point field in standard Megabytes (MB), filling unlisted entries with global baseline averages[cite: 4, 5].
4. **String Regex Sanitization**: Stripped out non-numeric characters, currency indicators (`$`), arithmetic notation (`+`), and string grouping separators (`,`) across the `Price` and `Installs` arrays to properly cast them into computational `float64` and `int64` data types[cite: 4, 5].

---

## 🚀 How to Run the Analysis

### Prerequisites
Ensure you have Python installed along with the required libraries:
```bash
pip install pandas numpy matplotlib
