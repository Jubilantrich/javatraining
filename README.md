To combine all three datasets using InsuredRef, you'll need to join the datasets based on the InsuredRef and other relevant fields (like Commencement Date, Loss Date, entdate, etc.). Here's a detailed breakdown of the process to calculate the Loss Ratio and Profitability using your three datasets.

Data Structure:
Production Data: Contains InsuredRef, Commencement Date, Gross, Com Expense.
Claims Paid Data: Contains InsuredRef, entdate, Clm Paid.
Claims Outstanding Data: Contains InsuredRef, Loss Date, clmost.
SQL Query for Loss Ratio and Profitability
1. Loss Ratio Calculation
We need to join the three datasets on InsuredRef and group by the year of the Commencement Date. Then, we'll sum the Claim Paid, Claim Outstanding, and Gross Premium for the calculation.
