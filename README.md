# -Medicine-Recommendation-System
This project is a Disease Prediction System that uses Machine Learning to identify potential illnesses based on a set of user-provided symptoms. In addition to the prediction, the system provides a comprehensive healthcare recommendation including disease descriptions, precautions, medications, and dietary advice.

🩺 Disease Prediction & Recommendation System
📊 Project Overview
This project leverages supervised learning to classify 41 different diseases based on 132 unique symptoms. The system achieved 100% accuracy on the test set using a Linear Support Vector Classifier (SVC).

Key Components:
Predictive Model: A trained SVC model that maps symptoms to a specific prognosis.

Recommendation Engine: A logic-based system that retrieves medical context (Description, Precautions, Medications, and Diets) from localized datasets after a disease is identified.

🛠️ Tech Stack
Language: Python 3.x

Libraries: * Scikit-learn: Model training, evaluation, and preprocessing.

Pandas: Data manipulation and analysis.

NumPy: Numerical operations and vectorization.

Pickle: Model serialization and persistence.

📂 Dataset Description
The system utilizes five key CSV files:

Training.csv: The primary dataset containing symptom rows (0 or 1) and the target prognosis column.

description.csv: Detailed definitions of each disease.

precautions_df.csv: Four levels of preventative measures for each condition.

medications.csv: Recommended medications for the identified disease.

diets.csv: Dietary suggestions to aid recovery.

🚀 Machine Learning Pipeline
Data Loading: Reading the symptom-disease mapping.

Preprocessing: * Label Encoding the target prognosis.

Splitting data into Training (70%) and Testing (30%).

Model Benchmarking: Evaluated multiple algorithms:

Support Vector Classifier (SVC) - Selected Model

Random Forest Classifier

Gradient Boosting Classifier

K-Nearest Neighbors (KNN)

Multinomial Naive Bayes

Serialization: The trained SVC model is saved as svc.pkl for fast deployment without retraining.

💻 How It Works
The system converts user input (textual symptoms) into a numerical feature vector of length 132.

Python
# Example Usage
symptoms = "itching, nodal_skin_eruptions, joint_pain"
predicted_disease = get_predicted_value(user_symptoms)
description, precautions, medications, diet = helper(predicted_disease)
📈 Results
The models were evaluated using Accuracy Scores and Confusion Matrices.

SVC Accuracy: 1.0 (100%)

Random Forest Accuracy: 1.0 (100%)

Naive Bayes Accuracy: 1.0 (100%)
