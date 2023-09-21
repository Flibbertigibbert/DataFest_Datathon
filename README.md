# DataFest_Datathon
DataFest 2023 Datathon Data Science for Data Powerhouse

DataFest_datathon-EDA Notebook

DataFest Modeling - Preprocessing and Model Training


Fraud Detection for Online Payment Platform

Overview

The Fraud Detection dataset serves as a cornerstone asset for our enterprise, endowing us with invaluable insights and opportunities for fortifying the security and trustworthiness of our online payment platform. This dataset encapsulates a comprehensive repository of transactions and user-related data, meticulously collected over an extended period from our platform. Our paramount objective revolves around the development of a sophisticated predictive model, one with the capacity to discern potentially fraudulent transactions.

Context

The online payment platform is a juggernaut, processing a staggering volume of transactions each day. This volume leaves us exposed to an array of fraudulent activities, each constituting a significant menace to both our enterprise and our cherished customers. To shield the platform from these threats and to enrich the user experience, we are resolute in harnessing the prowess of data science and machine learning to proactively identify and thwart fraudulent transactions.
Objectives
 Develop a state-of-the-art machine learning model capable of predicting whether a given transaction bears the hallmarks of potential fraudulence or stands as a legitimate transaction. 

# Data Exploratory Insights
In this dataset, consisting of 6,000,000 rows and 32 columns, a thorough examination revealed the following key insights:

1. Class Balance: The distribution of the 'Fraudulent Flag,' our target variable, demonstrates a well-balanced dataset. Both fraudulent and non-fraudulent transactions are approximately evenly represented.`
2. Feature Distribution: Upon meticulous analysis, we observed a balanced distribution across all dataset features. Notably, the feature values for fraudulent transactions closely resemble those for non-fraudulent transactions.

3. Categorical Features: A noteworthy observation centers around the prevalence of high cardinality among categorical features. This observation underscores the importance of prudent feature engineering and meticulous handling to extract meaningful insights from these complex categorical attributes.
   
# Feature Engineering

To address the challenges identified during the exploratory phase, a systematic approach was employed.
With a focus on feature generation. Numerical features with a significant impact on fraud were identified using K-best and ANOVA scores. Notably, user transaction history, User ID, and user income emerged as influential factors. New features, such as Transaction Amount to Income Ratio, Transaction Frequency, Days of the Week, Hour of the Day, Time Taken for Transaction_UserAvg, Transaction Time Deviation, Transaction Amount_UserAvg, and Transaction Amount Deviation, were derived to capture key insights.

Additionally, certain features that should have had a high impact on unusual transactions exhibited low impact, likely due to high value count. To address this, features like "Merchant's Reputation Score," "User Age," and "Merchant's Business Age" were reclassified into meaningful categories. 

Categorical features with high cardinality underwent a careful regrouping process to improve model manageability and utility, given the challenges posed by the balanced data. The decision was made to retain these features for comprehensive analysis, with feature importance guiding subsequent refinement efforts.


# Data Splitting and Preparation for Model Training

The model development phase began with thorough data preparation,After that i employed data scaling using the Standard Scaler. Principal Component Analysis (PCA), a dimensionality reduction technique, was then applied to further streamline training times and enhance model performance.

To maintain data integrity, the `train_test_split` method was employed with a random seed (`random_state`) of 5 to shuffle the dataset. Considering the dataset's size, efforts were made to expedite training and improve model efficiency.

# Model Training and Results
The training phase involved three prominent models: Logistic Regression, LGBModel, and a neural network. 

Regrettably, the results yielded an accuracy, precision, and recall of 0.50, suggesting that the models performed no better than random guessing. 

The ROC curve's area under the curve (AUC) also confirmed this lackluster performance, further emphasizing the necessity for significant model refinement to align with the project's overarching objectives.


## Model Result

### Logistic Regression
Accuracy : 0.500095

Recall: 0.6108139501893393

Precision: 0.4995243509130142

F1-score: 0.5495918526705268

### LGB Model
Accuracy: 0.49935833333333335

Precision: 0.4988150504334322

Recall: 0.5553640003404602

F1-score: 0.5255728078363365




