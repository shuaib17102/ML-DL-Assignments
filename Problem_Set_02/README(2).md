Project Title: Bank Term Deposit Subscription Prediction using Logistic Regression
 
Objective:

The objective of this project is to develop a machine learning model that predicts whether a customer will subscribe to a term deposit based on their banking and demographic information. This is formulated as a binary classification problem.
 
Dataset:
•	Dataset Name: Bank Marketing Dataset
•	Total Records: 45,211
•	Features: 17 attributes including age, job, balance, loan status, and contact details
•	Target Variable: Subscription status (yes/no)
•	Data Source: Provided dataset for the assignment(https://drive.google.com/file/d/18KwSR9aVTZRNaOVF76VE9USSEkqnYzzQ/view?usp=sharing)
 
Approach and Methodology:
1.	Data Exploration:

•	The dataset was loaded and examined using pandas
•	Basic structure and statistics were analyzed
•	Class distribution showed imbalance, with more “no” responses than “yes”
 
2.	Data Preprocessing:

•	The target variable was converted into binary format (yes = 1, no = 0)
•	Categorical features were transformed using one-hot encoding
•	Redundant columns were avoided using drop_first=True
 
3.	Data Splitting:

•	The dataset was split into training (80%) and testing (20%) sets
•	Stratified sampling was used to preserve class distribution in both sets
•	This ensures fair evaluation and avoids biased learning
 
4.	Feature Scaling:

•	StandardScaler was applied to normalize feature values
•	This improves model performance and convergence speed
 
5.	Model Building:

•	Logistic Regression was selected for this task because:
o	It is suitable for binary classification
o	It is efficient for structured/tabular data
o	It provides interpretable results
•	The model was trained with increased iterations to ensure proper convergence
 
6.	Model Evaluation:

The model was evaluated using multiple performance metrics:
•	Accuracy Score to measure overall performance
•	Confusion Matrix to analyze correct and incorrect predictions
•	Classification Report including Precision, Recall, and F1-score
•	ROC Curve and AUC Score to evaluate performance across thresholds
 
7.	Feature Analysis:

•	Model coefficients were analyzed to understand feature importance
•	This provides insight into which variables influence customer decisions
 
Results and Findings:
•	The model achieved approximately 90.12% accuracy on the test dataset
•	The model performs well in predicting the majority class (non-subscribers)
•	Lower recall for the minority class indicates the effect of class imbalance
•	AUC score above 0.90 indicates strong discriminative performance
 
Conclusion:

This project demonstrates that Logistic Regression is an effective baseline model for predicting customer subscription behavior. While overall accuracy is high, performance on minority class predictions can be improved with advanced techniques.
 
How to Run:
1.	Open the notebook in Google Colab
2.	Download the dataset using the provided link
3.	Run all cells sequentially
4.	Observe outputs including evaluation metrics and graphs
 
Additional Notes:
•	Stratified splitting was used to maintain class balance
•	ROC-AUC provides a more reliable evaluation than accuracy alone
•	Feature importance analysis improves model interpretability
 
Future Improvements:
•	Apply class balancing techniques such as SMOTE or class weights
•	Experiment with advanced models like Random Forest or XGBoost
•	Perform hyperparameter tuning for further optimization

