# Prosper Loan Data Analysis
## by Suelen Fenali


## Dataset

The dataset is provided by [Prosper](https://www.prosper.com) and contains 81 columns related to many different aspects of a loan. In order to narrow the analysis and focus on some insights, I used only 17 variables. Some of the features were available only after July 2009, so I cleaned the data and from the 113937 loan registries available, I used 84853. The features used are described below:


**BorrowerAPR**: The Borrower's Annual Percentage Rate (APR) for the loan. 

**BorrowerRate**: The Borrower's interest rate for this loan.  

**EstimatedLoss**: Estimated loss is the estimated principal loss on charge-offs. Applicable for loans originated after July 2009. 

**EstimatedReturn**: The estimated return assigned to the listing at the time it was created. Estimated return is the difference between the Estimated Effective Yield and the Estimated Loss Rate. Applicable for loans originated after July 2009. 

**Term**: The length of the loan expressed in months. 

**ProsperRating (Alpha)**: The Prosper Rating assigned at the time the listing was created between AA - HR.  Applicable for loans originated after July 2009. 

**ProsperScore**: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009. 

**ListingCategory (numeric)**: The category of the listing that the borrower selected when posting their listing: 0 - Not Available, 1 - Debt Consolidation, 2 - Home Improvement, 3 - Business, 4 - Personal Loan, 5 - Student Use, 6 - Auto, 7- Other, 8 - Baby&Adoption, 9 - Boat, 10 - Cosmetic Procedure, 11 - Engagement Ring, 12 - Green Loans, 13 - Household Expenses, 14 - Large Purchases, 15 - Medical/Dental, 16 - Motorcycle, 17 - RV, 18 - Taxes, 19 - Vacation, 20 - Wedding Loans 

**Occupation**: The Occupation selected by the Borrower at the time they created the listing. 

**EmploymentStatus**: The employment status of the borrower at the time they posted the listing. 

**EmploymentStatusDuration**: The length in months of the employment status at the time the listing was created. 

**IsBorrowerHomeowner**: A Borrower will be classified as a homowner if they have a mortgage on their credit profile or provide documentation confirming they are a homeowner.

**CurrentDelinquencies**: Number of accounts delinquent at the time the credit profile was pulled. 

**AmountDelinquent**: Dollars delinquent at the time the credit profile was pulled. 

**DelinquenciesLast7Years**: Number of delinquencies in the past 7 years at the time the credit profile was pulled.

**LoanOriginalAmount**: The origination amount of the loan. 

**LoanStatus**: The current status of the loan: Cancelled,  Chargedoff, Completed, Current, Defaulted, FinalPaymentInProgress, PastDue. The PastDue status will be accompanied by a delinquency bucket. 


## Summary of Findings

During the exploratory analysis, I could see that the BorrowerRate, BorrowerAPR  have all values distributed between 0.05 and 0.40, both of them were very similar, and [this](https://www.bankrate.com/finance/mortgages/apr-and-interest-rate.aspx) explains that the BorrowerRate is the borrowers interest with some other fees. So, I chose to use it in the analysis. Some interesting insights that was possible to get from the data is that the highest interest rates are not related to the biggest amounts of money, and the less is the duration of employment the higher is the estimated return variance. Furthermore, loans with bigger amounts have smaller EstimatedLoss rate.
Employment duration is concentrated in a few months (less than 50), however there are different estimated loss rates cross many months, so it shows that there is not a strong relation between this two features. Also, the listings' categories did not show a strong correlation with the borrower APR.
The ProsperScore that is the risk for the loan shows that better risk categories have more homeowners. For example, in the category AA, around 1/3 of the borrowers have a house, while in category HR it's just half. The score also illustrates that better risk categories have less delinquent borrowers. In the category AA, only 5% of the borrowers have delinquencies, while in category HR around 25% are delinquent.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.