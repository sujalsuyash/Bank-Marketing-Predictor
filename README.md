***BANK MARKETING SUBSCRIPTION PREDICTOR ->***



EXECUTIVE SUMMARY Engineered an end-to-end Machine Learning pipeline to predict bank term deposit subscriptions. Analyzed over 45,000 customer records and optimized a predictive model to identify high-value leads. Maximized sales efficiency by prioritizing high-probability customers, achieving an 80% Recall rate on a highly imbalanced dataset.



***BUSINESS PROBLEM ->***



Inefficiency: Mass cold-calling results in low conversion rates and high operational costs.

Data Imbalance: Only 11.7% of customers subscribe, causing standard models to fail in detecting potential buyers.

Objective: Develop a precision targeting system to identify "Yes" customers and reduce wasted calls.

TECHNICAL ARCHITECTURE \& METHODOLOGY

Data Preprocessing

Transformed categorical variables using One-Hot Encoding for model compatibility.

Stratified training data (70/30 split) to preserve class distribution integrity.

Mitigated class imbalance impacts using advanced weighting strategies.

Model Optimization

Implemented an XGBoost Classifier (Extreme Gradient Boosting) for superior tabular performance.

Executed an extensive RandomizedSearchCV (1,000 iterations, 5-Fold CV) to tune hyperparameters including learning rate, tree depth, and scale weights.

Calibrated the decision threshold to 0.58, mathematically balancing Precision and Recall to favor opportunity capture.



***KEY RESULTS ->***



The optimized XGBoost model achieved exceptional performance in identifying potential customers:

Recall: 80% (Successfully captured the vast majority of potential subscribers).

AUC Score: 0.93 (Demonstrated elite class separability and ranking ability).

Precision: 52% (Maintained actionable efficiency for the sales team).



***VISUAL EVIDENCE ->***



Confusion Matrix Identified 1,286 out of 1,598 total subscribers, minimizing missed revenue opportunities. (See images/confusion\_matrix.png)

ROC Curve Achieved an AUC of 0.93, demonstrating robust predictive power across all thresholds. (See images/roc\_curve.png)

Feature Importance Identified 'Past Success' and 'Call Duration' as primary conversion drivers. (See images/feature\_importance.png)



***TECH STACK ->***



Language: Python 3.9+

Modeling: XGBoost, Scikit-Learn

Analysis: Pandas, NumPy

Visualization: Matplotlib, Seaborn



***HOW TO RUN ->***



Install dependencies: pip install -r requirements.txt

Load the saved model for inference: import joblib model = joblib.load('xgboost\_bank\_model.pkl') prediction = model.predict(new\_data)

