# Spotify-Songs-Hit-Prediction
Project Title: Spotify Hit Predictor

Overview: In today's competitive music industry, streaming platforms like Spotify play a crucial role in defining what makes a song a "hit." This project utilizes machine learning and music analytics to forecast whether a track will become a hit based on its innate audio features (such as acousticness, danceability, energy, and tempo) and musical properties. The goal is to provide data-driven insights that help artists, producers, and record labels understand the sonic patterns underlying popular music.

Tech Stack: Python, Pandas, Scikit-Learn, XGBoost, Seaborn, Matplotlib.

*Methodology & Workflow:*

Exploratory Data Analysis (EDA): Conducted comprehensive analysis on the "Spotify 2023" dataset, including univariate/bivariate analysis and correlation heatmaps to uncover relationships between track attributes and success.

Data Preprocessing: Cleaned the dataset by handling missing values and duplicates. Categorical variables (key, mode) were transformed using One-Hot Encoding, and predictive numerical features were normalized using StandardScaler.

Preventing Data Leakage: A critical focus was placed on model integrity; direct proxy variables for popularity (such as playlist inclusions and chart rankings) were explicitly removed to ensure the model predicts based on musical quality rather than existing popularity.

Predictive Modeling:

Classification: Categorized songs as 'Hits' or 'Non-Hits' using models including Random Forest, XGBoost, and Logistic Regression.

Regression: Predicted exact stream counts using Random Forest and Decision Tree Regressors.

Hyperparameter Tuning & Evaluation: Optimized configurations using GridSearchCV and RandomizedSearchCV. Performance was rigorously evaluated using F1-Scores, AUC-ROC curves, and RMSE.
