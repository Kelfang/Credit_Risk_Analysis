# Credit Risk Analysis

## Project Overview

The motivation behind this project is to utilize machine learning and statistical reasoning to solve a real-world challenge: credit card risk. 

Using the credit card dataset from LendingClub, a peer-to-peer lending services company, I deployed the use of multiple algorithms and models to determine which, if any, should be used to predict credit risk. 

## Resources
* Python 
* Imbalanced-learn library
* Scikit-learn library
* Numpy library
* Pandas library
* Jupyter Notebook
* Data Sources: .csv and .ipynb files

## Results

Overall, this process included six machine learning models and, in the details below, I will outline the balanced accuracy scores, the precision scores and recall scores of each. After the csv file was cleaned, 68,817 loans remained. Below are the counts of the loan status. 

<sub> Loan Status Origin Count</sub>

 ![loan_status_origin_count](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/loan_status_origin_count.png)

------------------------------------------------------

### 1. Random Oversampling

![ros_counter](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/random_oversampling/ros_counter.png)

* **Balanced Accuracy Score - 63.8%**

<sub>Random Oversampling Balanced Accuracy Score</sub>

![ros_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/random_oversampling/ros_balanced_accur_score.png)


* **Precision and Recall Scores**
  - The "high risk" precision is only 1%, with the recall sitting at 66%.
  - The "low risk" precision is significantly different at 100%, while the recall is lower at 61%. 

![ros_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/random_oversampling/ros_confusion_matrix.png)

![ros_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/random_oversampling/ros_classification_report_imb.png)

------------------------------------------------------

### 2. SMOTE Oversampling

![smote_counter](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smote_oversampling/smote_counter.png)

* **Balanced Accuracy Score - 65.9%**
  - This is slightly immproved over the Random Oversampling.

<sub>SMOTE Balanced Accuracy Score</sub>

![smote_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smote_oversampling/smote_balanced_accur_score.png)

* **Precision and Recall Scores**
  - Similar to the Random Oversampling, the "high risk" precision is only 1%, with the recall sitting lower at 62%.
  - Just like above, the "low risk" precision is also at 100%, while the recall is at 69%.

![smote_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smote_oversampling/smote_confusion_matrix.png)

<sub>SMOTE Imbalanced Classification Report</sub>

![smote_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smote_oversampling/smote_classification_report_imb.png)

------------------------------------------------------

### 3. Undersampling – ClusterCentroids

![cc_under_counter](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/undersampling_clustercentroids/cc_under_counter.png)

* **Balanced Accuracy Score - 54.4%**
  - This is lowest of all the models presented.

<sub>Undersampling Balanced Accuracy Score</sub>

![cc_under_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/undersampling_clustercentroids/cc_under_balanced_accur_score.png)


* **Precision and Recall Scores**
  - As we saw with both models previously, the "high risk" precision is at 1%, with the recall sitting at 69%.
  - The "low risk" precision hits 100%, with the recall sitting at 40% (the lowest of all the models).

![cc_under_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/undersampling_clustercentroids/cc_under_confusion_matrix.png)


<sub>Undersampling Imbalanced Classification Report</sub>

![cc_under_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/undersampling_clustercentroids/cc_under_classification_report_imb.png)

------------------------------------------------------

### 4. SMOTEENN Combination Sampling

![smoteenn_combo_counter](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smoteenn_combo_sampling/smoteenn_combo_counter.png)


* **Balanced Accuracy Score - 66.7%**

<sub>SMOTEENN Balanced Accuracy Score</sub>

![smoteenn_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smoteenn_combo_sampling/smoteenn_balanced_accur_score.png)


* **Precision and Recall Scores**
  - Fallin in line with all the previous models, the "high risk" precision is at 1%, with the second highest recall at 79%. 
  - The "low risk" precision is 100%, with the recall at 54%.

![smoteenn_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smoteenn_combo_sampling/smoteenn_confusion_matrix.png)

<sub>SMOTEENN Imbalanced Classification Report</sub>

![smoteenn_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/smoteenn_combo_sampling/smoteenn_classification_report_imb.png)

------------------------------------------------------

### 5. Balanced Random Forest Classifier

* **Balanced Accuracy Score - 78.9%**
  - This is the second highest score of all models presented.

<sub>Balanced Random Forest Classifier Balanced Accuracy Score</sub>

![brf_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/balanced_random_forest/brf_balanced_accur_score.png)


* **Precision and Recall Scores**
  - The "high risk" precision sits at 3%, with the recall at 70%. It's worth noting that the F1 score is at 6%, higher than the previous models. 
  - The "low risk" precision is 100%, with the recall at 87%, the second highest of all the models. 

![brf_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/balanced_random_forest/brf_confusion_matrix.png)

<sub>Balanced Random Forest Imbalanced Classification Report</sub>

![brf_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/balanced_random_forest/brf_classification_report_imb.png)

------------------------------------------------------

### 6. Easy Ensemble AdaBoost Classifier

* **Balanced Accuracy Score - 93.2%**
  - This is the highest score of all models presented.

<sub>Easy Ensemble Classifier Balanced Accuracy Score</sub>

![ee_balanced_accur_score](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost/ee_balanced_accur_score.png)

* **Precision and Recall Scores**
  - The "high risk" precision is at 9%, with the recall at 92%. The F1 is the highest of all models at 16%.
  - The "low risk" precision is 100%, with the recall at 94%.

![ee_confusion_matrix](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost/ee_confusion_matrix.png)


<sub>Easy Ensemble Imbalanced Classification Report</sub>

![ee_classification_report_imb](https://github.com/Kelfang/Credit_Risk_Analysis/blob/main/images/easy_ensemble_adaboost/ee_classification_report_imb.png)



## Summary 



