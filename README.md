# High Value Client Prediction

## Project Overview

This project demonstrates a simple machine learning classification workflow for predicting whether a client belongs to the high-value segment.

The model uses client characteristics, purchasing behavior, and support interaction data to classify clients as either high-value or not high-value.

This is an educational machine learning project focused on practicing the full ML pipeline: data preparation, train/test split, model training, model comparison, evaluation, cross-validation, confusion matrix analysis, and feature importance interpretation.

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
* matplotlib
* seaborn
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
7. Training a limited-depth Decision Tree Classifier
8. Comparing model evaluation metrics
9. Comparing train and test accuracy
10. Applying cross-validation
11. Analyzing the confusion matrix
12. Visualizing the confusion matrix with a heatmap
13. Analyzing feature importance
14. Visualizing feature importance
15. Writing final conclusions

## Models

Two decision tree models were trained in this project:

* Decision Tree Classifier
* Decision Tree Classifier with limited depth (`max_depth=2`)

The limited-depth model was added to compare the original decision tree with a simpler and more interpretable version.

## Evaluation Metrics

The models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score

On the small test set, both models achieved maximum metric values. However, this result should not be considered reliable evidence of high model quality because the dataset is very small.

## Train and Test Accuracy Comparison

Train and test accuracy were compared to evaluate whether the models might be overfitting.

Both models achieved the same train and test accuracy values on the current dataset. However, because the dataset contains only 20 clients, this comparison should be interpreted with caution.

## Cross-Validation

Cross-validation was applied to compare model performance across several data splits.

This provides a more stable estimate of model performance than a single train/test split. However, the dataset is still very small, so the cross-validation results should also be interpreted carefully.

## Confusion Matrix

The confusion matrix was used to analyze model errors in more detail.

The model made no false positive or false negative errors on the current test set. The confusion matrix was also visualized as a heatmap to make the result easier to interpret.

However, the test set contains only 6 clients, so this result should not be treated as proof of perfect model performance.

## Feature Importance

The feature importance analysis showed that the model mainly relied on `total_amount`.

This is logical from a business perspective because clients with a higher total purchase amount are more likely to belong to the high-value segment.

However, with a larger dataset, the importance of features could change, and other features such as `orders_count`, `avg_order_amount`, or `days_since_last_order` could become more important.

## Key Findings

* A simple classification model was successfully built.
* The target variable was `is_high_value`.
* Two decision tree models were trained and compared.
* Both models achieved maximum metric values on the small test set.
* Train/test accuracy comparison and cross-validation were used for additional model evaluation.
* The confusion matrix showed no errors on the current test set.
* The most important feature was `total_amount`.
* The results should be interpreted carefully because the dataset contains only 20 clients.

## Limitations

This project uses a small educational dataset. Because of this, the model evaluation results may be unstable and should not be treated as proof of real-world model performance.

The target variable is also strongly related to purchasing behavior, especially `total_amount`, which makes the classification task relatively simple in this educational example.

For a more reliable analysis, a larger real-world dataset would be required.

## Future Improvements

In the future, this project could be improved by:

* using a larger real-world dataset;
* comparing additional machine learning models;
* tuning model hyperparameters;
* applying more robust validation techniques;
* evaluating performance on a larger and more stable test set;
* adding more realistic client behavior features;
* testing the model on unseen real-world data.

## Repository Structure

```text
high-value-client-prediction/
│
├── high_value_client_prediction.ipynb
└── README.md
```

## Conclusion

This project demonstrates the basic steps of a machine learning classification task. It shows how to prepare data, train and compare models, evaluate model performance, apply cross-validation, analyze errors with a confusion matrix, and interpret feature importance.

Although the dataset is small, the project provides a clear example of an end-to-end machine learning workflow.
