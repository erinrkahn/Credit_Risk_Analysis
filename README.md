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

- The RandomOverSampler will generate new samples by randomly selecting replacements from existing samples to account for under-representation. In this example the Balanced accuracy score was X while the f1 score was X. Using SMOTE (Syntheitc Minority Over-sampling Technique), random examples from the minority class are chosen then k of the nearest neighbors are found. Neighbors are then used to generate synthetic examples. In this analysis, the SMOTE method produced a Balanced accuracy score of X anf f1 of X. 

### **Undersampling Algorithm**

#### ClusterCentroids
Balanced Accuracy Score
>![UnderA](https://user-images.githubusercontent.com/77405273/119721594-2857b680-be20-11eb-8097-fcdd6074a61b.png)

Imbalanced Classification Report
>![UnderB](https://user-images.githubusercontent.com/77405273/119721596-2857b680-be20-11eb-8d15-a1cf8d5a2f2b.png)

- Description

### **Combination Over- and Undersampling Algorithm**

#### SMOTEENN
Balanced Accuracy Score
>![SMOTEENNA](https://user-images.githubusercontent.com/77405273/119721601-2b52a700-be20-11eb-9e59-b5104d2e90c1.png)

Imbalanced Classification Report
>![SMOTEENNB](https://user-images.githubusercontent.com/77405273/119721604-2b52a700-be20-11eb-8c33-69bf6fb187a0.png)

- Description

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

- Description

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.
