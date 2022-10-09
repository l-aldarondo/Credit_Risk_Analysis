# Credit_Risk_Analysis
Using Supervise Machine Learning to Predict Credit Risk

## Background

### Overview of Analysis

TThis new assignment consists of three technical analysis deliverables and a written report. You will submit the following:

- Deliverable 1: Use Resampling Models to Predict Credit Risk

- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk

- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

- Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)


### Purpose

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Resources

Data source:

- (1) credit_risk_ensemble_starter_code, (2) credit_risk_resampling_starter_code, (3) LoanStats_2019Q1

Software:

- Google Colab, AWS RDS, pgAdmin 6.14, Visual Studio Code 1.71.2
 
<br/>

## Methodology

### D1: Use Resampling Models to Predict Credit Risk

Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

<br/>

We chose an [Amazon_reviews_dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) to be analyzed. All the datasets had the same schemata, as shown in this image below:

(a)![amazon_dataset_example](./Images/amazon_dataset_example.png)
 
<sub> Figure (a) Amazon Dataset Schema example

<br/>

### D2: Use the SMOTEENN algorithm to Predict Credit Risk

CUsing your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.


(b)![customer_id_table](./Images/customer_id_table.png)
 
<sub> Figure (b) The customers_table DataFrame

<br/>

### D3: Use Ensemble Classifiers to Predict Credit Risk

Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.


(c)![product_id_table](./Images/product_id_table.png)
 
<sub> Figure (c) The final products_table DataFrame

<br/>


## Results:
#### Refer to figure(f) above

- Q1. How many Vine reviews and non-Vine reviews were there?

    - A1. There were **170** Vine reviews and **37,840** non_Vine reviews.

- Q2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

    - A2. There were **65** 5 star Vine reviews and **20,612** 5 star non-Vine reviews.

- Q3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

    - A3. **38.24%** of the 5 star reviews were Vine and **54.47%** of 5 star reviews were non-Vine.


## Summary

Ho: 5star_vine = 5star_not_vine, there is no difference in the percenage(proportion) of 5star ratings paid(vine) vs unpaid(not vine).

Ha: 5star_vine <> 5star_not_vine, there is a difference in the percenage(proportion) of 5star ratings paid(vine) vs unpaid(not vine).

- percentage_5star_vine = **38.24%**
 
- percentage_5star_not_vine = **54.47%**
 
- **findings: the percentage of 5 star rating is not the same when comparing vine reviews to not_vine reviews**, figure (f).
 
- **There is reason to believe that the percentage of 5 star raitings is not directly tied to whether the review is paid or unpaid.**
 
- Additional analysis should be perform to evaluate the hypothesis test comparing the proportion of 5 star reviews among the two samples.


## References

[Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

[Spark](https://downloads.apache.org/spark/)
 
[Google Colab](https://colab.research.google.com/github/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/01.01-Help-And-Documentation.ipynb)

