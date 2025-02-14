# Predictors of Loan Pricing
This is the second of a series of three projects completed for my Applied Econometrics course of UCLA's Master of Quantitative Economics. The objective is to identify the best predictor of personal loan prices. To achieve this, we test multiple MLR models inclusive of variables transformations and interaction variables.

## Introduction
In this project, our team aims to construct a predictive model that examines the determinants of loan pricing in approved loan applications. The primary objective is identifying and evaluating the factors influencing the loan-to-price ratio, focusing on understanding demographic, financial, and loan-specific characteristics. By developing a robust model, we hope to uncover patterns that can inform more equitable and efficient lending practices.

## Research Questions
1. What are the most significant predictors of loan amount as a percentage of the price among quantitative and categorical variables?
2. How do demographic factors such as marital status and education level affect loan amount as a percentage of the price?
3. What role do financial indicators, including income and creditworthiness, play in determining loan amount as a percentage of the price?

## Project Objective and Data Source
We utilize the **Loan Application Dataset** sourced from the Wooldridge data package for this analysis. This dataset includes 1,989 observations on 59 variables, encompassing demographic details, financial indicators, loan-specific attributes, and approval outcomes. The data originates from a well-documented study on mortgage lending decisions by researchers at the Boston Federal Reserve Bank (Munnell et al., 1996).

Our dependent variable, `loanprc` (loan amount as a percentage of the property price), reflects the loan's proportional value relative to the asset's cost. The independent variables were carefully selected through statistical methods and domain knowledge to ensure their relevance and impact. The dataset is particularly suited to our analysis due to its breadth and focus on approved loans, allowing us to isolate pricing factors without confounding rejection-related criteria.

We aim to create a predictive model that addresses patterns in mortgage lending and gain a broader understanding of financial equity.

## Results
The most significant quantitative predictors of loan-to-price ratio are applicant income, appraised value, net worth, and other obligations as a percentage of income. Captured as the log of income (`appinc_log`), applicant income has a strong positive impact on the loan-to-price ratio squared, indicating that higher-income borrowers can secure larger loans relative to the property price. However, the appraised value (`apr_log`) shows a strong negative effect, reflecting that properties with higher appraised values tend to have smaller loan-to-price ratios, likely because wealthier borrowers make larger down payments. Net worth (`log_netw`) also has a significant negative impact, as borrowers with greater financial reserves rely less on loans. Lastly, other obligations (`obrat`) positively affect loan-to-price ratios for fixed-rate loans. Still, they are moderated by adjustable-rate loan types, indicating that obligations are more scrutinized in fixed-rate lending. Among categorical variables, the loan type (`fixadj`) is particularly important as it interacts significantly with other predictors, such as obligations and net worth, to influence loan pricing dynamics.

We initially expected factor variables related to marital status and education to be statistically significant in affecting loan prices, but after controlling for other financial indicators—namely, those included in our final model—they did not appear to be statistically significant in affecting loan pricing.

Financial indicators are central in determining loan terms, with income being the most critical factor. Higher-income is strongly associated with higher loan-to-price ratios, as it signals a borrower’s ability to handle larger loan payments. Creditworthiness is reflected indirectly through variables such as net worth and obligations. Borrowers with higher net worth generally secure smaller loan-to-price ratios, indicating greater financial independence, while those with higher obligations face scrutiny, particularly for fixed-rate loans.
