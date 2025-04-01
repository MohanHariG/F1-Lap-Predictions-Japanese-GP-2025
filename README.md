# F1-Lap-Predictions-Japanese-GP-2025
Predicting the Lap time of the players of the Japanese GP F1 2025

## Overview
This project predicts F1 qualifying lap times using machine learning. It leverages historical data and regression models to estimate Q3 lap times for each driver in an upcoming race.

## Features
- Fetches F1 data using FastF1
- Preprocesses and cleans data
- Trains a regression model (Linear Regression)
- Predicts qualifying times
- Evaluates model performance using Mean Absolute Error (MAE) and R² Score

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/f1-lap-prediction.git(give my repository URL)
   cd f1-lap-prediction 
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Enable FastF1 caching: if the cache folder is not created
   ```python
   import os
   import fastf1
   cache_dir = "cache"
   os.makedirs(cache_dir, exist_ok=True)  # Creates the directory if it doesn't exist
   fastf1.Cache.enable_cache(cache_dir)

## Usage
1. Run the script:
   ```bash
   python f1_lap_predictor.py
   ```
2. The script will display predicted qualifying results and model performance metrics.

## Output Example
```
Japanese GP 2025 Qualifying Predictions:
====================================================================================================
Position  Driver              Team                     Predicted Q3
----------------------------------------------------------------------------------------------------
1         Max Verstappen      Red Bull Racing          89.038s
...
Model Performance Metrics:
Mean Absolute Error: 1.79 seconds
R² Score: 0.65
```

## Potential Improvements
- Use more features like track temperature, tire compounds, and sector times.
- Experiment with advanced models like Gradient Boosting or Neural Networks.
- Improve data preprocessing and augmentation.

## License
This project is open-source under the MIT License.
