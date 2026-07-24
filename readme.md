# Multi-Radar Human Localization using Range and Angle Features

A machine learning pipeline for **2D human localization** using multiple mmWave radars. The project explores multi-radar sensor fusion, DBSCAN-based clustering, geometric triplet selection, and machine learning models to estimate human positions from radar measurements.

---

## Overview

The localization pipeline consists of the following stages:

```text
Raw Radar Data
      │
      ▼
Coordinate Transformation
      │
      ▼
Time Synchronization
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

## Project Structure

```
multi-radar-human-localization/
│
├── notebooks/
│   ├── 01_dbscan_visualization.ipynb
│   ├── 02_localization_pipeline.ipynb
│   └── 03_model_comparison.ipynb
│
├── docs/
│   ├── dbscan_visualization/
│   ├── localization_metrics/
│   ├── triplet_visualization/
│   ├── simulation_results/
│   ├── CSM_angle_GPR/
│   ├── CSM_range_GPR/
│   └── CSM_CSM_geometry_tuning/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Notebooks

### 01_dbscan_visualization.ipynb

Visualizes the preprocessing stages of the localization pipeline, including:

- Raw radar detections
- DBSCAN clustering
- Cluster centroids
- Candidate triplets
- Selected triplets

---

### 02_localization_pipeline.ipynb

Implements the complete localization framework.

Main components:

- Data preprocessing
- Coordinate transformation
- DBSCAN clustering
- Triplet selection using the Minimum Midpoint Distance heuristic
- Feature extraction
- Gradient Boosting Regression for localization
- Performance evaluation

---

### 03_model_comparison.ipynb

Compares different regression models using the same preprocessing pipeline.

Models evaluated include:

- Gradient Boosting Regressor
- Random Forest
- Ridge Regression
- Gaussian Process Regression
- Multi-Layer Perceptron (MLP)
- Quantile Gradient Boosting

---

## Features

- Multi-radar sensor fusion
- Time synchronization
- Coordinate transformation
- DBSCAN clustering
- Candidate triplet generation
- Geometric triplet selection (Min-DMid)
- Range-angle feature engineering
- Supervised machine learning for localization
- Model comparison and evaluation

---

## Results

The `docs/` directory contains representative outputs from the experiments, including:

- DBSCAN clustering visualizations
- Triplet selection visualizations
- Geometry tuning results
- Localization metrics
- Gaussian Process Regression results
- Simulation outputs

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

## Technologies

- Python
- NumPy
- Pandas
- Scikit-learn
- SciPy
- Matplotlib
- Jupyter Notebook

---

## Installation

Clone the repository

```bash
git clone https://github.com/Charithagadari/multi-radar-human-localization.git
```

Install the required packages

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook

```bash
jupyter notebook
```

---

## Future Work

- Real-time localization
- Multi-person tracking
- Deep learning-based localization
- Kalman Filter based trajectory estimation
- Sensor fusion with vision and LiDAR
- ROS integration

---

## Author

**Charitha Gadari**

M.Tech, Computer Science and Engineering

Indian Institute of Information Technology Design and Manufacturing (IIITDM) Kurnool

Research Interests:

- Machine Learning
- Computer Vision
- Autonomous Systems
- Sensor Fusion
- Radar Signal Processing
- Human Localization

---

## License

This project is released under the MIT License.