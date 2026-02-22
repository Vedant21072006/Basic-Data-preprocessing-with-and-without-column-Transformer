🧠 Data Preprocessing in Machine Learning (Manual vs ColumnTransformer)

This project demonstrates two different approaches to preprocessing tabular data using Python and Scikit-learn:

🔹 Manual preprocessing (step-by-step)

🔹 Automated preprocessing using ColumnTransformer

The goal of this project is to understand how feature preprocessing works internally and how it can be efficiently handled using Scikit-learn utilities.

📊 Dataset Features

The dataset contains the following columns:

age → Numerical

fever → Numerical (contains missing values)

cough → Categorical (Ordinal: Mild / Strong)

gender → Categorical (Nominal)

city → Categorical (Nominal)

📂 Project Structure
.
├── without_columntransformer.py
├── with_columntransformer.py
└── README.md
1️⃣ Manual Preprocessing Approach

In manual_preprocessing.py, each preprocessing step is applied separately:

Handling missing values using SimpleImputer

Encoding ordinal feature (cough) using OrdinalEncoder

Encoding nominal features (gender, city) using OneHotEncoder

Converting sparse matrices to dense format

Combining processed columns using numpy.concatenate

Debugging dimension mismatch and train/test alignment issues

✅ What This Demonstrates

Understanding how each transformation works

Handling sparse vs dense matrix issues

Fixing shape mismatch errors

Proper use of fit() and transform()

2️⃣ ColumnTransformer Approach

In column_transformer_preprocessing.py, preprocessing is handled using ColumnTransformer.

Applied transformations:

SimpleImputer → for missing values in fever

OrdinalEncoder → for ordinal feature cough

OneHotEncoder → for nominal features gender and city

remainder='passthrough' → keeps remaining columns unchanged

✅ Why This Is Better

Cleaner and more scalable

Reduces manual errors

Production-ready structure

Easily integrates with Pipeline
