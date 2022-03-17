# Prosper Loan data analysis

In this exploratory data analysis, I analysed **Prosper Loan data**. The dataset contains 113,937 loans with 81 variables on each loan, including basic information of the loan, i.e. date and amount, as well as information of the borrower, i.e. income and Prosper scores.

# Key question
The aim of this analysis is to investigate which and how variables influences borrower APR.

# Outline
Among all 81 variables, we selected several variables according to their definition. The exploratory analysis contains 3 steps:
1. summarise basic information of the loan.
2. investigate how non-borrower related variables influence borrower APR.
3. investigate how borrower related variables influence borrower APR.

## 1. Basic information of the loan.

I first explored some variables of the loan: term, status and APR.
I made count plot for term and loan status and histogram for borrower APR.
I found that the majority (77%) of the loans are of 2-year term, and half of the loan are currently running.
The key variable, borrower APR, doesn't follow normal distribution.

## 2. How non-borrower related variables influence borrower APR

The non-borrower related variables I selected are:
**a. Term**
I made boxplot to show the APR of different terms. I found that loans of 60-month term are of relative lower APR. Then I checked the distribution of APR for different terms.

**b. Loan original amount**
I first made scatter plot for loan original amount and APR, and found that they are negatively correlated.
The loan original amount might be also correlated with terms. To confirm this hypotheses, I made scatter plot of  loan original amount  vs. APR for different terms.

**c. State**
I made box plot for State and APR to explore whether average APR is the same along different states.

**d. Loan original quarter**
I made point plot to explore how APR changes with time, and whether APR is influenced by quarter.


## 3. How borrower related variables influence borrower APR
The borrower related variables that I selected are:
**a. Prosper rating and Prosper score**
I first investigated how Prosper rating and Prosper score are correlated. Then I checked how each of them correlated with borrower APR using box plot.

**b. Employment and Homeowning status**
I first checked how Employment and Homeowning status correlated with borrower APR respectively using box plot. I then investigated how those two variables influences APR together. Finally, I made bar plot for Prosper scores by those two variables to test whether they are correlated with Prosper score.

**c. Current delinquencies**
Initially I made histogram to show the distribution of current delinquencies. I then made scatter plot for current delinquencies and borrower APR to check their relationship.

**d. Income range**
I first made count plot to show the distribution of income of the borrowers. Then I used barplot to show how APR changes with income range.

**e. Total Prosper Loans**
I made barplot to show how total Prosper loans correlates with APR.


## Key insights

About half of the loans in the dataset are currently running. and 33.4% are completed. 10.5% are changed off, 4.4% are defaulted, and the rest 2% are past due.

77% Loans in the dataset are of 36 months term, 1.4% are of 12 months term, and 21,5% are of 60 months term. We also found that the distribution of borrower APR for different terms are different. Specifically, loans of 60 months term tend to of of lower APR.

We also notice that the loan original amount is negatively correlated with borrower APR. and the load original amount is lower for loan with 12 months term.

Borrower APR is different in different states. The top 3 states show highest average APR are AL, AR and SD. and the bottom 3 states with lowest APR are IA, ME and DC.

We found that APR also strongly correlated with borrower's Prosper rating and scores. Those two variables are strongly positive correlated and each of them is negatively correlated with borrower APR. Borrowers with high Prosper rating/score tend to have low APR.

And the Prosper score is strongly correlated with borrower's status, such as employment and home owning conditions. Unemployed borrowers are rated with lower score than employed borrowers. For homeowner condition, except for not employed borrowers that have higher score for non-homeowner, borrowers owning home are rated with higher score.

The majority of the borrowers have less than 2 current delinquencies. Borrowers with high current delinquencies have higher APR than those with low current delinquencies.

Income range is also an important varible that it strongly negative correlated with borrower APR. However, it is interesting to note that borrowers with 0 dollar income have lower APR than borrower with income range between 1 and 49,999.

I found the more Prosper loans the borrowers have, the lower APR they will have.

To sum up, we found borrower APR are correlated with multiple borrower, as well as non-borrower, related variables.


## Limitation

This is an exploratory analysis which went through several selected variables and investigated how they influences borrower APR. However, systematic statistical analysis is still need for an solid conclusion.

I also notice during the analysis that multiple variables are correlated with each other, such as Prosper rating are correlated with employment status. The correlation among variables may lead to complications if we want to build models to predict borrower APR.
