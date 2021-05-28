# Credit Risk Analysis

## Overview of the Analysis 

### Purpose

This analysis utilizes imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Multiple sampling methods are used to predict and compare credit risk among credit card applicants. RandomOverSampler and SMOTE are used to oversample the data, ClusterCentroids to undersample, SMOTEENN as a combination approach of over- and undersampling, and BalancedRandomForestClassifier and EasyEnsembleClassfier machine learning models are used to reduce bias. All models are evaluated for performance and a final recommendation.  

## Results

### **Oversampling Algorithms**

#### RandomOverSampler
Balanced Accuracy Score
>![RandomOverSamplerA](https://user-images.githubusercontent.com/77405273/119721584-268df300-be20-11eb-953b-0dffb2282d4d.png)

Imbalanced Classification Report
>![RandomOverSamplerB](https://user-images.githubusercontent.com/77405273/119721590-27268980-be20-11eb-937d-7ae048e3c36b.png)

#### SMOTE
Balanced Accuracy Score
>![SMOTEA](https://user-images.githubusercontent.com/77405273/119721591-27bf2000-be20-11eb-95db-baa3f4aff765.png)

Imbalanced Classification Report
>![SMOTEB](https://user-images.githubusercontent.com/77405273/119721593-27bf2000-be20-11eb-9111-0e731e7f882f.png)

- The RandomOverSampler will generate new samples by randomly selecting replacements from existing samples to account for under-representation. In this example the Balanced accuracy score was 0.65 while the f1 score was 0.81. Using SMOTE (Synthetic Minority Over-sampling Technique), random examples from the minority class are chosen then k of the nearest neighbors are found. Neighbors are then used to generate synthetic examples. In this analysis, the SMOTE method produced a Balanced accuracy score of 0.62 and f1 of 0.77.

### **Undersampling Algorithm**

#### ClusterCentroids
Balanced Accuracy Score
>![UnderA](https://user-images.githubusercontent.com/77405273/119721594-2857b680-be20-11eb-8097-fcdd6074a61b.png)

Imbalanced Classification Report
>![UnderB](https://user-images.githubusercontent.com/77405273/119721596-2857b680-be20-11eb-8d15-a1cf8d5a2f2b.png)

- The ClusterCentroids method of undersampling where the majority class is under sampled by replacing a cluster of majority samples using the KMeans algorithm. In this analysis, the ClusterCentroids method produced a Balanced Accuracy score of 0.51 and an f1 of 0.60, which underperforms compared to the Oversampling techniques with this particular dataset. 

### **Combination Over- and Undersampling Algorithm**

#### SMOTEENN
Balanced Accuracy Score
>![SMOTEENNA](https://user-images.githubusercontent.com/77405273/119721601-2b52a700-be20-11eb-9e59-b5104d2e90c1.png)

Imbalanced Classification Report
>![SMOTEENNB](https://user-images.githubusercontent.com/77405273/119721604-2b52a700-be20-11eb-8c33-69bf6fb187a0.png)

- SMOTEENN combines over- and undersampling using SMOTE paired with Edited Nearest Neighbors. In this analysis, SMOTEENN produced a Balanced Accuracy Score of 0.62 and a f1 of 0.70, performing similarly to the Oversampling methods, but will a signifacntly lower recall score. 

### **Ensemble Classifiers**

#### BalancedRandomForestClassifier
Balanced Accuracy Score
>![BalancedRandomForestClassifierA](https://user-images.githubusercontent.com/77405273/119721605-2beb3d80-be20-11eb-8a87-2df8cbf664f9.png)

Imbalanced Classification Report
>![BalancedRandomForestClassifierB](https://user-images.githubusercontent.com/77405273/119721608-2c83d400-be20-11eb-8427-bdc9c6e4826a.png)

#### EasyEnsembleClassifier
Balanced Accuracy Score
>![EasyEnsembleA](https://user-images.githubusercontent.com/77405273/119721610-2c83d400-be20-11eb-9cfc-110227dae52a.png)

Imbalanced Classification Report
>![EasyEnsembleB](https://user-images.githubusercontent.com/77405273/119721611-2c83d400-be20-11eb-908b-dab39c89f401.png)

- BalancedRandomForestClassifier randomly under-samples each bootstrap sample to balance it, while EasyEnsembleClassifier also achieves balance through random undersampling, but by utilizing AdaBoost learners. In this analysis, BalancedRandomForestClassifier had a Balanced Accuracy Score of 0.79 and a f1 of 0.95, while EasyEnsembleClassifier had a Balanced Accuracy score of 0.93 and a f1 of 0.97.

## Summary

After completing the analysis using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling, multiple sampling methods were used to predict and compare credit risk among credit card applicants. The over-, under- and combination sampling methods all demonstrated high precision with a lower recall, so we would not recommend this for the purposes of predicting credit risk in card applicants. The ensemble methods performed well and the EasyEnsembleClassifier would be recommended for its precision, recall and f1 score, although overfitting needs to be taken into consideration with both Ensemble methods. 

