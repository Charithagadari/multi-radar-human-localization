# Multi-Radar Human Localization using Range and Angle Features

A machine learning-based pipeline for **2D human localization** using multiple mmWave radars. The project combines **multi-radar sensor fusion**, **DBSCAN clustering**, **geometric triplet selection**, and **supervised machine learning** to estimate human positions from radar measurements.

---

## Project Overview

This project investigates localization using **range and angle measurements** collected from multiple radars. The proposed pipeline:

- Synchronizes detections from multiple radars
- Clusters radar detections using DBSCAN
- Generates candidate radar triplets
- Selects the most consistent triplet using a geometric heuristic (Minimum Midpoint Distance)
- Extracts localization features
- Trains machine learning models to predict the human's 2D position

The project also compares multiple regression models for localization performance.

---

## Pipeline

```
Raw Radar Data
        │
        ▼
Coordinate Transformation
        │
        ▼
Time Synchronization & Binning
        │
        ▼
DBSCAN Clustering
        │
        ▼
Cluster Centroid Extraction
        │
        ▼
Candidate Triplet Generation
        │
        ▼
Minimum Midpoint Distance (Min-DMid) Selection
        │
        ▼
Feature Extraction
(Range, Angle, SNR, Intensity, Noise)
        │
        ▼
Machine Learning Regression
        │
        ▼
Predicted Human Position (x, y)
```

---

## Features

- Multi-radar sensor fusion
- Coordinate transformation to a common reference frame
- Time synchronization of radar detections
- DBSCAN-based spatial clustering
- Candidate triplet generation
- Geometric triplet selection using the **Minimum Midpoint Distance (Min-DMid)** heuristic
- Range and angle feature engineering
- Machine learning-based localization
- Performance evaluation using RMSE, MAE, and R²

---

## Machine Learning Models

The project compares several regression models for localization:

- Gradient Boosting Regressor (GBR)
- Multi-Layer Perceptron (MLP)
- Random Forest Regressor
- Ridge Regression
- Polynomial Ridge Regression
- Gaussian Process Regression
- Quantile Gradient Boosting

---

## Repository Structure

```
range-angle-human-localization/
│
├── notebooks/
│   ├── 01_dbscan_visualization.ipynb
│   ├── 02_localization_pipeline.ipynb
│   └── 03_model_comparison.ipynb
│
├── results/
│   ├── dbscan_visualizations/
│   ├── triplet_visualizations/
│   ├── localization_metrics/
│   └── simulation_results/
├── README.md
```

---

## Notebook Description

### 01_dbscan_visualization.ipynb

Visualizes each stage of preprocessing:

- Raw radar detections
- DBSCAN clustering
- Cluster centroids
- Candidate triplets
- Selected triplets

---

### 02_localization_pipeline.ipynb

Implements the complete localization pipeline:

- Data preprocessing
- Feature extraction
- Gradient Boosting localization model
- Hyperparameter optimization
- Model evaluation
- Prediction visualization

---

### 03_model_comparison.ipynb

Compares multiple machine learning models and evaluates their localization performance using identical preprocessing and feature sets.

---

## Evaluation Metrics

Localization performance is evaluated using:

- Root Mean Square Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score
- Euclidean Localization Error
- Prediction Scatter Plots
- Error Histograms

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- SciPy
- Matplotlib
- Jupyter Notebook

---

## Example Outputs

The repository contains example outputs including:

- DBSCAN clustering visualizations
- Candidate triplet plots
- Selected triplet visualizations
- Prediction vs Ground Truth scatter plots
- Localization error histograms
- Model performance metrics



## Author

**Charitha Gadari**

M.Tech Computer Science and Engineering  
Indian Institute of Information Technology Design and Manufacturing (IIITDM) Kurnool
# multi-radar-human-localization
# multi-radar-human-localization
