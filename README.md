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

![image](https://user-images.githubusercontent.com/60198979/139580755-47884b9f-a603-4295-97b8-d1c6e9005c8b.png)

3.Click Run.
The result: 2.69%

Question: What are the top 5 selling products?

4.Add the following query in the Query editor, and then click Run:

![image](https://user-images.githubusercontent.com/60198979/139581257-3cfb8613-8f47-4775-8151-6755afddaa1c.png)

![image](https://user-images.githubusercontent.com/60198979/139581291-a8c23cfa-5401-4390-a863-74c5756f0d17.png)


