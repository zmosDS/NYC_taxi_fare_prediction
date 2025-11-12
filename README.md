# NYC Taxi Fare Prediction (2014–2024)

Predicting NYC Yellow Taxi fares using large-scale trip data and a tuned LightGBM model.  
**Notebook:** [View model notebook](https://github.com/anon/nyc-taxi-eda/blob/Milestone3/model_1_final.ipynb)

## Goal
Build an accurate fare estimator from trip features (distance, duration, tolls, time of day, passenger count) and surface key patterns in the taxi system.

## Built With
- Python (Pandas, NumPy, Matplotlib)
- Apache Spark / PySpark
- LightGBM
- Jupyter Notebook

## Features
- Scalable EDA on 2014–2024 Yellow Taxi trips  
- Rigorous cleaning and outlier filtering  
- LightGBM regression trained on 150M+ rides  
- Residual analysis vs. distance, time, tolls, hour  
- Plots for distribution, distance bins, and residuals  

## Results
| Metric | Linear Regression | LightGBM (Train) | LightGBM (Test) |
|:--|:--:|:--:|:--:|
| RMSE | 5.24 | 2.55 | 2.66 |
| MAE | 3.95 | 1.85 | 1.91 |
| R²  | 0.74 | 0.94 | 0.94 |

Test RMSE ≈ \$2.66 (≈17% of average fare). Model explains ~93% of variance.

## Figures
<p align="center">
  <img src="https://github.com/user-attachments/assets/8f7abab6-b052-4ea4-8d68-a5ffa7831dcf" alt="Fare Amount Distribution" width="450"/>
  <img src="https://github.com/user-attachments/assets/34cf691a-2a8c-4a80-bbf5-763464bf7d5b" alt="Trip Distance Distributions" width="500"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/c946c92b-066c-4e7d-b940-17ff9f76cc07" alt="Residuals vs Features" width="500"/>
</p>

## Files
```
NYC_taxi_fare_prediction/
├── model_1_final.ipynb # Fare prediction notebook (LightGBM)
├── nyc_taxi_data/ # Parquet trip data (not included in repo)
├── figures/ # Screenshots and plots used in README
├── README.md # Project overview
└── requirements.txt # Python dependencies
```

## Data Source
New York City Taxi & Limousine Commission (TLC):  
https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page  
Parquet archive (2014–2024):  
https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_[YYYY]-[MM].parquet

## Author
## Author
Developed by students at UC San Diego for the DSC 232 Group Project, Spring 2025.  
Each team member contributed across all project milestones.  

**Zack Mosley** — Model 1
