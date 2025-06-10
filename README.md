# yelp-rating-predictor
A project that predicts Yelp ratings using linear regression

# Yelp Exploration & Rating Prediction 📍📊

This project, titled `yelp_exploration.ipynb`, explores Yelp's dataset to analyze what factors influence a restaurant's star rating, and builds a multiple linear regression model to predict that rating.

## 🔍 Overview

The notebook walks through:
- Loading and merging 6 real Yelp JSON datasets (businesses, reviews, users, photos, tips, check-ins)
- Cleaning the combined data by removing irrelevant columns and filling missing values
- Exploring correlations between features and Yelp star ratings
- Visualizing relationships between features and the target (`stars`)
- Training multiple regression models on different feature sets
- Evaluating model performance using R² score and prediction scatter plots
- Predicting the expected rating for a fictional new restaurant

## 🛠️ Tools & Libraries
- Python 3
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

## 💡 Key Decisions
- Dropped columns like `name`, `address`, `categories` that were text-heavy or not numerically useful
- Replaced missing values in numeric features (e.g. check-ins, tips) with `0`, assuming absence implies zero
- Explored several feature sets, from basic to full, to compare model performance
- Evaluated both training and test R² scores to check for overfitting
- Used a custom `model_these_features()` function to automate model comparison

## 🧪 Results
- The strongest predictor of Yelp rating was `average_review_sentiment`
- Simpler models underfit, while full-feature models improved R² but risked overfitting
- Final model predicted a hypothetical restaurant's rating with reasonable accuracy

## 📁 Files
- `yelp_exploration.ipynb`: Main Jupyter Notebook containing the full analysis and modeling workflow
