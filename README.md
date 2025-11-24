Groundwater Storage Prediction Using Satellite Data

This project uses satellite datasets (GRACE and GLDAS) to estimate and predict groundwater storage changes. The main idea is to combine gravity-based water measurements with land surface model data and train a simple Artificial Neural Network (ANN) to predict groundwater anomalies.

This work is based on my M.Tech research paper.

Project Summary

GRACE data provides total water storage anomalies.

GLDAS data provides soil moisture and other land surface variables.

After aligning both datasets, groundwater anomaly is calculated.

An ANN model is trained using these combined features.

The model learns the relationship between satellite inputs and groundwater variations.

What the Project Does

Loads GRACE and GLDAS satellite data (NetCDF format)

Preprocesses and aligns both datasets

Computes groundwater storage anomaly

Normalizes the inputs

Trains a small ANN with two hidden layers

Evaluates the model using R², RMSE, and MAE

Model Details

Input: GRACE LWE anomaly + GLDAS soil moisture

Architecture:

Dense(64, ReLU)

Dense(32, ReLU)

Dense(1, Linear)

Optimizer: Adam

Loss: MSE

Achieved R² around 0.90 on validation data

Why This Project Is Useful

Groundwater levels are difficult to measure directly because ground sensors are expensive and sparse. Using satellite signals makes it possible to estimate groundwater changes at a regional scale. This can help in water management and drought monitoring.

Tools and Libraries

Python

NumPy, Pandas

xarray (for NetCDF data)

TensorFlow / Keras

Matplotlib

scikit-learn

File Included

groundwater_ann.ipynb – contains dataset loading, preprocessing, ANN model, and evaluation steps.

Dataset Information

GRACE: Provides Total Water Storage anomalies

GLDAS: Provides soil moisture and related parameters
(both datasets were downloaded separately and used for academic work)

Author

Dhruv Kukadiya
M.Tech – AI & Data Science
VIT Bhopal University
