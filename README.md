# Taxi Demand Prediction (Machine Learning)

## Project Overview

New York City is known for its iconic yellow taxis, which play a vital role in the city's transportation system. However, with the rise of ride-sharing services like Uber and Lyft, the taxi industry faces significant challenges. This project aims to predict the demand for yellow taxis in NYC, enabling drivers to position themselves where demand is highest, thereby maximizing their revenue and improving taxi utilization.

## Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Project Phases](#project-phases)
  - [Phase 1: Initial Exploration and Data Analysis](#phase-1-initial-exploration-and-data-analysis)
  - [Phase 2: EDA - Analyzing Locations and Time Intervals](#phase-2-eda---analyzing-locations-and-time-intervals)
  - [Phase 3: Data Cleaning and Feature Engineering](#phase-3-data-cleaning-and-feature-engineering)
  - [Phase 4: Data Aggregation](#phase-4-data-aggregation)
  - [Phase 5: Univariate Forecasting with ARIMA](#phase-5-univariate-forecasting-with-arima)
  - [Phase 6: LSTM Networks](#phase-6-lstm-networks)
- [Conclusion](#conclusion)
- [Team](#team)
- [Usage](#usage)
- [Acknowledgments](#acknowledgments)

## Business Problem

Yellow taxis in NYC are a critical component of the city's transportation network. Despite their importance, they often struggle to meet demand during peak times, leading to longer wait times for passengers. This project aims to enhance the utilization of yellow taxis by providing real-time demand predictions. The goal is to help taxi drivers:

- Position themselves in areas with higher predicted demand.
- Increase their revenue by reducing idle time.
- Compete more effectively with ride-sharing services.

## Project Phases

### Phase 1: Initial Exploration and Data Analysis

- **Install and upgrade packages**
- **Load CSV files as Dask DataFrame**
- **Create Data Dictionary**
- **Parse dates using `map_partitions`**
- **Identify and correct erroneous dates**
- **Save DataFrame as Parquet for efficient storage**

### Phase 2: EDA - Analyzing Locations and Time Intervals

- **Load Parquet files from disk**
- **Analyze time intervals of partitions**
- **Visualize the number of trips by boroughs**
- **Focus on trips in Manhattan**
- **Analyze the number of trips by pickup location**

### Phase 3: Data Cleaning and Feature Engineering

- **Remove extreme outliers**
- **Clean and validate passenger count**
- **Analyze trip distance and fares**
- **Calculate trip duration and speed**

### Phase 4: Data Aggregation

- **Downsample time-series data grouped by location**
- **Apply aggregate functions: sum, average, count**
- **Determine the optimal frequency of samples with minimal null values**

### Phase 5: Univariate Forecasting with ARIMA

- **Combine data from 2017 and 2018**
- **Forward fill zeros to handle missing data**
- **Conduct visual inspection of time-series data**
- **Perform Augmented Dickey-Fuller and KPSS tests**
- **Plot Partial Auto-correlation and Auto-correlation**
- **Grid search for ARIMA parameters with the lowest AIC**
- **Implement walk-forward validation**

### Phase 6: LSTM Networks

- **Preprocess data for LSTM models**
- **Build Vanilla LSTM model**
- **Scale data for neural network training**
- **Diagnose model performance**
- **Develop Stacked LSTM model for enhanced predictions**

## Conclusion

Our model can be deployed in yellow taxis, providing real-time demand predictions to drivers. This helps them to position themselves strategically, increasing their earnings and improving service efficiency. This project has been an incredible journey, enriching our understanding of data science and machine learning.

## Team

- **Vishal Sharma**
- **Apoorv Goyal**
- **Kayshav Kaushik**

## Usage

1. **Clone the repository:**

   ```sh
   git clone https://github.com/vishxlshxrma/Taxi_Demand_Prediction.git
   cd Taxi_Demand_Prediction
   ```

2. **Install the required packages:**

   ```sh
   pip install -r requirements.txt
   ```

3. **Run the analysis and models:**

   - Follow the Jupyter notebooks provided in the repository for each phase of the project.
   - Ensure the datasets are placed in the correct directories as specified in the notebooks.

## Acknowledgments

We extend our gratitude to all those who supported us during this project. Special thanks to our mentors and peers for their invaluable feedback and encouragement.
