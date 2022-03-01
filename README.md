# Neural Network Charity Analysis

## Overview of the Analysis
Machine learning and neural networks were used to predict whether an applicant will be successful if funded.  Pandas and Scikit-Learn's standard scaler was used to preprocess the dataset.  TensorFlow was used to design a neural network and create a binary classification model.  Two additional optimizations on the model were attempted to try to hit the target predictive accuracy rate of 75%.

## Results

### Data Preprocessing

- The target variable was IS_SUCCESSFUL
- The features were: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- The EIN and NAME variables were neither target nor features so were removed from the input data

![EIN_NAME](https://user-images.githubusercontent.com/90982811/156249872-06eea9a3-ffba-4cdc-ad3a-8f4d44fdcd7b.jpg)


![split_preprocessed](https://user-images.githubusercontent.com/90982811/156249898-879afc16-761b-4b9f-89d3-4ad27ec36867.jpg)

### Compiling, Training, and Evaluating the Model

- 80 and 30 neurons were used within two hidden layers
- The target model performance of 75% was not achieved
- To try to increase the model's performance additional features were removed, STATUS and SPECIAL_CONSIDERATIONS.  A second attempt of optimization included adjusting the bin size.

![hidden_nodes](https://user-images.githubusercontent.com/90982811/156250203-8f48c2fd-074b-4510-8c22-95a7d42b6279.jpg)


![accuracy](https://user-images.githubusercontent.com/90982811/156249924-d0bf7e53-52d2-45db-80cb-bfb38ffb56ae.jpg)

## Summary

The initial accuracy rate was 69.34%, the first attempt of optimization returned 63.99% accuracy, and the final attempt returned 69.05% accuracy.  None of the attempts achieved the 75% target accuracy rate.  It is recommended to use the random forest classifier since it is effective in making predictions on large tabular datasets with less code and faster performance.
