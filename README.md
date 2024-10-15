# Cancer Risk Prediction Project

## Overview
This project aims to predict the risk of lung cancer using a dataset containing various lifestyle and health-related factors. The goal is to build and evaluate different machine learning models to classify individuals based on their risk of developing lung cancer, thus providing valuable insights for early detection and prevention efforts.

## Dataset
The dataset includes 3,000 entries with the following 15 features:

- **GENDER**: Gender of the individual
- **AGE**: Age of the individual
- **SMOKING**: Whether the individual smokes
- **YELLOW_FINGERS**: Presence of yellow fingers (often due to smoking)
- **ANXIETY**: Reports of anxiety
- **PEER_PRESSURE**: Peer pressure impact
- **CHRONIC_DISEASE**: Presence of chronic disease(s)
- **FATIGUE**: Reports of fatigue
- **ALLERGY**: Presence of allergies
- **WHEEZING**: Reports of wheezing
- **ALCOHOL_CONSUMING**: Whether the individual consumes alcohol
- **COUGHING**: Reports of coughing
- **SHORTNESS_OF_BREATH**: Difficulty in breathing
- **SWALLOWING_DIFFICULTY**: Difficulty swallowing
- **CHEST_PAIN**: Reports of chest pain

The target variable is **LUNG_CANCER**, with binary values indicating risk status (1 for risk, 0 for no risk).

## Preprocessing
The preprocessing involved the following steps:
1. **Binary Conversion**: The target column `LUNG_CANCER` was converted from "Yes" and "No" values to binary (1 and 0, respectively).
2. **Train-Test Split**: The dataset was split into training and test sets with an 80-20 ratio.

## Models and Evaluation
Three machine learning models were applied to the dataset:

1. **Logistic Regression**
2. **Random Forest Classifier**
3. **XGBoost Classifier**

Each model was evaluated on the following metrics:
- **Accuracy**: Overall correctness of the model.
- **Precision**: Proportion of true positive predictions among all positive predictions.
- **Recall**: Proportion of true positive predictions among all actual positive cases.
- **F1 Score**: Harmonic mean of precision and recall, used to balance both metrics.

### Results
| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 0.52     | 0.52      | 0.57   | 0.54     |
| Random Forest        | 0.50     | 0.50      | 0.54   | 0.52     |
| XGBoost              | 0.49     | 0.49      | 0.53   | 0.51     |

The **Logistic Regression** model outperformed the others with an F1 Score of 0.54, indicating a more balanced performance between precision and recall. 

## Conclusion
The Logistic Regression model emerged as the best-performing model for predicting lung cancer risk. While the accuracy of all models was around 50%, Logistic Regression provided the highest F1 Score, suggesting it may offer a reasonable trade-off between identifying high-risk cases accurately and avoiding false positives.


