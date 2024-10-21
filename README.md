# Lending Club Case Study
> The purpose of this project is to analyze the loan data from Lending Club, a peer-to-peer lending platform, to identify significant trends and factors influencing the loan status of borrowers. By performing extensive exploratory data analysis (EDA) and developing a predictive model, we aim to gain insights into the features that lead to loan defaults.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
## Objective
The main objective of this analysis is to:
- Understand the factors that contribute to loan defaults.
- Analyze the key factors affecting loan repayment using both univariate and bivariate analysis.
- Build predictive models to classify the loan status of borrowers.
- Provide business insights to help reduce defaults by highlighting risk factors.

## Dataset
The dataset used for this project contains detailed loan records of borrowers from the Lending Club platform. It includes both categorical and numerical features, such as loan amount, interest rate, employment status, and loan grade.

### Key Features:
- **loan_amnt:** The loan amount applied by the borrower.
- **int_rate:** The interest rate on the loan.
- **annual_inc:** The borrower's annual income.
- **loan_status:** The final status of the loan (fully paid, charged off, etc.).
- **grade and sub_grade:** Lending Club's internal grading system.
- **emp_title:** Job title of the borrower.
- **term:** Duration of the loan (in months).
- **purpose:** The stated reason for the loan (e.g., debt consolidation, home improvement).

## Approach
### Data Preprocessing:
- **Handling Missing Data:** Rows with significant missing values were either removed or imputed.
- **Derived Metrics:** Created new metrics like issue_month, issue_year from existing data.
- **Data Transformation:** Log-transformed features like `annual_inc` and `revol_bal` to handle skewness in the data.
- **Outliers:** Identified and handled outliers in continuous variables to improve model robustness.
  
### Exploratory Data Analysis (EDA):
- **Univariate Analysis:** Studied the distribution of key numerical features such as `loan_amnt`, `annual_inc`, and `int_rate` using histograms and boxplots.
- **Bivariate Analysis:** Analyzed the relationship between `loan_status` and other features like `int_rate`, `annual_inc`, and `purpose` using stacked bar plots and correlation heatmaps.
- **Categorical Feature Analysis:** Examined categorical features such as `grade`, `home_ownership`, and `verification_status` to understand their influence on loan defaults.

### Business Problem:

The core business problem revolves around making **accurate loan approval decisions** to balance risk and profitability for a consumer finance company. The company must decide whether to approve or deny a loan application based on the applicant's likelihood of repaying the loan. Two critical types of risks are associated with this decision:

1. **Risk of Loss of Business (False Negative):**
   - If the company **rejects a loan application** from an applicant who would have repaid the loan, it results in a **missed opportunity** and **loss of potential business**.
   
2. **Risk of Financial Loss (False Positive):**
   - If the company **approves a loan** for an applicant who is likely to default, it risks **financial loss** due to loan default.

#### Objective:
The business needs to **minimize financial losses** while **maximizing profitable loan approvals** by accurately identifying applicants who are likely to default. The aim of the analysis is to:
- **Identify patterns and risk factors** associated with loan defaults.
- **Improve decision-making** for loan approval based on the applicant’s profile.
- Take strategic actions like denying loans, reducing the loan amount, or charging higher interest rates for high-risk applicants, to **mitigate risks**.

In summary, the business problem is about optimizing the **loan approval process** to **reduce default rates** while **maximizing revenue** for the company, by making data-driven lending decisions.

## Conclusions
- ### Conclusion:

Based on the analysis of the key driver variables, we can conclude that certain factors significantly influence the likelihood of loan defaults. These findings can help the company in making data-driven decisions to mitigate risks associated with loan defaults:

1. **Loan Amount:**
   - Higher loan amounts are associated with an **increased likelihood of default**. This suggests that borrowers who take larger loans may face more financial strain, leading to a higher risk of non-repayment.

2. **Interest Rate:**
   - Loans with **higher interest rates** are more prone to default. Borrowers with higher interest rates may have a lower creditworthiness, leading to higher risks for the company.

3. **Loan Term:**
   - Loans with a **60-month term** are at a **higher risk of default** compared to loans with a 36-month term. Longer repayment periods may create more opportunities for financial distress over time.

4. **Grade:**
   - **Loan defaults gradually increase** as the grade worsens from **A to G**. Loans with higher grades (closer to A) tend to perform better, whereas loans with grades closer to G are riskier.

5. **Sub-grade:**
   - Similar to the overall grade, **sub-grade** analysis reveals that **loan defaults increase** as the sub-grade worsens from **A1 to G5**, with some exceptions. This provides a more granular view of creditworthiness.

6. **Loan Purpose:**
   - Certain loan purposes, specifically **small business loans**, exhibit a **higher risk of default**. This could be due to the volatility and risk associated with small businesses.

7. **Address State:**
   - **NE state loans** (loans issued to borrowers in Northeastern U.S. states) appear to be at a **higher risk of default** compared to loans in other regions. This may point to region-specific economic factors affecting borrowers' ability to repay.

In summary, by considering these driver variables in the loan approval process, the company can implement more effective risk mitigation strategies, such as adjusting loan terms, interest rates, or even denying loans in cases of high risk. These actions will help minimize financial losses and optimize loan portfolio performance.


## Technologies Used

- **Python**: The primary programming language used for data analysis and model development.
- **Pandas (version 1.3.3)**: For data manipulation and preparation, including handling missing values, feature engineering, and transforming the dataset.
- **NumPy (version 1.21.2)**: For numerical computations, used primarily for array operations and statistical calculations.
- **Matplotlib (version 3.4.3)**: For data visualization, used to create plots such as histograms, boxplots, and bar charts.
- **Seaborn (version 0.11.2)**: High-level visualization library based on Matplotlib, used for statistical graphics like heatmaps and count plots.
- **Jupyter Notebook**: For writing and organizing the code, visualizations, and documentation interactively.

These technologies helped efficiently process, visualize, and analyze the data, providing key insights into loan default patterns.

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements

- This project was inspired by the **Lending Club** case study, which provides real-world data on loan applicants and their repayment behavior.
- Special thanks to the **UpGrad Data Science Program** for providing the framework and guidance for this project.
- References: 
  - **Lending Club Loan Data** from [LendingClub.com](https://www.lendingclub.com/info/download-data.action) was the primary source for the dataset.

## Contact
Created by [@kamit1983] - feel free to contact me!
co authored by [@kc11381]
