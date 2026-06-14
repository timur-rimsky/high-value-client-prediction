# High Value Client Prediction

## Project Overview

This project demonstrates a simple machine learning classification workflow for predicting whether a client belongs to the high-value segment.

The model uses client characteristics, purchasing behavior, and support interaction data to classify clients as either high-value or not high-value.

This is an educational machine learning project focused on practicing the full ML pipeline: data preparation, train/test split, model training, evaluation, and feature importance analysis.

## Project Goal

The goal of this project is to build a simple machine learning model that predicts whether a client belongs to the high-value segment based on client characteristics and purchasing behavior.

## Dataset Description

The dataset contains information about clients, their purchasing behavior, and support interactions.

### Features

* `client_id` — unique client identifier
* `age` — client age
* `town` — client town
* `orders_count` — number of orders made by the client
* `total_amount` — total purchase amount
* `avg_order_amount` — average order amount
* `days_since_last_order` — number of days since the last order
* `complaints_count` — number of complaints from the client
* `support_messages_count` — number of support messages

### Target Variable

* `is_high_value` — target variable: 1 if the client is high value, 0 otherwise

## Tools and Libraries

* Python
* pandas
* scikit-learn
* Jupyter Notebook

## Machine Learning Workflow

The project includes the following steps:

1. Creating a client dataset
2. Initial data review
3. Preparing features and target variable
4. Encoding categorical variables with one-hot encoding
5. Splitting the data into training and test sets
6. Training a Decision Tree Classifier
7. Making predictions on the test set
8. Evaluating the model using classification metrics
9. Analyzing feature importance
10. Writing final conclusions

## Model

The first machine learning model used in this project is:

* Decision Tree Classifier

This model was chosen because it is easy to interpret and useful for understanding how different features influence classification decisions.

## Evaluation Metrics

The model was evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score

On the small test set, the model achieved maximum values for all evaluation metrics. However, this result should not be considered reliable evidence of high model quality because the dataset is very small.

## Feature Importance

The feature importance analysis showed that the model mainly relied on `total_amount`.

This is logical from a business perspective because clients with a higher total purchase amount are more likely to belong to the high-value segment.

However, with a larger dataset, the importance of features could change, and other features such as `orders_count`, `avg_order_amount`, or `days_since_last_order` could become more important.

## Key Findings

* A simple classification model was successfully built.
* The target variable was `is_high_value`.
* The Decision Tree Classifier predicted all test values correctly on the small test set.
* The most important feature was `total_amount`.
* The results should be interpreted carefully because the dataset contains only 20 clients.

## Limitations

This project uses a small educational dataset. Because of this, the model evaluation results may be unstable and should not be treated as proof of real-world model performance.

For a more reliable analysis, a larger real-world dataset would be required.

## Future Improvements

In the future, this project could be improved by:

* using a larger real-world dataset;
* comparing several machine learning models;
* tuning model hyperparameters;
* evaluating performance on a larger and more stable test set;
* adding cross-validation;
* analyzing model performance with a confusion matrix.

## Repository Structure

```text
high-value-client-prediction/
│
├── high_value_client_prediction.ipynb
└── README.md
```

## Conclusion

This project demonstrates the basic steps of a machine learning classification task. It shows how to prepare data, train a model, evaluate its performance, and interpret feature importance.

Although the dataset is small, the project provides a clear example of an end-to-end machine learning workflow.
