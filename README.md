# Anomaly Detection in Real-Time Data Streams
## Project Overview: 
This project implements a Python script for detecting anomalies in 
continuous data streams. The script identifies unusual patterns, such as 
exceptionally high values or deviations from the norm, in real-time sequences 
of floating-point numbers. 
## Objectives: 
#### Algorithm Selection: 
Identify and implement a suitable algorithm for 
anomaly detection, capable of adapting to concept drift and seasonal 
variations. 
#### Data Stream Simulation: 
Design a function to emulate a data stream, 
incorporating regular patterns, seasonal elements, and random noise. 
#### Anomaly Detection:
Develop a real-time mechanism to accurately flag 
anomalies as the data are streamed. 
#### Optimization:
Ensure the algorithm is optimized for both speed and 
efficiency. 
#### Visualization:
Create a straightforward real-time visualization tool to display 
both the data stream and any detected anomalies.
## 1. Moving Z-Score 
Algorithm: Calculate the moving average and standard deviation of the data 
stream, then use the Z-score to identify anomalies. 
Strengths: 
- Simple to implement. 
- Adapts to changing mean and variance. 
Weaknesses:
- Assumes normal distribution.
- Sensitive to parameter choices (window size).
![image alt](https://github.com/GouthamiKethavath09/Anomaly-Detection-in-Real-Time-Data-Streams/blob/main/Moving%20Z-score.jpg?raw=true)

## 2. Exponential Smoothing (ES) 
Algorithm: Use ES to forecast future values, then detect anomalies based on 
residuals.  
Strengths: 
- Handles seasonality and trend.
- Robust to outliers. 
Weaknesses:
- Assumes stationary data. 
- Sensitive to parameter choices (smoothing factor).
![image alt](https://github.com/GouthamiKethavath09/Anomaly-Detection-in-Real-Time-Data-Streams/blob/main/Exponential%20smoothing.jpg?raw=true)

## 3. Isolation Forest (IF) 
Algorithm: Train an ensemble of decision trees to isolate anomalies instead of 
profiling normal data. 
Strengths: 
- Handles high-dimensional data.
- Robust to outliers.
- No assumption about data distribution. 
Weaknesses:
- Computationally expensive.
- Requires careful hyperparameter tuning.
![image alt](https://github.com/GouthamiKethavath09/Anomaly-Detection-in-Real-Time-Data-Streams/blob/main/isolation%20Forest.jpg?raw=true)
## 4. Autoencoder (AE) 
Algorithm: Train a neural network to reconstruct input data, then detect 
anomalies based on reconstruction error. 
Strengths: 
- Handles non-linear relationships.
- Robust to noise.
- No assumption about data distribution. 
Weaknesses:
- Requires large amounts of training data.
- Sensitive to hyperparameter choices.
![image alt](https://github.com/GouthamiKethavath09/Anomaly-Detection-in-Real-Time-Data-Streams/blob/main/AutoEncoder.jpg?raw=true)
## Requirements: 
1. NumPy (1.21.5) 
2. Scikit-learn (1.0.2) 
3. TensorFlow (2.8.0 ) 
4. Matplotlib (3.5.1) 
5. DataGenerator (optional, version depends on implementation)
## Optimization Techniques: 
1. Parallel Processing: Utilize multi-core processors or GPUs for accelerated 
computation. 
2. Cache Optimization: Minimize memory access latency using caching 
strategies. 
3. Efficient Data Structures: Use optimized data structures (e.g., arrays, 
matrices) for fast computation.

