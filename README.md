# Employee Reimbursement Analysis Dashboard

## Overview
This Power BI project focuses on cleaning, transforming, and analyzing employee reimbursement data using Power Query and DAX.

The project includes:
- Data cleaning
- Currency transformation
- DAX measures
- Interactive dashboard visuals

---

## Tools Used
- Power BI
- Power Query
- DAX

---

## Dataset Features
The dataset contains:
- Employee Names
- Project Names
- Expense Types
- Currency Details
- Reimbursement Amount
- Request Status

---

## Tasks Performed

### Data Cleaning
- Corrected spelling and punctuation errors in the Expense Type column
- Standardized inconsistent Project Names

### Currency Handling
- Filled missing currency values using conditional logic:
  - Amount >= 1000 → INR
  - Amount < 1000 → USD

### Currency Conversion
- Converted reimbursement amounts into INR based on currency values

### DAX Measures Created
- Total Reimbursed Amount
- Project_B Reimbursement Amount
- Declined Request Count

---

## Power Query Formula

### Conditional Currency Logic
```powerquery
if [Currency] = null and [Amount] >= 1000 then "INR" 
else if [Currency] = null and [Amount] < 1000 then "USD" 
else [Currency]
