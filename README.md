# Can we predict who is likely to buy?

## The idea

When businesses run ads online, they want to reach the people most 
likely to buy — not waste budget showing ads to people who won't. 
The challenge is: how do you know in advance who those people are?

I explored that question using a real dataset of social network users. 
The goal was simple: given basic information about a user (their age 
and salary), can I predict whether they will purchase a product?

## The data

I downloaded a publicly available dataset from Kaggle called 
Social Network Ads. It contains 400 users with three pieces of 
information: age, estimated salary, and whether they made a purchase.
Small dataset, but a clear and realistic problem.

## Why machine learning?

I could have just looked at the data and made a judgement call  
for example "older users with higher salaries tend to buy more." 
And that intuition would actually be partially right.

But machine learning lets me go further. Instead of relying on 
a single rule, ML finds the combination of signals that best 
predicts the outcome — automatically, at scale, without having 
to guess the right thresholds manually.

This matters in advertising because there are millions of users 
and milliseconds to decide whether to show them an ad. 

## What I did

Following the data science life cycle:

1. Defined the problem — predict which users will convert
2. Acquired and cleaned the data from Kaggle
3. Explored the data to understand patterns and audience behaviour
4. Built two models and compared them:
   - Logistic Regression as a simple baseline
   - XGBoost as a more powerful alternative

## What I found

XGBoost outperformed the baseline model. Age turned out to be the 
strongest predictor of whether someone would purchase — more so 
than salary alone. This suggests that demographic signals like age 
should be weighted heavily when deciding who to target.

## What I learned

- EDA (Exploratory Data Analysis) matters more than I expected — understanding the data before 
  modelling led to better decisions throughout
- Keep it simple. Always start with a simple baseline model before trying something 
  more complex, otherwise you have nothing to compare against. 
- Data can challenge your assumptions — I expected salary to be the 
  strongest predictor but age turned out to matter more
- Writing comments that explain the "why" not just the "what" forces 
  you to make sure you actually understand every step

## Tech used

Python, pandas, scikit-learn, XGBoost, matplotlib, seaborn
