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
- Evaluate models using the test data.

In summary: procure data, construct pipelines, fit models, and evaluate models.

### Project Outcomes

The project achieved the goals outlined in the project aims. More details are outlined here:

- Kaggle yielded seven datasets on customer churn, which can be found in the assets folder or from the following links: [1](<https://www.kaggle.com/datasets/rangalamahesh/bank-churn>), [2](<https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn>), [3](<https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset>), [4](<https://www.kaggle.com/datasets/santoshd3/bank-customers>), [5](<https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction>), [6](<https://www.kaggle.com/datasets/shubhammeshram579/bank-customer-churn-prediction>), and [7](<https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers>).
- Pyspark on Databricks was chosen to host the Jupyter notebooks since big organisations will tend to be working with big data. Pyspark offers computation through clusters to manage big data.
- A data pipeline was constructed to merge multiple datasets together into one cohesive dataframe to be fed into the machine learning pipeline. A main machine learning pipeline was constructed, which branched out into four variants: `logistic_regression`, `decision_tree`, `gradient_boosted_trees`, and `random_forest`. An additional comment is that PySpark's ML library was extremely friendly to the user because the ML objects had very similar methods which allowed classifiers to be easily swapped out with each other: only a single line of code needed to be changed to fit an entirely different model.

### Product Description

The project produced five Jupyter notebooks in the `/databricks` folder:

- `Explanatory Data Analysis.ipynb`: An initial investigation which uncovered that most of the data is similar.
- `Data Pipeline Model.ipynb`: A test to ensure that the data pipeline is working as intended.
- `Data Pipeline.ipynb`: The data pipeline which merges the datasets into one dataframe.
- `Datapipeline EDA of Output.ipynb`: An investigation of the result.
- `ML_Pipelines.ipynb`: Fitting various ml models, and using the "best" model to predict customer churn.

### Conclusion

It was discovered that `gradient_boosted_trees` seemed to solve customer churn better than the other models. Using accuracy as the metric, here's how the models performed:

- logistic regression: `78.16%`
- decision trees: `82.07%`
- gradient boosted trees: `82.13%`
- random forest: `80.64%`

More metrics are reported in the `ML_Piplines` notebook such as: recall, precision, and AUC.

