# Loan Default Risk Analysis Dashboard

A Power BI project I built to explore loan default risk — basically trying to understand which kind of applicants are more likely to default, and what patterns show up around income, credit score, employment type, and age.

The dashboard has 3 pages:

**1. Loan Default & Overview**
Gives a general picture — loan amount by purpose, average income by employment type, default rate by employment type, average loan by age group, and how default rate has moved year over year.

**2. Applicant Demographics & Financial Profile**
Digs into who the applicants actually are — credit score distribution, loan amounts by marital status and age group, how mortgage/dependents status affects loans, and loans broken down by education level.

**3. Financial Risk Metrics**
The more "risk" focused page — YoY change in loan amount and defaults, YTD loan amount by credit score bucket, and a decomposition tree to see what's actually driving loan amounts.

## Data used

Everything is built off one main table, `Loan_default`, which has the loan-level data (loan amount, purpose, employment type, credit score, marital status, mortgage/dependents flags, education, income bracket, year, default status).

I kept the measures split into separate tables (`Measures Table`, `Measures Table 2`, `Measures Table 3`) instead of dumping them all in one place — made it easier to manage since each set roughly maps to one page.

## Built with

- Power BI Desktop
- DAX for the measures (YoY, YTD, averages, medians, default rates)

## Running it

Clone the repo and open the `.pbix` in Power BI Desktop:

```bash
git clone https://github.com/Piyush-Pundir/Loan-Default-Risk-Analysis-Dashboard.git
```

Once it's open, just move between the 3 tabs at the bottom. On the last page, click into the decomposition tree to explore what's driving loan amount up or down.

## Author

Piyush Pundir
