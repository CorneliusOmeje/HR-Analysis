# HR-Analysis

## Project Overview

This Data Analsis project aims to generate actionable insights from the employee records to enhance performance and make better decision from the Employee data.
By analyzing various aspect of the sales data, i seek to identify:
- How many Employees are working in the organisation,
- What are percentages of Male and Female Employees,
- How many years has each Employee been with the Organisation,
- Determine the total number of employees due for promotion,
- How far is the Employee's residence from the company,
- What percentage of Employees are to be retrenched.

<img width="1251" height="771" alt="Screenshot 2025-10-31 040049" src="https://github.com/user-attachments/assets/71dafc91-5505-441e-88b5-22cb22326632" />

## Data Sources
Employee Data: The primary dataset used for this analysis is "HR Analytics Data" CSV file, containing detailed information of each sales made by the company.  [HR Analytics Data.csv](https://github.com/user-attachments/files/23250019/HR.Analytics.Data.csv)

## Analysis Tools Used
- Microsoft Excel
- Power Query
- Power Pivot
- Power BI

## Data Cleaning and Preparation
In the initial Data Cleaning and Preparation Phase, i performed the following tasks:
1. Imported the data using power query
2. Used Power query to transform and add additional columns
3. Unpivoted the datasets
4. Performed value replacement
5. Removed Duplicates
6. Handled Blanks and Trimmed Spaces

<img width="1238" height="779" alt="Screenshot 2025-10-31 040228" src="https://github.com/user-attachments/assets/e25eff06-ed2c-4abc-8b0e-4d32c5ace804" />

## Data Analysis
Power Pivot was used for creating some measures using DAX Funcions. Some of the measures used for these analysis include:
``` Sql
Male = CALCULATE([Total Emp],'HR Analytics Data'[Gender]="Male")
```
``` Sql
Female = CALCULATE([Total Emp],'HR Analytics Data'[Gender]="Female")
```
``` Sql
To be retrenched = IF(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Retrenchment]="To be retrenched")),0,CALCULATE([Total Emp],'HR Analytics Data'[Retrenchment]="To be retrenched"))
```
``` Sql
Due for Promotion = IF(ISBLANK(CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="Due for promotion")),0,CALCULATE([Total Emp],'HR Analytics Data'[Promotion Status]="Due for promotion"))
```
``` Sql
% High Rating = DIVIDE([High Emp Rating],[Total Emp],0)

## Findings
 The analysis results are summarized as follows:
1. 60% of the Employeees are Male.
2. 40% of the Employee are Female.
3. Majority of the Employees are in Level 1 & 2.
4. 63.95% of the Employeees are staying very close to the office.
5. 15.58% summarized Employees living very far from office.
6. Only 4.9% of the Employees are due for promotion.
