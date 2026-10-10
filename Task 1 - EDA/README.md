# Telco Customer Churn – Exploratory Data Analysis

**Devixo Solutions Data Science Internship – Task 01**
**Author:** Dua Sajid

## Project Description
This project explores a real-world telecom dataset with Python to find out which customers leave (churn), when they leave, and what they have in common. It follows the full EDA workflow: data cleaning, feature analysis, correlation analysis, visualization, business insights and recommendations.

## Dataset Information
- **Name:** Telco Customer Churn
- **Source:** [Kaggle (blastchar)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **File:** `Telco-Customer-Churn.csv`
- **Size:** 7,043 customers and 21 columns
- **Content:** customer profile (gender, senior citizen, partner, dependents), account details (tenure, contract, billing, payment method), services (phone, internet, security, support, streaming), charges, and the target column `Churn` (Yes/No)

## Technologies Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, GitHub

## Analysis Performed
1. **Data import and understanding** – shape, columns, data types, numerical and categorical columns, basic statistics
2. **Data cleaning** – `TotalCharges` converted from text to numbers (11 blanks, all new customers with tenure 0, filled with 0); no duplicates; no invalid values
3. **Feature analysis** – distributions, minimum, maximum and average values, important categories, IQR outlier check (the only "outliers" flagged are in the 0/1 `SeniorCitizen` column, which is not a real outlier problem)
4. **Correlation analysis** – correlation matrix and heatmap
5. **Visualization** – 15 charts (histogram, bar, count, pie, scatter, line, box, violin, heatmap, pair plot, distribution plot, area chart)
6. **Business insights** – 15 insights backed by numbers from the data
7. **Recommendations** – 5 practical, evidence-based recommendations

## Key Findings
- 26.5% of customers (1,869 of 7,043) have churned.
- Month-to-month contracts churn at 42.7%, against 11.3% (one year) and 2.8% (two year). They make up 88.6% of all churners.
- Tenure has the strongest correlation with churn (-0.35). Churn falls from 47.4% in the first 12 months to 6.6% after 60 months.
- Fiber optic customers churn at 41.9% (DSL 19.0%) and pay more on average ($91.50 vs $58.10).
- Electronic check users churn at 45.3%, against 15-19% for other payment methods.
- Customers without online security or tech support churn at about 42%, against about 15% for those with them.
- Gender and phone service make almost no difference to churn.

## Business Recommendations
1. Move month-to-month customers onto one- or two-year contracts with a small incentive.
2. Run a first-year retention programme with check-ins at months 1, 3 and 6.
3. Review fiber optic pricing and service quality.
4. Encourage electronic check customers to switch to automatic payment.
5. Bundle online security and tech support for at-risk customers.

## Repository Structure
```
DevixoSolutions-Internship/
├── Telco-Customer-Churn.csv      # Dataset
├── requirements.txt
├── README.md
├── EDA_Report.pdf                # Final PDF report
├── EDA_notebook.ipynb            # Full analysis (Parts 1-7)
└── screenshots/                  # Code and output screenshots  
├── graphs/                       # 15 chart images                     
```

## How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/duasajid65-cloud/DevixoSolutions-Internship.git
   cd DevixoSolutions-Internship
   ```
2. Install the libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Start Jupyter and open the notebook:
   ```bash
   jupyter notebook EDA_notebook.ipynb
   ```
4. Keep `Telco-Customer-Churn.csv` in the same folder as the notebook, then choose **Kernel → Restart & Run All**.

You can also upload the notebook and CSV to Google Colab and run all cells.

## Note
The findings describe associations in this dataset and do not prove that any single factor causes churn.
