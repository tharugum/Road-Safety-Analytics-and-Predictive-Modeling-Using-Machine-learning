# Road Safety Analytics and Predictive Modeling Using Machine Learning

## Project Overview

Road traffic collisions are a major public safety concern, resulting in fatalities, serious injuries, property damage and significant social and economic consequences. This project applies data analytics and machine learning techniques to historical UK road-safety data to investigate factors associated with collision severity and develop predictive models for classifying collision outcomes.

The study uses road-safety open data published by the **UK Department for Transport (DfT)**, containing detailed information about collisions, vehicles and casualties.

The project follows an end-to-end data science workflow, including data integration, preprocessing, exploratory data analysis, statistical analysis, spatial analysis, feature engineering, machine learning, model optimisation, cost-sensitive learning and explainable AI.

---

## Objectives

The main objectives of this project are:

- Integrate relevant UK road-safety collision, vehicle and casualty datasets.
- Clean and preprocess the collected data for analysis and modelling.
- Perform exploratory, statistical and spatial analysis of road collisions.
- Identify important factors associated with collision severity.
- Engineer and select relevant features for predictive modelling.
- Develop and compare multiple machine-learning classification models.
- Optimise the selected XGBoost model.
- Investigate cost-sensitive learning to address class imbalance.
- Evaluate models using multiple classification metrics.
- Apply SHAP explainability to understand the factors influencing predictions.
- Identify the limitations and potential applications of machine learning in road-safety analysis.

---

## Dataset

The project uses the UK Department for Transport's Road Safety Open Data.

**Data Source:**  
https://www.gov.uk/government/statistical-data-sets/road-safety-open-data

The datasets contain information relating to:

- Road collisions
- Vehicles involved in collisions
- Casualties
- Road and environmental characteristics
- Temporal characteristics
- Geographical information
- Collision severity

The original datasets were integrated and processed before being used for machine-learning analysis.

### Dataset Processing

The integrated Collision + Vehicle dataset contained:

**920,692 records × 81 variables**

After preprocessing, feature engineering and feature selection, the final modelling dataset contained:

**48,431 collision records × 31 predictive features**

The target variable represents three collision-severity classes:

- Fatal
- Serious
- Slight

---

## Methodology

The project follows the workflow below:

```text
UK DfT Road Safety Data
          |
          v
Data Collection & Inspection
          |
          v
Data Integration
          |
          v
Data Cleaning & Preprocessing
          |
          v
Exploratory Data Analysis
          |
          v
Statistical & Spatial Analysis
          |
          v
Feature Engineering
          |
          v
Train/Test Preparation
          |
          v
Baseline Machine Learning Models
          |
          v
Model Comparison
          |
          v
XGBoost Hyperparameter Tuning
          |
          v
Cost-Sensitive Learning
          |
          v
Model Evaluation

```

Exploratory Data Analysis:

Exploratory analysis was performed to investigate patterns in collision severity across different characteristics, including:

Year
Month
Hour of occurrence
Speed limit
Road type
Junction characteristics
Urban/rural classification
Vehicle-related characteristics
Geographical distribution

Visualisation and statistical analysis were used to identify patterns and relationships before predictive modelling.

Machine Learning Models:

Multiple supervised classification algorithms were evaluated:

Logistic Regression
Decision Tree
Random Forest
Extra Trees
XGBoost

The models were compared using a consistent training and testing framework.

XGBoost was subsequently selected for further investigation through hyperparameter tuning and cost-sensitive modelling.

Class Imbalance:

Collision severity is highly imbalanced, with Slight collisions representing the majority of observations and Fatal collisions representing a much smaller proportion.

Because of this imbalance, accuracy alone was not considered sufficient for evaluating model performance.

The following metrics were used:

Accuracy
Balanced Accuracy
Precision
Recall
F1-score
Macro F1-score
ROC-AUC
Confusion Matrix
Precision-Recall analysis

Cost-sensitive learning was also investigated to increase the importance of severe collision outcomes during model training.

Model Explainability:

SHAP (SHapley Additive exPlanations) was used to interpret the final XGBoost model.

The SHAP analysis was used to:

Identify the most influential predictive features.
Understand the contribution of individual variables.
Examine how features influence model predictions.
Improve the interpretability of the machine-learning results.

This allows the project to move beyond simply evaluating predictive performance and investigate which factors influence collision-severity predictions.

Key Analytical Areas:

The project investigates several important road-safety dimensions:

Temporal Analysis:

Analysis of collision patterns across years, months and hours of the day.

Road and Environmental Analysis:

Investigation of factors such as speed limit, road type, junction characteristics and urban/rural classification.

Spatial Analysis:

Examination of the geographical distribution and concentration of recorded collisions.

Predictive Modelling:

Comparison and optimisation of machine-learning models for collision-severity classification.

Explainable AI:

Interpretation of model predictions using feature importance and SHAP analysis.


Technologies Used:
Programming Language - Python
Development Environment - Google Colab
Libraries - Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, SHAP

Project Outcomes:

The project provides an end-to-end framework for analysing UK road-collision data and predicting collision severity.

The analysis demonstrates that machine-learning models can identify useful patterns within historical road-safety data. However, predicting rare severe outcomes remains challenging because of the substantial class imbalance.

The project therefore evaluates model performance using class-sensitive metrics and supplements predictive modelling with SHAP-based interpretation.

Limitations:

The main limitations of the study include:

Significant imbalance between collision-severity classes.
Limited representation of Fatal collision outcomes.
Dependence on the variables available in the historical dataset.
Historical relationships may not fully represent future road conditions.
Machine-learning associations should not be interpreted as causal relationships.
The model is intended for analytical and decision-support purposes rather than automated safety decisions.


Future Work:

Future improvements could include:

Incorporating traffic-volume and road-exposure data.
Adding more detailed weather and infrastructure information.
Applying advanced spatial and temporal modelling.
Investigating additional imbalance-handling techniques.
Testing additional machine-learning and deep-learning approaches.
Performing time-based validation using future years.
Validating the model on independent datasets.
Developing a decision-support dashboard for road-safety analysis.
Continuously monitoring model performance after deployment.
          |
          v
SHAP Explainability
