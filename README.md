# HeartDiseasePredictionUsingANN
Heart Disease Prediction Using Artificial Neural Networks (ANN)
Objective:
The goal of this project is to predict whether a patient will experience a heart-related event (indicated by the DEATH_EVENT column) based on clinical records.

Dataset Overview:
Source: The dataset consists of 299 samples and 13 features, including:
Patient demographics: age, sex.
Clinical indicators: anaemia, diabetes, high_blood_pressure, etc.
Lab test results: serum_creatinine, serum_sodium, platelets.
Outcome: DEATH_EVENT (target variable with binary classification: 0 = no event, 1 = event).
The dataset is balanced, as shown by a count plot for the target variable.
Preprocessing Steps:
Feature Scaling: StandardScaler was applied to standardize the features to a mean of 0 and standard deviation of 1.
Data Splitting:
75% of the data was used for training and 25% for testing.
Validation data (20% of training data) was used for early stopping.
Feature Matrix (X): All features excluding DEATH_EVENT.
Target Variable (y): DEATH_EVENT.
Model Architecture:
The Artificial Neural Network (ANN) was implemented using Keras with the following layers:

Input Layer: 12 input features.
Hidden Layers:
1st Layer: 16 neurons, ReLU activation.
2nd Layer: 8 neurons, ReLU activation.
Dropout: 25% to prevent overfitting.
3rd Layer: 4 neurons, ReLU activation.
Dropout: 50% to further prevent overfitting.
Output Layer: 1 neuron with a sigmoid activation function (for binary classification).
Training the Model:
Loss Function: Binary Crossentropy (suitable for binary classification).
Optimizer: Adam (efficient gradient-based optimizer).
Callbacks: Early stopping was employed to halt training if no improvement in validation accuracy was observed for 30 epochs.
Training Details: 500 epochs with a batch size of 32.
Performance Metrics:
Validation Accuracy: Achieved a mean validation accuracy of 66.67%.
Confusion Matrix: Provides insight into the true positives, true negatives, false positives, and false negatives.
A normalized heatmap of the confusion matrix was plotted to visually assess performance.
Results:
The ANN achieved modest predictive performance.
The confusion matrix highlights potential areas for improvement in correctly identifying the DEATH_EVENT cases.
Visualization:
A diverging palette heatmap was used to display the normalized confusion matrix, aiding in performance analysis.
Potential Improvements:
Feature Engineering:
Include derived features or interactions between existing ones.
Analyze the importance of individual features.
Hyperparameter Tuning:
Optimize the number of neurons, layers, dropout rates, and learning rates.
Model Complexity:
Experiment with more advanced architectures (e.g., deeper networks or recurrent layers like LSTM for temporal data).
Class Imbalance:
If imbalance exists, consider oversampling techniques like SMOTE.
This model provides a foundation for predicting heart disease events using ANN but leaves room for further optimization and exploration of alternative techniques.
