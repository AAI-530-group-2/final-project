# Drone Anomaly Detection

AAI-530 Group 2 Final Project

Aliaksei Matsarski and Andrew Fennimore

## About

This project builds and compares two deep learning approaches for classifying drone flight windows as healthy or faulty using time series sensor data. An LSTM classifier serves as a supervised baseline, while a 1D CNN Autoencoder provides an unsupervised anomaly detection alternative that learns only from healthy flight patterns. Model predictions are exported for interactive visualization in Tableau.


## Setup

1. Clone the repo
2. Install dependencies
   ```
   pip install -r requirements.txt
   ```
3. Open Group_2_Notebook.ipynb in Jupyter
4. Run the first cell to import all packages
5. Run the second cell to download the dataset from Kaggle. The first time it will ask you to log in through your browser. After that it remembers your credentials.

## How to Run

Run the notebook cells top to bottom. The notebook will:

1. Download the dataset from Kaggle
2. Load and inspect the data
3. Show summary statistics and check for missing values
4. Visualize class balance and feature distributions
5. Split the data 70/15/15 into train, validation, and test sets
6. Save the splits to data/ as .npz files
7. Train an LSTM classifier and evaluate on the test set
8. Train a 1D CNN Autoencoder on healthy samples and detect anomalies via reconstruction error
9. Compare both models and export predictions for Tableau

If you already have the splits saved in data/, you can skip straight to the modeling sections since they load from those files directly.


