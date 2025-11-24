# Groundwater Storage Prediction Using Satellite Data

This project predicts groundwater storage anomalies using satellite datasets from **GRACE** and **GLDAS**.  
The goal is to estimate groundwater changes by combining gravity-based total water storage data with land surface variables, and training an Artificial Neural Network (ANN) for prediction.

This work is part of my M.Tech research at VIT Bhopal.

---

##  Project Summary

- **GRACE** provides Total Water Storage (TWS) anomalies  
- **GLDAS** provides soil moisture and surface variables  
- Groundwater anomaly is computed by combining both datasets  
- Preprocessing includes:
  - resampling
  - cleaning
  - normalization  
- ANN model is trained to learn the relationship between satellite signals and groundwater variation  
- Achieved **R² ≈ 0.90** on validation set  

---

## Data Sources

- **GRACE (Gravity Recovery and Climate Experiment)**
  - Provides mass change measurements (TWS anomaly)
- **GLDAS (Global Land Data Assimilation System)**
  - Provides soil moisture and land surface variables

---

##  Model Architecture (ANN)

```text
Input Layer: GRACE + GLDAS features
Dense (64, ReLU)
Dense (32, ReLU)
Dense (1, Linear)
Loss: MSE
Optimizer: Adam
```

---

## 📂 Files in This Repository

| File Name                               | Description |
|-----------------------------------------|-------------|
| `groundwater_ann.ipynb`                 | Notebook containing preprocessing, ANN training, and evaluation |
| `Groundwater_ML_Research_Dhruv.pdf`     | Research paper describing methodology and results |
| `README.md`                             | Project documentation |

---

## Tools & Libraries Used

- Python  
- NumPy  
- Pandas  
- xarray  
- scikit-learn  
- TensorFlow / Keras  
- Matplotlib  

---

## Results

- ANN model learned seasonal groundwater variation patterns
- Achieved high correlation (**R² ~ 0.90**)  
- Shows potential for satellite-based groundwater monitoring

---

##  Author

**Dhruv Kukadiya**  
M.Tech – AI & Data Science  
VIT Bhopal University  
