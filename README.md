# Better-Profit-Strategy
## Problem Statement:
We have access to a specific bank loan data. We have data about all loans asked to the bank, 
whether the bank decided to grant it and, finally, whether the borrower managed to repay it. 
We also have info about the person asking for the loan at the moment she is asking for the 
loan.
We have to come up with a better strategy to grant loans. Specifically, build a 
model which is better than the bank model. 
Assume that:
If you grant the loan and the it doesn’t get repaid, you lose 1.
If you grant the loan and the it does get repaid, you gain 1
If you don’t grant the loan, you gain 0.
Using the rules above, compare bank profitability vs your model profitability.
## DATA DICTIONARY
loan_file - general information about the loan
Columns:
loan_id : the id of the loan. Unique by loan. Can be joined to loan id in the other table
loan_purpose : the reason for asking the loan: investment, other, business, emergency_funds, 
home
date : when the loan was asked
loan_granted : whether the loan was granted
loan_repaid : whether the loan was repaid. NA means that the loan was not granted

borrower_file - information about the borrower
Columns:
loan_id : the id of the the loan. Unique by loan. Can be joined to loan id in the other table
is_first_loan : did she ask for any other loans in her lifetime?
fully_repaid_previous_loans : did she pay on time all of her previous loans? If this is the first 
loan, it is NA
currently_repaying_other_loans : is she currently repaying any other loans? If this is the first 
loan, it is NA
total_credit_card_limit : total credit card monthly limit
avg_percentage_credit_card_limit_used_last_year : on an average, how much did she use of 
her credit card limit in the previous 12 months. This number can be >1 since it is possible to 
go above the credit card limit
saving_amount : total saving amount balance when she asked for the loan
checking_amount : total checking amount balance when she asked for the loan
is_employed : whether she is employed (1) or not (0)
yearly_salary : how much she earned in the previous year
age : her age
dependent_number : number of people she claims as dependen
