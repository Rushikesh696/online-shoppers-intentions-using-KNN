# online-shoppers-intentions-using-KNN
## **Project Overview**
The goal of this project is to develop a machine learning model that can predict whether an online shopper will complete a purchase during a session based on their browsing behavior, traffic source, and session characteristics. Using the Online Shoppers Intention dataset, the model classifies user sessions as either resulting in a purchase or not, helping e-commerce businesses enhance marketing strategies, improve user experience, and optimize conversion rates. This is a binary classification problem, where the model classifies each session into two categories: purchase or no purchase.

## **Table of Contents**
Project Description

Data Preprocessing

Model Building

Model Evaluation

Usage

Conclusion

Dependencies

## **Project Description**
This project focuses on predicting the purchase intent of online shoppers by analyzing various features such as:

Browsing behavior: Time spent on pages, number of pages visited.

Traffic source: Where the traffic is coming from (e.g., search engine, direct).

Session characteristics: Whether the session occurred on a weekend, whether the user is a returning visitor, etc.

## **Objective**
The objective of this project is to create a predictive model using machine learning that can classify sessions into:

1 (Will Purchase)

0 (No Purchase)

By predicting these outcomes accurately, e-commerce businesses can enhance their marketing and optimize user experience to improve conversion rates.

## **Data Preprocessing**

Outlier Detection: Outliers in numerical features were identified and handled to avoid skewing the model’s predictions.

Feature Encoding: Categorical features, such as Month and VisitorType, were transformed into numerical values using encoding techniques like Label Encoding.

Feature Scaling: Standard scaling was applied to the numerical features to normalize the data and improve the performance of distance-based models like KNN.

SMOTE (Synthetic Minority Over-sampling Technique): To address class imbalance in the target variable Revenue, SMOTE was applied to generate synthetic samples for the minority class, improving the model’s ability to predict purchases.

## **Model Building**
Model Selection: We chose the K-Nearest Neighbors (KNN) algorithm for this classification problem, as it is a simple yet effective model for predicting outcomes based on feature similarity.

Training: The model was trained using the scaled training data, with the target variable being the Revenue (whether a purchase was made or not).

Hyperparameter Tuning: We selected n_neighbors=3 for the KNN algorithm, based on cross-validation and grid search to find the optimal value of k.

## **Model Evaluation**
After training the model, we evaluated its performance using several metrics:

Accuracy: The model achieved an accuracy of 80.09% on the initial dataset and 65.06% after applying SMOTE.

Precision: After balancing the dataset, the precision for the positive class (purchase) improved to 88.85%.

Confusion Matrix: The confusion matrix revealed the number of true positives, true negatives, false positives, and false negatives, indicating areas where the model could be improved.

F1-Score: The F1-score for the positive class was 0.89, showing a good balance between precision and recall.

## **Conclusion**
The KNN model is effective in predicting purchase intent based on browsing behavior, with a focus on improving precision for purchases. After addressing class imbalance with SMOTE, we observed significant improvements in the model’s ability to predict purchase sessions. The imbalance between the target classes (purchase vs. no purchase) remains a challenge, but by using resampling techniques like SMOTE, we were able to optimize the model’s predictive power for the minority class. The insights gained from this model can be used to guide business decisions around targeted marketing and session optimization.
