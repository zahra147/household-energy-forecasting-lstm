# Household Energy Forecasting with LSTM

## Overview

This project focuses on short-term household electricity consumption forecasting using a Multi-Step LSTM neural network.

The model is trained on the UCI Individual Household Electric Power Consumption dataset and predicts future electricity consumption at multiple forecasting horizons.

## Forecast Horizons

The model predicts electricity consumption:

- 30 minutes ahead
- 40 minutes ahead
- 50 minutes ahead
- 60 minutes ahead

## Methodology

The project includes the following steps:

1. Dataset loading
2. Data cleaning
3. Missing value handling
4. Timestamp creation
5. Resampling to 10-minute intervals
6. Cyclical time feature engineering
7. Log transformation of the target
8. Train/Test time-based split
9. Feature scaling without data leakage
10. Sequence generation
11. Time-series validation
12. Multi-Step LSTM training
13. Early stopping
14. Test evaluation
15. Persistence baseline comparison
16. Actual vs. Predicted visualization

## Model Architecture

The LSTM model consists of:

- LSTM layer: 64 units
- Dropout: 0.2
- LSTM layer: 32 units
- Dropout: 0.2
- Dense layer: 16 units with ReLU
- Output layer: 4 neurons

The four output neurons correspond to the four forecasting horizons.

## Evaluation Metrics

The model is evaluated using:

- R²
- MAE

The LSTM model is also compared against a Persistence Baseline to determine whether the neural network provides meaningful improvement over a simple forecasting strategy.

## Technologies

- Python
- NumPy
- Pandas
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Jupyter / Google Colab

## Project Structure

```text
household-energy-forecasting-lstm/
│
├── notebooks/
│   └── household_energy_lstm.ipynb
│
├── results/
│
├── .gitignore
├── requirements.txt
└── README.md