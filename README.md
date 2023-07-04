# Lending Club Case Study

## Table of Contents
* [Problem Statement](#problem-statement)
* [Business Objectives](#business-objectives)
* [Data Understanding](#data-understanding)
* [Approach](#approach)
* [Case Study Analysis](#case-study-analysis)
* [Technologies Used](#technologies-used)
* [Summary](#Summary)
* [Team](#team)

<br />

## Problem Statement
The consumer finance company specializes in lending various types of loans to urban customers. When the company receives a loan application, it needs to make a decision on loan approval based on the applicant's profile. There are two types of risks associated with the company's decision:

1. If the applicant is likely to repay the loan, not approving the loan results in a loss of business.
2. If the applicant is likely to default, approving the loan may lead to a financial loss for the company.

The aim of this case study is to identify patterns in the data that indicate if a person is likely to default on the loan. By understanding the consumer attributes and loan attributes that influence the tendency of default, the company can take appropriate actions such as denying the loan, reducing the loan amount, or lending to risky applicants at a higher interest rate.
 
<br />

## Business Objectives
1. Identify risky loan applicants and reduce the amount of credit loss.
2. Understand the driving factors behind loan default to inform portfolio and risk assessment.

In other words, *the company wants to understand the driving factors (or driver variables)* behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment. 

<br />

## Data Understanding
The dataset contains information about past loan applicants and whether they defaulted on the loan or not. The dataset includes various attributes such as loan amount, interest rate, employment details, credit history, and borrower's demographic information. The dataset covers the time period from 2007 to 2011.

<br />

### *Analysis based on Domain Understanding*
Based on domain understanding in the field of risk analytics and lending, here is an analysis based on data understanding:

*1. Loan Status Distribution:*<br> The loan dataset provides information about the loan statuses, including fully paid, current, and charged-off loans. Understanding the distribution of loan statuses is crucial for risk assessment and portfolio management. By analyzing the proportion of different loan statuses, lenders can identify the potential areas of risk and focus on reducing default rates.

*2. Loan Amount Analysis:*<br> The loan amount is an important factor that affects the risk associated with lending. Higher loan amounts may indicate a higher risk of default, as borrowers may struggle to repay larger sums. Analyzing the distribution and characteristics of loan amounts can help lenders determine the maximum loan limits they are comfortable with and identify potential risk thresholds.

*3. Loan Grade and Interest Rate Analysis:*<br> Loan grade and interest rate are significant factors in risk assessment. Loans with lower grades and higher interest rates generally carry higher default risk. Analyzing the distribution of loan grades and interest rates can help lenders assess the risk associated with different loan segments and price loans accordingly.

*4. Employment Length Analysis:*<br> The length of employment of borrowers provides insights into their stability and ability to repay loans. Analyzing the distribution of employment lengths can help lenders understand the risk associated with borrowers at different stages of their careers. It can also inform decision-making regarding lending criteria based on employment length.

*5. Loan Purpose Analysis:*<br>The purpose of a loan can provide insights into the risk profile of borrowers. Different loan purposes may have varying levels of default risk. Analyzing the distribution of loan purposes can help lenders identify high-risk segments and tailor lending strategies accordingly.

*6. Loan Term Analysis:*<br> Loan term refers to the duration of the loan. Longer loan terms may carry higher default risk, as borrowers have a more extended period to encounter financial difficulties. Analyzing the distribution of loan terms can help lenders evaluate the trade-off between loan duration and default risk.

By conducting these analyses based on domain understanding, lenders can gain insights into the key factors that impact loan default and make data-driven decisions to minimize risk and optimize lending strategies. It allows lenders to identify potential patterns, relationships, and risk indicators within the dataset, enabling them to develop effective risk assessment models and make informed lending decisions.

<br />

### *Columns Analysis of the Dataset*
Based on the columns present in the loan dataset, let's analyze each column and understand its significance in the context of risk analytics and lending:

*1. Loan ID:* This column represents a unique identifier for each loan. It may not have direct significance in risk analytics but can be used for data management and tracking purposes.

*2. Loan Status:* This column indicates the current status of the loan, such as fully paid, charged-off, or current. It is a critical variable for risk analytics as it provides information on the loan's repayment status and default risk.

*3. Loan Amount:* This column represents the amount of money borrowed by the borrower. It is an important variable in risk assessment as higher loan amounts may pose a higher risk of default.

*4. Loan Term:* This column indicates the duration of the loan in months. The loan term affects the repayment period and can provide insights into the borrower's ability to manage long-term financial obligations.

*5. Interest Rate:* This column denotes the interest rate assigned to the loan. Higher interest rates are generally associated with higher-risk loans. Analyzing the interest rate distribution can help lenders assess the risk profile of borrowers.

*6. Installment:* This column represents the monthly installment amount that the borrower needs to pay. It is influenced by the loan amount, interest rate, and loan term. Understanding the installment amount helps evaluate the borrower's capacity to make regular payments.

*7. Grade:* The loan grade indicates the risk classification assigned to the loan based on the borrower's creditworthiness. It is an important variable in risk assessment and helps in determining interest rates and loan terms.

*8. Sub Grade:* This column provides further sub-classification within each loan grade, providing more granularity in assessing the borrower's risk profile.

*9. Emp Length:* This column represents the length of employment of the borrower in years. It provides insights into the stability of the borrower's income source and their ability to repay the loan.

*10. Home Ownership:* This column indicates the type of home ownership, such as own, mortgage, or rent. It can provide insights into the borrower's financial stability and commitment to homeownership.

*11. Annual Income:* This column represents the annual income of the borrower. It is a significant variable in risk assessment as it reflects the borrower's financial capacity to repay the loan.

*12. Verification Status:* This column indicates whether the income source of the borrower has been verified or not. It provides information on the reliability of the borrower's stated income.

*13. Purpose:* This column represents the purpose of the loan, such as debt consolidation, credit card refinancing, or home improvement. It helps lenders understand the intended use of funds and evaluate the risk associated with different loan purposes.

*14. State:* This column represents the borrower's state of residence. It can provide insights into geographical factors that may influence loan default rates.

*15. DTI:* The Debt-to-Income (DTI) ratio represents the borrower's debt obligations relative to their income. It helps assess the borrower's ability to manage additional debt and is an essential factor in risk analysis.

*16. Delinquency 2 Years:* This column indicates the number of times the borrower has been delinquent on payments in the past two years. It provides insights into the borrower's payment behavior and credit history.

*17. Inquiries 6 Months:* This column represents the number of credit inquiries made by lenders in the past six months. It provides insights into the borrower's recent credit-seeking activity, which can impact their creditworthiness.

*18. Open Accounts:* This column denotes the number of open credit accounts that the borrower currently has. It provides insights into the borrower's credit utilization and financial management.

*19. Revolving Balance:* This column represents the total amount of revolving credit that the borrower currently owes. It helps assess the borrower's existing debt

<br />

### *Ignored Rows and Columns because of missing data*
Based on the data understanding, there may be certain rows and columns in the loan dataset that are ignored or excluded from the analysis due to missing data. Here are some common scenarios where rows or columns may be ignored:

*1. Missing Rows:* Rows that contain missing values or have incomplete information may be excluded from the analysis. This is done to ensure data integrity and to avoid bias in the analysis.

*2. Missing Columns:* Columns that have a significant number of missing values or provide redundant or irrelevant information may be ignored. These columns may not contribute to the analysis or may introduce noise in the results.

*3. Irrelevant Columns:* Columns that are not relevant to the analysis objectives or do not provide meaningful insights may be excluded. These columns may include irrelevant identifiers or information that does not impact the risk assessment or lending decisions.

*4. Redundant Columns:* Columns that provide redundant information, such as duplicate or highly correlated variables, may be ignored to simplify the analysis and avoid multicollinearity issues.

*5. Incomplete Time Periods:* If the dataset covers a specific time period and there are missing data points within that period, those incomplete time periods may be excluded from the analysis to ensure consistency and accuracy.

*6. Low Variance Columns:* Columns with very low variance, indicating little or no variability in values, may not provide useful information and can be ignored.

It is important to carefully consider the impact of ignoring rows or columns on the analysis and ensure that the remaining data is representative and sufficient for drawing meaningful conclusions. Data preprocessing techniques such as imputation or data augmentation may also be applied to handle missing data and salvage valuable information before excluding any rows or columns.

<br />

## Approach
- Perform Exploratory Data Analysis (EDA) to understand the data and identify patterns.
- Analyze the distribution of variables, handle missing values, and perform data cleaning if necessary.
- Conduct univariate analysis to understand the distribution of individual variables.
- Perform bivariate analysis to explore the relationship between variables and default status.
- Identify significant variables that strongly indicate default.
- Summarize the important results and insights from the analysis.
- Develop a presentation to present the analysis approach, results, and insights.

<br />

## Case Study Analysis

After performing exploratory data analysis (EDA) on the loan dataset, several conclusions and insights can be derived. Here are some key findings:

### *Univariate Analysis Inferences:*
From the univariate analysis of the loan dataset, we can draw the following inferences:

1. Loan Status:<br> 
The majority of loans in the dataset are fully paid (around 80%), followed by current loans and charged-off loans. This indicates that the company has a relatively low default rate.

2. Loan Amount:<br> 
The loan amount ranges from a few thousand to a maximum of 40,000. The distribution of loan amounts is right-skewed, with a higher concentration of loans in the lower amount range. This suggests that the company primarily provides smaller loans.

3. Loan Grade:<br> 
The loan grades range from 'A' to 'G', with 'A' being the highest grade representing lower risk. The dataset has a higher number of loans with grades 'B' and 'C', indicating that the company mostly lends to borrowers with moderate creditworthiness.

4. Interest Rate:<br> 
The interest rates assigned to loans range from 5.31% to 30.99%. The distribution is approximately normally distributed, with a peak around 10% to 15% interest rate. Higher interest rates are typically associated with riskier loans.

5. Employment Length:<br> 
The length of employment of borrowers ranges from less than 1 year to over 10 years. The majority of borrowers have an employment length of more than 1 year, suggesting that the company prefers lending to individuals with stable employment.

6. Loan Purpose:<br> 
The dataset includes various loan purposes, such as debt consolidation, credit card refinancing, home improvement, and others. Debt consolidation is the most common loan purpose, followed by credit card refinancing and home improvement.

7. Loan Term:<br> 
Loan is granted to applicants for all purposes either for 36 months or 60 months. debt_consolidation lead high in both the terms followed by credit_card.Most of the loan applicants are given 36 months for the loan term.

These inferences provide an overview of the loan dataset and highlight important characteristics of individual variables. They serve as a starting point for further analysis and can help identify potential patterns and relationships between variables in subsequent bivariate or multivariate analyses.

<br />

### *Bivariate Analysis Inferences:*
Bivariate analysis explores the relationship between two variables in the loan dataset. Here are some inferences from bivariate analysis:

1. Loan Status and Loan Grade:<br>
There is a strong association between loan status and loan grade. Higher-grade loans (grades 'A' and 'B') have a higher proportion of fully paid loans, while lower-grade loans (grades 'D' and below) have a higher proportion of charged-off loans. This suggests that loan grade is a good indicator of loan default risk.

2. Annual income vs Chargedoff Proportion:<br>
Income range 80000+  has less chances of charged off. Income range 0-20000 has high chances of charged off. Notice that with increase in annual income charged off proportion got decreased.

3. Puprose of loan and Loan amount:<br> 
The purpose of the loan has a significant impact on the loan amount. Certain loan purposes tend to have higher average loan amounts, indicating a greater financial need or investment value associated with those purposes.

4. Loan Amount and Interest Rate:<br>
There is a positive relationship between Loan Amount and Interest Rate. As the loan amount increases, the interest rate tends to be higher. This suggests that lenders may charge higher interest rates for larger loan amounts to compensate for the increased risk associated with larger loans.

5. DTI and Interest Rate:<br>
There is a positive relationship between the DTI ratio and the Interest Rate. As the DTI ratio increases, the Interest Rate tends to be higher. This suggests that borrowers with higher DTI ratios, indicating a higher level of debt relative to income, are perceived as higher risk borrowers by lenders, resulting in higher interest rates.

6. Grade and Interest Rate:<br>
Lower-grade loans are associated with higher default risk. Lenders compensate for this increased risk by charging higher Interest Rates to protect their investment. Higher Interest Rates on lower-grade loans act as a risk premium to cover potential losses in case of default.

7. Purpose and Interest Rate:<br>
 The purpose of the loan provides insights into the borrower's intended use of the funds and their financial situation. Lenders assess the risk associated with each loan purpose and adjust the interest rate accordingly. Higher-risk loan purposes may be charged higher interest rates to compensate for the increased likelihood of default.

8. Recoveries and Annual income<br>
Higher percentage of loan amount is recovered when annual income is high. Plot shows no significant variation but there is slight increase in recovery percentage with increase in annual income.

These inferences highlight the relationships and dependencies between different variables in the loan dataset. By understanding these relationships, lenders can make informed decisions about loan approvals, interest rates, and risk assessment to minimize the risk of default and financial loss.

<br />

## Technologies Used
- [Python]
- [numpy]
- [pandas]
- [matplotlib]
- [seaborn]
- [Jupyter Notebook]
- [Anaconda]

<br />

## Summary
- The lending club case study focuses on a consumer finance company that specializes in lending various types of loans to urban customers.
- The company receives loan applications and makes decisions on loan approvals based on the applicant's profile, considering the risk associated with each applicant.
- Two types of risks are involved: approving a loan to an applicant who is likely to default, resulting in a financial loss, and not approving a loan to an applicant who is likely to repay, resulting in a loss of business.
- The goal of the case study is to identify patterns and indicators of loan default using exploratory data analysis (EDA).
- EDA is performed on a loan dataset containing information about past loan applicants and their loan repayment status.
- The dataset includes attributes such as loan grade, annual income, loan amount, interest rate, purpose of the loan, and more.
- Univariate analysis is performed to understand the distribution and characteristics of individual variables.
- Bivariate analysis is performed to understand the relationship between two variables, such as loan status and loan grade, annual income and charged-off proportion, purpose of the loan and loan amount, etc.
- The findings from the analysis can be utilized by the lending company to make informed decisions on loan approvals, interest rates, and risk assessment.
- The case study highlights the importance of EDA in understanding risk analytics in the banking and financial services industry.

<br />

## Team
* [Surjeet Haldar](https://www.linkedin.com/in/surjeethaldar/)
* [Abhishek Ranjan](ranjanabr@gmail.com)
