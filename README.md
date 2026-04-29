Diabetic Foot Ulcer (DFU) Risk Prediction System
===============================================

Overview:
This project presents an AI-driven diabetic foot ulcer (DFU) risk prediction system that combines a supervised neural network model with an interactive chatbot interface to estimate the likelihood of a patient developing a diabetic foot ulcer. The goal of the project is to provide an accessible clinical decision-support prototype that transforms structured patient information into an individualized ulcer-risk assessment.

The model was trained using the Diabetes 130-US Hospitals dataset, containing over 100,000 patient records. Relevant features such as age, hospital visits, glucose results, A1C levels, medication usage, and diagnosis history were cleaned, encoded, and used to train a feedforward neural network for binary classification. The model outputs both a probability score and a predicted ulcer-risk class.

To improve usability, a chatbot intake tool was developed to guide users through a structured questionnaire, validate responses, preprocess inputs, and generate model-ready features in real time. This creates a full end-to-end workflow where user inputs are transformed into a DFU risk prediction in a simple conversational format.

The project demonstrates practical applications of deep learning, healthcare data preprocessing, feature engineering, and conversational AI to build an intelligent healthcare support system for early diabetic foot ulcer risk awareness.

Project Files:
--------------
1. DeepLearning_ProjectTeam2_DataProcessing.ipynb
   - Cleans and preprocesses the hospital dataset
   - Performs feature engineering
   - Exports the processed dataset as a CSV file

2. NeuralNetwork_model.ipynb
   - Trains the neural network model
   - Generates:
       * scaler.pkl
       * dfu_model.pkl
       * feature_order.pkl

3. ChatBot.ipynb
   - Launches the chatbot interface
   - Collects user inputs
   - Applies preprocessing
   - Produces a DFU risk prediction

How to Run:
-----------
1. Run `DeepLearning_ProjectTeam2_DataProcessing.ipynb`
   This prepares and exports the cleaned dataset. This step only needs to be completed once.

2. Run `NeuralNetwork_model.ipynb`
   This trains the neural network and saves the required model artifacts (`scaler.pkl`, `dfu_model.pkl`, and `feature_order.pkl`). This step only needs to be completed once.

3. Run `ChatBot.ipynb`
   This launches the chatbot intake tool. The chatbot will prompt the user for clinical information and return a predicted DFU risk score.

Technologies Used:
------------------
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Pickle

Future Improvements:
--------------------
- Improve model performance with class imbalance handling techniques such as SMOTE or class weighting
- Expand chatbot guidance with low/medium/high risk explanations
- Integrate with electronic health record (EHR) systems
- Deploy as a web-based application for real-time clinical use

License:
--------
This project was developed for academic purposes as part of an AI/Deep Learning course project.
