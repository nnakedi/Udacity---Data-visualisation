# Prosper Loan Data


## Introduction
> This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others
>
> Prosper Marketplace is America's first peer-to-peer lending marketplace, with over USD7 billion in funded loans. Borrowers request personal loans on Prosper and investors (individual or institutional) can fund anywhere from USD2,000 to USD40,000 per loan request. Investors can consider borrowers’ credit scores, ratings, and histories and the category of the loan. Prosper handles the servicing of the loan and collects and distributes borrower payments and interest back to the loan investors.
>
> Prosper verifies borrowers' identities and select personal data before funding loans and manages all stages of loan servicing. Prosper's unsecured personal loans are fully amortized over a period of three or five years, with no pre-payment penalties. Prosper generates revenue by collecting a one-time fee on funded loans from borrowers and assessing an annual loan servicing fee to investors.
>
> <i>Source: [Wikipedia](https://en.wikipedia.org/wiki/Prosper_Marketplace) </i>





# Main question: What are the key variable(s) that drive finance cost (BorrowersAPR)?
- The analysis below will attempt to answer this question using different univariate, bivariate and multivariate visualisations

## Summary of Observations

During the investigation, we attempted to understand what the biggest driver of finance cost (Borrower's APR). This was done through the analysis of univariate, bivariate and mulitvariate analysis. For some observations, a random sample of 5000 items was used. This sample is representative of the population, therefore it should not have a noticeable impact on the observations.

My investigation focused on the credit risk which is represented by two key variables in the dataset, namely the BorrowersAPR and the ProsperRating (numeric). This two variables had the highest correlation in the bivariate heatmap. For further insights, other variables were explored and the results are summarised below:

- The distribution of the loans according to ProsperRatings appeared to be normally distributed with 4 being the average score. The graph was slightly screwed to the left where the ProsperRating is lower. Fewer Borrowers have a high rating
- The average Original loan amount was USD 8,337 with most of the loans ranging from USD1,000 t0 USD10,000. In further observations when the loan amount was paired with the BorrowerAPR had a weak negative correlation of 0.3.
- Looking at employment status, full-time and part-time employees appear to have the lowest BorrowerAPR average, hovering below 0.2%. Surprisingly, where data is unavailable, the borrower APR is at 0.2% with the maximum just above 0.3%. Full-time employees have the widest range with minimums and maximums on the extreme ends of the spectrum
- The correlation between MonthlyStatedIncome and BorrowerAPR is weak, there are some observable insights. The higher the monthly income, the narrower the range of the BorrowerAPR. The BorrowerAPR is much more favourable to higher Monthly Income earners, despite the weak correlation
- Focusing on the employment statuses,  36 months appears to be the most popular term. Good-standing loan statuses (Completed, current) are dominant amongst employed and full-time employees.
- Long-term loans (60 months) are more frequent from the mean point of 4.0 on the ProsperRating, indicating that people with poor ratings opt for longer terms
- Looking at the mulitivariate analysis between PropserRating, BorrowerAPR and Loan amount, it was interesting to see that a long-term of 60 months attracts the lowest average BorrowerAPR until the mean ProsperRating of 4. After the mean ProsperRating of 4, 60-months attracts the highest average BorrowerAPR, followed by 36 months, then finally 12 months. The term of the loan appears to have an impact on BorrowerAPR after from the Mean ProsperRating of 4. However, across the board, the term of 60 months have the largest interquartile ranges as compared to the other two terms.
- Lastly, BorrowerAPR appear to average slightly above 0.2% regardless of the term, meaning that the term of the loan has little influence on the BorrowerAPR. However, the term of the loan has a higher impact on the term. Yields for the lenders are higher at 36 months, making it the sweetest spot for the lenders, which could explain why a significant portion of the loans have a term of 36 months. Lenders/investors are more likely to fund loans with the highest return for them. 12-month loans are 1% of the population, and this could be caused by the fact that these loans have the lowest yield for the lender
In conclusion, ProsperRating is the biggest driver of the finance cost (Borrower's APR).

<b>Key insights for presentation</b>
- The keysights will stem from the analysis of credit risk driven by the BorrowersAPR and their credit risk rating defined as the ProsperRating.
- Secondly, we will look at relationship of the Loan amount, ProsperRating and BorrowersAPR because the relationship of these variables is not linear and does change at a certain point
- Finally, we will look at the investor/lenders return, to try an understand the distribution of the terms of the loan based on the lenders yield
