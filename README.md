# Predicting-Visitor-Purchases-with-a-Classification-Model-with-BigQuery-ML
BigQuery ML (BigQuery machine learning) is a feature in BigQuery where data analysts can create, train, evaluate, and predict with machine learning models with minimal coding.

In this lab, we learn to perform the following tasks:

1.Use BigQuery to find public datasets

2.Query and explore the ecommerce dataset

3.Create a training and evaluation dataset to be used for batch prediction

4.Create a classification (logistic regression) model in BQML

5.Evaluate the performance of your machine learning model

6.Predict and rank the probability that a visitor will make a purchase

#Task 1. Explore ecommerce data
Scenario: Your data analyst team exported the Google Analytics logs for an ecommerce website into BigQuery and created a new table of all the raw ecommerce visitor session data for you to explore. Using this data, you'll try to answer a few questions.

Question: Out of the total visitors who visited our website, what % made a purchase?

1.Click the Query editor.

2.Add the following to the New Query field:

#standardSQL
WITH visitors AS(
SELECT
COUNT(DISTINCT fullVisitorId) AS total_visitors
FROM `data-to-insights.ecommerce.web_analytics`
),
purchasers AS(
SELECT
COUNT(DISTINCT fullVisitorId) AS total_purchasers
FROM `data-to-insights.ecommerce.web_analytics`
WHERE totals.transactions IS NOT NULL
)
SELECT
  total_visitors,
  total_purchasers,
  total_purchasers / total_visitors AS conversion_rate
FROM visitors, purchasers
