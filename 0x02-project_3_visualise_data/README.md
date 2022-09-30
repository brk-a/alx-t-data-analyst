# Exploration and Analysis of Loans Data from Prosper

## by F Njakai 

| [Github](https://www.github.com/brk-a)
| [LinkedIn](https://www.linkedin.com/in/francis-n-6b61b2a0)


## Dataset

[Prosper](https://www.prosper.com/) is a peer-to-peer lending marketplace in the US. Borrowers apply online for a fixed-rate, fixed-term loan between USD 2,000.00 and USD 40,000.00. Individuals, like you and I, and institutions, Sequoia Capital for example, invest in said loans. Prosper handles all loan servicing on behalf of the borrowers and investors.

The data set to be explored has 113,937 observations (loans, if you like) and 81 variables; detailed information on the variables can be found [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).


## Summary of Findings


### Loans
* average amount borrowed is _c._ USD 8,337.00; the range is USD 1,000.00 to 35,000.00
    * loans of amount USD 5k, 10k, 15k, 20k and 25k have higher-than-average frequency
* average rate is _c._ 0.19%; the range is zero to 0.5%
* the number of loans disbursed changes with time
    * the number fluctuates
        * there are seemingly regular but wide fluctuations
            * fluctuations in the periods Q4 2013 to Q2 2014 inclusive are remarkably wide
        * there are little to no fluctuations starting Q4 2008 to Q3 2009, inclusive (this is exactly 12 months)
    * the number of loans issued appears to increase exponentially despite the fluctuations
    * the average number of loans issued, per annum, between 2005 and 2014 inclusive is _c._ 4.3 million
* an overwhelming majority of loans of all terms are in the range 0.05% to 0.35% borrowing rate
* majority of the tenure of the loans is 3 years or more
* the least funded loans are at 70% funding for all levels of borrowing rate

### Occupations and employment status
* an overwhelming majority of the top ten occupations are [white collar](https://www.investopedia.com/terms/w/whitecollar.asp)
* a majority of the bottom ten occupations, that are not students, are [blue collar](https://www.investopedia.com/terms/b/bluecollar.asp); half of the occupations in the bottom ten are students
* Prosper lends to unemployed applicants

### Income level
* Prosper appears to prefer to lend to high income earners at less-than-average rates
    * the region of high income and low rates is quite dense
    * an overwhelming majority of loans are issued to those whose income level is above USD 25,000.00 _p.a._
        * the top 2 groups account for 55.8% of loans issued 
        * the top 4 groups account for 85.4% of loans issued

### Home ownership status
* there is an almost-even split between those that own a home and those that do not; 50.4% of borrowers own a home

### Location of borrower
* a majority of the states with the least borrowers are from the so-called "[fly-over country](https://en.wikipedia.org/wiki/Flyover_country)"
* all of the states with the most borrowers are on either [seaboard](https://www.oxfordlearnersdictionaries.com/us/definition/english/seaboard)

### Factors that affect the nominal borrowing rate
* there is weak, positive correlation between `BorrowerRate` and `Term` -> _c._ 0.02
* there is weak, negative correlation between
    * `BorrowerRate` and `StatedMonthlyIncome` -> _c._ -0.09
    * `BorrowerRate` and `EmploymentStatusDuration` -> _c._ -0.02
* there is strong, positive correlation between
    * `BorrowerRate` and `BorrowerAPR` -> _c._ 0.99
* none of the variables of interest have a strong, negative correlation

### Factors that affect the number of investors
* none of the variables of interest have a weak, positive correlation
* there is weak, negative correlation between
    * `Investors` and `BorrowerRate` -> _c._ -0.27
    * `Investors` and `PercentFunded` -> _c._ -0.05
* none of the variables of interest have a strong, positive correlation
* none of the variables of interest have a strong, negative correlation


## Key Insights for Presentation

* the number of loans issued appears to increase exponentially
* the factors investigated do not affect the borrowing rate significantly
* the factors investigated do not affect the proportion of loans invested in significantly