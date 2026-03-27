# Time Series Forecasting of Air Passengers using LSTM Neural Networks

## Overview
This project implements a Long Short-Term Memory (LSTM) neural network for time series forecasting using the AirPassengers dataset. The objective is to model and predict monthly airline passenger traffic based on historical trends.

The model leverages deep learning techniques to capture temporal dependencies and sequential patterns in the data.

---

## Problem Statement
Time series forecasting is critical in domains such as transportation, finance, and demand planning. This project aims to:

- Learn temporal patterns from historical passenger data
- Predict future passenger counts using sequence modeling
- Evaluate the effectiveness of LSTM networks for time-dependent data

---

## Dataset Description

The dataset contains monthly totals of international airline passengers from 1949 to 1960.

### Features:
- `Month`: Timestamp (monthly frequency)
- `Passengers`: Number of passengers

---

## Methodology

### 1. Data Preprocessing
- Converted date column to datetime format
- Set date as index
- Normalized data using MinMaxScaler

---

### 2. Supervised Learning Transformation
Time series data was converted into supervised learning format using a sliding window approach.

- Time step (window size): 12 months
- Each input sequence predicts the next time step

---

### 3. Model Architecture

The model is built using a Sequential architecture with LSTM layers:

- LSTM Layer (50 units, return sequences)
- LSTM Layer (50 units)
- Dense Output Layer (1 unit)

Total parameters: 30,651

---

### 4. Training Configuration

- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam
- Epochs: 100
- Batch Size: 16
- Train-Test Split: 80/20

---

## Results

### Training Behavior
- Training loss decreases steadily, indicating effective learning
- Validation loss stabilizes but shows slight fluctuations in later epochs

### Model Performance
- The model captures overall trend and seasonality
- Predictions align well with actual values in training data
- Slight deviation observed in test predictions, especially at later time steps

---

## Visualization

The following outputs are generated:

- Original time series plot
- Training predictions vs actual data
- Test predictions vs actual data

These plots demonstrate the model’s ability to learn temporal patterns.

---

## Key Insights

- LSTM effectively captures sequential dependencies in time series data
- Seasonal patterns (annual cycles) are learned through the 12-step window
- Model performance depends on sequence length and training stability

---

## Limitations

- Model may overfit due to small dataset size
- Performance degrades for long-term forecasting
- No hyperparameter tuning applied
- Single feature (univariate time series)

---

## Future Improvements

- Use multivariate time series (add external features)
- Apply hyperparameter tuning (units, layers, learning rate)
- Use advanced architectures (GRU, Bidirectional LSTM)
- Implement regularization (Dropout)
- Add evaluation metrics (RMSE, MAE)
- Perform cross-validation for time series

---

## Project Structure

├── AirPassengers.csv
├── lstm_model.py
├── README.md 

---

## Installation

### 1. Clone the Repository

git clone https://github.com/your-username/lstm-time-series.git
cd lstm-time-series

### 2. Install Dependencies
pip install -r requirements.txt

---

## Running the Project
python lstm_model.py

---

## Model Details

- Model Type: Recurrent Neural Network (LSTM)
- Input Shape: (Time Steps = 12, Features = 1)
- Output: Single-step forecast
- Scaling: MinMaxScaler

---

## Conclusion

This project demonstrates the application of LSTM networks for time series forecasting. The model successfully learns temporal patterns and provides reasonable predictions for short-term forecasting.

However, improvements in model tuning and dataset expansion are necessary for more robust and generalized performance.

---

## Author

Sandeep S L  
MSc Data Analytics (Computational Science)  
Digital University of Kerala  

---

## License

This project is open-source and available under the MIT License.
