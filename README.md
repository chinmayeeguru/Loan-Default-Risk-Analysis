# Loan Default Risk Analysis


# INTRODUCTION

This case study aims to give an idea of applying EDA in a real business scenario. In this case study, we will apply the EDA techniques towards developing a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

This case study aims to identify patterns which indicate if a client has difficulty paying their instalments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. 

This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

# CURRENT APPLICATION DATA

Inspection & Cleaning

After reading and inspecting the dataset, we performed missing data analysis and the below points can be considered towards missing data imputation:
- Columns with more than 50% missing data can be dropped 
- Columns with 13% or lower missing values, can be imputed with mode, median or mean depending on the type of the column and data distribution
- Categorical columns with > 20% but < 50% missing data can have a new type such as ‘Unknown’ for missing data imputation.

Data type correction

- The columns representing the number of enquires to Credit Bureau about the client are of float data type. We can change the data type to int.
- DAYS  related columns and CNT_FAM_MEMBERS can be changed to int data type as they represent number of days  and family member count respectively.

Data Standardization

- DAYS  related columns have some negative values. They can be replaced with their respective absolute values.
- We can create a new column based on DAYS_BIRTH to show the age of the applicant for better readability and then we can drop the DAYS_BIRTH column. Similarly we can convert the other DAYS columns to represent the value in years.
- The CODE_GENDER column has XNA values that can be replaced with nan.

Outlier Analysis

- AMT_INCOME_TOTAL has very high valued outliers. As we know the income may vary from person to person, we can cap value here and get rid of very high incomes.

![image](https://user-images.githubusercontent.com/103338455/162632598-5fd730c4-50bb-4444-b38a-27fa8d177444.png)

- DAYS_EMPLOYED has huge outliers. Some data points are showing close to 1000 years in service which is impossible. We can cap the value at a desired point after analysing the quantiles.

![image](https://user-images.githubusercontent.com/103338455/162632646-9d0939a5-99db-4f66-bbb9-d2dae0f46480.png)






