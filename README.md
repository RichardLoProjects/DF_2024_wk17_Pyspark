# DF_2024_wk17_Pyspark
# Dataset Integration for Churn Prediction

### Motivation

What is *churn rate*? A simple google search yields: *The churn rate refers to the rate at which subscribers or customers stop transacting with your business. Simply put, they are subscribers who canceled their subscriptions or customers who did not return to your store. A higher churn rate means more customers are leaving your business.*

Customer churn does not appear to be a good thing for an organisation. Perhaps more care must be given to customers who are likely to churn over those who are not likely to churn. I believe it would be helpful for internal decision making within an organisation if that particular organisation knew which customers were likely to churn.

### Problem Statement

Given data on a customer, make an estimate on whether or not they are likely to churn. Thus the organisation can take additional measures for that customer.

### Project Aims

- Find multiple datasets on customer churn.
- Format, clean, validate, and integrate the datasets.
- Prepare the dataset for machine learning (i.e. feature engineering), ensuring the final dataset is split into a train-test split.
- Fit a variety of machine learning models (logistic regression, random forest, gradient boosted trees) on the training data to predict customer churn.
- Pickle the models.
- Load the pickles in Jupyter notebooks to showcase the models using the test data.

In summary: procure some data, process in pipelines, fit some models, pickle them, and evaluate the models.

### Project Outcomes

The project achieved (or did not achieve) the goals outlined in the project aims. More details are outlined here:

- The project yielded seven datasets on customer churn, which can be found in the assets folder or from the following links: [1](<https://www.kaggle.com/datasets/rangalamahesh/bank-churn>), [2](<https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn>), [3](<https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset>), [4](<https://www.kaggle.com/datasets/santoshd3/bank-customers>), [5](<https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction>), [6](<https://www.kaggle.com/datasets/shubhammeshram579/bank-customer-churn-prediction>), [7](<https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers>).
- Pyspark on Databricks was chosen to host the data and machine learning pipelines since big organisations will tend to be working with big data. Pyspark offers computation through clusters to manage big data.

### Product Description

The project produced several Python-pickle-objects containing trained machine learning models that predict customer churn based on the following features:

- feature 1...

### Conclusion



