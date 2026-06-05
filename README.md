#Smart Budget Shopping Recommender
An ML-powered product recommender that finds the best Amazon products within your budget — combining value scoring, price prediction, and budget optimization.

# Project Overview
Given a list of items and a total budget, this system recommends the best products by analyzing 6,69,926 Amazon products across 113 categories using three ML techniques.
Example:
Input  → Items: ['laptop', 'headphones', 'mouse'] | Budget: ₹60,000
Output → Top 3 best-value picks for each item within budget

#DataSet
Source: Amazon Products Dataset by Lokesh Parab — Kaggle
Size: 6,69,926 products across 113 categories
Price range: ₹8 — ₹12,49,990
Average rating: 3.81/5
Categories include: Electronics, Headphones, Shoes, Books, Fashion, Kitchen, Sports, and more

# How It Works
1. Value Score
Rates every product on a 0–100 scale:
value_score=(rating×log(no_of_ratings+1))/log(price + 1)
Higher score=better value for money.
2. Price Prediction (Random Forest)
Predicts the fair market price of a product based on category, sub-category, ratings, discount percentage, and number of reviews. If a product's actual price is much lower than the predicted price, it's flagged as a great deal.
3. Budget Optimizer
Divides budget equally across items
Searches the dataset for matching products
Ranks by combined value+deal score
Returns top 3 picks per item with savings summary

#Tech Stack
Python                Core language
Pandas & NumPy        Data processing
Scikit-learn          Random Forest, Label Encoding, MAE, R²
Matplotlib & Seaborn  Visualizations
Kaggle                Dataset + notebook hosting

# Results
Successfully recommends best-value products across 113 categories
Price prediction R² = 0.766 (Random Forest)
Price MAE = ₹1,233
Budget optimizer works for any combination of items and budget
