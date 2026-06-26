# 🎵 Spotify-Songs-Hit-Prediction

## Project Description

The **Spotify Hit Predictor** is an end-to-end Machine Learning project that explores whether a song is likely to become a **Hit** or **Non-Hit** by analyzing its musical characteristics and metadata. With millions of songs released every year, identifying the factors that contribute to commercial success has become an important challenge for artists, producers, record labels, and streaming platforms. This project leverages data science and machine learning techniques to uncover patterns within Spotify's music dataset and build predictive models capable of estimating a song's success before it gains widespread popularity.

Unlike traditional popularity prediction systems that rely heavily on streaming statistics or playlist appearances, this project focuses primarily on a song's inherent attributes, including audio features and metadata. By deliberately removing popularity-based variables during the classification task, the models learn relationships based on musical characteristics rather than existing popularity, resulting in a more realistic and unbiased prediction process.

The project demonstrates a complete machine learning pipeline, covering every stage from data exploration and preprocessing to model training, optimization, and evaluation. It serves as a practical implementation of data analytics, feature engineering through preprocessing, supervised learning, and model selection using real-world Spotify data.

# Objectives

The primary objectives of this project are to:

* Analyze the relationship between musical attributes and song popularity.
* Build a classification model capable of predicting whether a song will become a **Hit** or **Non-Hit**.
* Develop regression models to estimate the expected number of Spotify streams.
* Compare the performance of multiple machine learning algorithms.
* Improve model performance using hyperparameter optimization techniques.
* Evaluate models using standard classification and regression metrics.
* Demonstrate an end-to-end machine learning workflow using real-world music data.

# Dataset

This project utilizes the **Spotify 2023 Dataset**, which contains information about thousands of songs released on Spotify.

The dataset includes:

* Song metadata
* Artist information
* Release year
* Release month
* Musical key
* Mode
* Danceability
* Energy
* Acousticness
* Instrumentalness
* Speechiness
* Liveness
* Valence
* Tempo
* Loudness
* Duration
* Stream count
* Playlist appearances
* Chart rankings across multiple streaming platforms

These features provide valuable insights into both the musical composition and commercial performance of songs.

# Exploratory Data Analysis (EDA)

Before building predictive models, extensive exploratory data analysis was performed to understand the dataset and identify important patterns.

The analysis included:

* Dataset inspection
* Missing value analysis
* Duplicate detection
* Statistical summaries
* Distribution analysis of numerical features
* Univariate analysis
* Bivariate analysis
* Correlation analysis
* Correlation heatmaps
* Feature relationship visualization
* Outlier identification

These visualizations and statistical analyses helped identify the variables that have stronger relationships with song popularity while providing a deeper understanding of the dataset's structure.

# Data Preprocessing

A comprehensive preprocessing pipeline was implemented to improve data quality and prepare the dataset for machine learning algorithms.

The preprocessing steps included:

### Handling Missing Values

Missing values were identified and appropriately handled to ensure consistency throughout the dataset.

### Removing Duplicate Records

Duplicate songs were removed to prevent repeated observations from influencing model performance.

### Encoding Categorical Variables

Categorical variables such as:

* Musical Key
* Mode

were converted into numerical representations using **One-Hot Encoding**, allowing machine learning algorithms to process them effectively.

### Feature Scaling

Continuous numerical variables were standardized using **StandardScaler** to ensure that all features contribute equally during model training.

### Target Variable Creation

For the classification task, songs were categorized as **Hit** or **Non-Hit** by applying the **75th percentile of stream counts** as the decision threshold. Songs with stream counts above this threshold were labeled as Hits, while the remaining songs were labeled as Non-Hits.

# Preventing Data Leakage

One of the key aspects of this project was ensuring that the machine learning models learned genuine musical patterns rather than relying on information that directly reflects a song's existing popularity.

To achieve this, popularity-dependent features such as:

* Spotify Playlist Count
* Spotify Chart Rankings
* Apple Playlist Count
* Apple Chart Rankings
* Deezer Playlist Count
* Deezer Chart Rankings
* Shazam Chart Count
* Stream Count (for classification)

were removed before training the classification models.

Removing these variables prevents **data leakage**, allowing the models to make predictions using only song characteristics and metadata that would realistically be available before a song becomes popular.

# Machine Learning Models

To identify the most effective predictive approach, multiple machine learning algorithms were implemented and compared.

## Classification Models

Several supervised learning algorithms were trained to classify songs into **Hit** and **Non-Hit** categories.

The models include:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* K-Nearest Neighbors (KNN)
* Naive Bayes
* AdaBoost Classifier
* Gradient Boosting Classifier
* XGBoost Classifier

Each model was trained and evaluated to compare predictive performance, generalization capability, and robustness.

## Regression Models

In addition to classification, regression models were developed to predict the approximate stream count of a song.

The regression algorithms include:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor

These models estimate continuous stream values rather than assigning categorical labels.

# Hyperparameter Optimization

Model performance was further improved through systematic hyperparameter tuning.

Two optimization techniques were employed:

## GridSearchCV

GridSearchCV performs an exhaustive search across predefined parameter combinations to identify the optimal configuration for each model.

Parameters such as:

* Number of estimators
* Maximum tree depth
* Minimum samples split
* Minimum samples leaf
* Maximum features

were optimized to achieve improved predictive performance.

## RandomizedSearchCV

RandomizedSearchCV was used to efficiently explore larger hyperparameter spaces by randomly sampling parameter combinations.

Compared with exhaustive search, this approach significantly reduces computational cost while still identifying high-performing model configurations.

These optimization techniques helped improve model accuracy, enhance generalization capability, and identify the best-performing models for the dataset.

# Model Evaluation

The trained models were evaluated using multiple industry-standard performance metrics.

### Classification Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* ROC Curve
* Area Under ROC Curve (AUC)
* Confusion Matrix

These metrics provide a comprehensive evaluation of classification performance beyond simple accuracy.

### Regression Metrics

Regression models were evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

These metrics measure prediction accuracy and the ability of the models to explain variations in stream counts.

# Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Seaborn
* Jupyter Notebook

# Key Features

* Complete end-to-end Machine Learning pipeline
* Comprehensive Exploratory Data Analysis (EDA)
* Data cleaning and preprocessing
* One-Hot Encoding for categorical features
* Feature scaling using StandardScaler
* Prevention of data leakage through feature selection
* Hit/Non-Hit classification
* Stream count prediction using regression
* Comparison of multiple machine learning algorithms
* Hyperparameter optimization using GridSearchCV and RandomizedSearchCV
* Performance evaluation using classification and regression metrics
* Visualization of feature relationships and model insights

# Conclusion

The **Spotify Hit Predictor** demonstrates how machine learning can be applied to analyze musical characteristics and predict song success using real-world streaming data. By combining exploratory data analysis, robust preprocessing, multiple supervised learning algorithms, hyperparameter optimization, and comprehensive evaluation techniques, the project provides valuable insights into the factors that influence a song's popularity. It highlights the importance of preventing data leakage, comparing multiple models, and using appropriate evaluation metrics to build reliable predictive systems. Overall, this project serves as a practical example of an end-to-end machine learning workflow and showcases the application of data science techniques to solve real-world problems in the music industry.
