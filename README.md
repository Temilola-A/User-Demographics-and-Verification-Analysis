# User Demographics and Verification Analysis

### Table Of Content

- [Project Overview](#project-overview)
  
- [Data Sources](#data-sources)
  
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
  
- [Exploratory Data Analysis](exploratory-data-analysis)
  
- [Results and Findings](results-and-findings)
  
- [Recommendations](#recommendations)
  
- [Limitations and References](limitations-and-references)
  

  ## Project Overview

![image](https://github.com/user-attachments/assets/be481258-e6fd-48fd-ba73-80f4d7e9c52a)


  This project was focused on analyzing user and transaction data from a fintech platform to gain insights into user demographics, verification status, and transaction behaviours. The objective was to import raw data into a Excel, perform data analysis, and develop an interactive and insightful dashboard using PowerBi for stalkholders.

  ## Data Sources
  
  - Users Dataset : CSV file containing user information such as gender, age, occupation, country of residence, verification status and registration date.

  - Transactions Dataset : CSV file with details on transactions including base amount, send currency, recieve currency, currency corridor, and transaction timestamps.
 
    ## Tools and Technologies Used

 ### Excel [Download here](http://microsoft.com)
    - For data import, transformation, and validation.
    - For preliminary and inspection and metadata review.

  ### Microsoft PowerBI
  - For vizualization and dashboard development.

## Data Cleaning and Preparation 
- Merged sheets
- Normalized columns
- Calculated fields
- Handling Nulls and Outliers
- Saved Clean File


## Exploratory Data Analysis (EDA)
EDA was conducted in power BI with summary metrics and quick vizuals to understand:
- Distribution of users by gender, country, and age group.
- Volume and count of transactions over time
- Most frequent currency corridors
- Verification and KYC trends
- Occupation trends

  Calculate the total users, total verified users, total non verified userS and Active users

![image](https://github.com/user-attachments/assets/f76b9ad4-8fdc-448c-a0a3-bfb5ad715be8)

Total Users by Age Bracket

![image](https://github.com/user-attachments/assets/9d47d203-28e8-4222-9964-07d5fc1c7e06)

Total User by Gender

![image](https://github.com/user-attachments/assets/b77f1fa4-a959-4fb5-8019-f3a6de8ad275)

Total User by occupation

![image](https://github.com/user-attachments/assets/1ae45468-7b02-4224-a3f4-8dc401302989)

Total Users by Residence Country

![image](https://github.com/user-attachments/assets/a9e718a8-7a1e-4b21-9d0f-d37bf58d11e0)



  ## Data Modelling and Analysis im Power BI

- #### Linked Users and Transactions by UserID
    
- #### Key DAX Measures:
- TotalUsers = DISTINCTCOUNT (Users[UserID])
    
 - VerifiedUsers = CALCULATE ([TotalUsers] , Users[KYCStatus] = "Passed")
 
 - TotalVolume = SUM(Transactions[BaseAmount])
 
 - AvgTransaction = AVERAGE(Transactions[BaseAmount])
 
- Time intelligence for new users/ transactions over days, weeks, months
    
 
    ## Results and Key Findings

    | Metrics | Value |
    |---------| ------|
    |Total Users | 22,000 |
    | Verified Users | 4,375 (20%) |
    | Unverified Users | 17,624 (80%) |
    | Top Residence Country | Nigeria (16.3K; 74%)
    | Gender Split | M 58%, F 22%, NB 19% |
    | Age 18-34 | 65% of users |
    | Total Transaction Volume Amount | 60M |
    | Avg. Transaction Amount | 366.86 |
    | Active Users in Q1 | 16,000 |
    | Top Currency Corridor | CAD-NGN (30 M+) |

  Behavioral Insights : Peaks in transaction volume mid-week and at month-ends.
  Occupation Insight : 4.1K students and 1.8K business owners driving the user base.

  ## Limitations

  - The analysis was based solely on the available user and transaction data. Additonal datasets (e.g., user feedback, failed transaction logs, or session logs) could have provided deeper insights into user behaviour and transaction issues.
  - Missing Regions: Zero data from some countrires__ possible collection issues.
  - Time Scope: Only January - March 2024 __No seasonal trends beyond Q1.

Here is the link to the Dashboard [Downlaod here](https://app.powerbi.com/view?r=eyJrIjoiMjUxNDEzMjItMzcxNS00NzlkLTgwYmUtYjYyNmMxMmZjNjZiIiwidCI6IjY4ZDBlMjhiLTg3NTUtNDgzMi1iM2JjLWRhOGQwNjM3YzY5ZCJ9)
  

  ## Recommendations

  - KYC Push: Automate reminder and incentiives to convert the 80% unverified.
  - Student and Youth Focus: Tailored offers to loyalty programs for 18-34 segment.
  - Optimize CAD-NGN Flows: Faster settlement, promotional rates, or corridor-specific UX.
  - Expand in Low-Activity Markets: Investigate why Australia/UK show zero activity__ data gap or market opportunity?
  - Weekly Monitoring: Configure Power BI alerts on sharp drops/spikes in users or volume.

😄

💻




 

  
   

    



  







  
