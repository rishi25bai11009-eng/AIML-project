# CreditWise Loan System
## Problem Statement
A mid-sized financial company named SecureTrust Bank offers personal and home loans to customers across urban and rural regions of India. Every day, hundreds of customers apply for loans through online and branch applications.

Until now, SecureTrust Bank has been using a manual verification processwhere loan officers evaluate applications by checking income proofs, employment details, credit history, and other documents. This process is time-consuming, biased & inconsistent.

As a result, the bank faces two major challenges:

1.Good customers sometimes get rejected, leading to loss of business.

2.High-risk customers sometimes get approved, leading to financial losses

To solve this problem, the bank wants to introduce an systemintelligent loan approval powered by Machine Learning that can automatically analyse applicant details and  
predict whether a loan should be Approved or Rejected human verification.

You are hired as a Machine Learning Engineer before final to design and develop this intelligent system using historical loan application data. The system must learn hidden patterns from previous customer records and provide accurate, fast, and unbiased loan approval decisions.

## 📊 Dataset Description

| Column               | Description                                      |
|---------------------|--------------------------------------------------|
| Applicant_ID        | Unique applicant ID                              |
| Applicant_Income    | Monthly income of applicant                      |
| Coapplicant_Income  | Monthly income of co-applicant                   |
| Employment_Status   | Salaried / Self-Employed / Business              |
| Age                 | Applicant age                                    |
| Marital_Status      | Married / Single                                 |
| Dependents          | Number of dependents                             |
| Credit_Score        | Credit bureau score                              |
| Existing_Loans      | Number of already running loans                  |
| DTI_Ratio          | Debt-to-Income ratio                             |
| Savings             | Savings balance                                 |
| Collateral_Value    | Value of collateral provided                     |
| Loan_Amount         | Loan amount requested                            |
| Loan_Term           | Loan duration (months)                           |
| Loan_Purpose        | Home / Education / Personal / Business           |
| Property_Area       | Urban / Semi-Urban / Rural                       |
| Education_Level     | Graduate / Postgraduate / Undergraduate          |
| Gender              | Male / Female                                    |
| Employer_Category   | Govt / Private / Self                            |
| Loan_Approved       | 1 = Approved, 0 = Rejected                       |

## Dataset Source

The dataset used in this project is a synthetic dataset created and modified for educational purposes to simulate real-world loan approval scenarios.
The dataset is included in this repository as loan_approval_data.csv.

## Exploratory Data Analysis (EDA)

1. Loan Approval Distribution (Pie Chart)

A pie chart is used to visualize the distribution of Loan Approved (Yes/No).

Insight:

Helps identify whether the dataset is balanced or imbalanced.

If one class dominates, the model may become biased toward that class.

🔹 2. Education Level Distribution (Bar Plot)

A bar plot shows counts of different Education Levels.

Insight:

      Reveals the most common education category among applicants.
      
      Helps understand whether education plays a role in loan approval (to be validated later).

🔹 3. Applicant Income Distribution (Histogram)

Histogram plotted for Applicant_Income.

Insight:

       Data is right-skewed (few applicants with very high income).

       Majority of applicants fall in a lower to mid income range.

Indicates possible outliers.

🔹 4. Coapplicant Income Distribution (Histogram)

Histogram for Coapplicant_Income.

Insight:

     Many values are zero or low, meaning many applicants may not have coapplicants.

     Distribution is also skewed.

🔹 5. Applicant Income vs Loan Approval (Boxplot)

Boxplot comparing income across loan approval status.

Insight:
       
       Approved applicants tend to have slightly higher median income.
       Presence of outliers in both approved and rejected groups.

🔹 6. Multiple Financial Features vs Loan Approval (Boxplots Grid)

Features analyzed:

Applicant Income

Credit Score

DTI Ratio

Savings

Insights:

Credit Score:

          Strong separation → higher scores → more approvals ✅

Ratio (Debt-to-Income):

         Lower DTI → higher approval chances ✅

Savings:

       Higher savings correlate with loan approval

Applicant Income:
  
                Influence exists but not as strong as credit score

🔹 7. Credit Score vs Loan Approval (Histogram with Hue)

Histogram with Loan_Approved as hue.

Insight:
    
      Clear pattern:
             Higher credit score → mostly approved
             Lower credit score → mostly rejected
Strongest predictor in dataset

🔹 8. Applicant Income vs Loan Approval (Histogram with Hue)

Histogram comparing income distribution for approved vs rejected loans.

Insight:
      
        Overlap exists between approved and rejected groups
        income alone is not sufficient to decide approval
        Works better combined with other features

🔹 9. Correlation Heatmap

Heatmap showing correlation between numerical features.

Insight:

     Identifies relationships between variables
Helps in:

     Feature selection
     Detecting multicollinearity
     Likely strong correlations:
     Credit Score ↔ Loan Approval
     Financial indicators ↔ each other

  
