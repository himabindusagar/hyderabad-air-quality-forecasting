 # Hyderabad PM2.5 Forecasting Using Machine Learning

## Project Overview
This project analyzes historical air-quality data from monitoring stations in Hyderabad, Telangana, and explores whether machine-learning techniques can forecast hourly PM2.5 concentrations.
PM2.5 refers to fine particulate matter that can affect human health. Forecasting its concentration can help identify pollution patterns and support further air-quality analysis.
The project compares a simple Persistence Baseline with an Enhanced Random Forest regression model to evaluate their performance in predicting PM2.5 concentrations one hour ahead.
 ## Objectives
	•	Analyze historical PM2.5 measurements.
	•	Clean and preprocess time-series air-quality data.
	•	Handle missing observations and prepare forecasting features.
	•	Create a next-hour PM2.5 prediction target.
	•	Train and evaluate a Random Forest regression model.
	•	Compare machine-learning performance against a Persistence Baseline.
	•	Visualize actual and predicted PM2.5 concentrations.
 ## Dataset
	•	Location: Hyderabad, Telangana, India
	•	Period: January 2024 – December 2025
	•	Original dataset size: 70,176 rows and 30 columns
	•	Target variable: Next-hour PM2.5 concentration
	•	Data frequency for forecasting: Hourly
The dataset contains air-quality measurements collected over time. Missing PM2.5 readings were identified during preprocessing and handled when preparing the forecasting dataset.
Note: Include the original dataset's source and access link here before publishing.
 ## Tools and Technologies
	•	Python
	•	Google Colab
	•	Pandas and NumPy
	•	Matplotlib
	•	Scikit-learn
	•	Time-series feature engineering
	•	Random Forest Regression
	•	MAE, RMSE and R² evaluation metrics
	•	Git and GitHub
## Methodology:
	1	Data loading: Loaded the historical air-quality dataset.
	2	Data cleaning: Inspected missing values and prepared the data for analysis.
	3	Time-series preparation: Converted measurements to an hourly frequency.
	4	Feature engineering: Created time-based and lag-based features to help forecast future PM2.5 concentrations.
	5	Target creation: Defined the target as the PM2.5 concentration one hour ahead.
	6	Train-test split: Used a chronological split to preserve time order.
	7	Model development: Evaluated a Persistence Baseline and an Enhanced Random Forest model.
	8	Model evaluation: Compared predictions using MAE, RMSE and R².
	9	Visualization: Plotted model comparisons and actual versus predicted concentrations.
## Model Performance:
The following results were obtained in the final evaluation using 1,603 valid test observations.
Metric
Persistence Baseline
Enhanced Random Forest
MAE
5.203
8.535
RMSE
9.391
13.420
R² Score
0.801
0.593
## Key Findings:
The Persistence Baseline outperformed the Enhanced Random Forest across all three evaluation metrics in this experiment.
The baseline predicts that the next-hour PM2.5 concentration will equal the current concentration. Its performance suggests that recent measurements provide a strong reference for short-term forecasting.
This result demonstrates why machine-learning models should be compared with simple baselines before concluding that a more complex model provides better predictions.
 ## Visualizations:
The notebook includes visualizations comparing:
	•	Persistence Baseline and Enhanced Random Forest performance.
	•	Actual PM2.5 measurements against model predictions.
	•	Changes in observed PM2.5 concentrations across the test period.
Project Structure:
Hyderabad-Air-Quality-Forecasting/
├── data/
│   └── air_quality.csv
├── notebooks/
│   └── Air_quality_hyd.ipynb
├── README.md
└── .gitignore
 ## Limitations: 
	•	The dataset contains missing PM2.5 observations.
	•	Sudden changes in pollution levels can be difficult to predict.
	•	The evaluation reflects the available dataset and test period.
	•	The current Random Forest model did not outperform the Persistence Baseline.
	•	Forecasting performance may change across monitoring stations, time periods and pollution conditions.
 ## Future Improvements:
	•	Test additional time-series forecasting approaches.
	•	Investigate the causes of large prediction errors.
	•	Evaluate performance separately across stations and pollution levels.
	•	Improve missing-data handling and feature engineering.
	•	Tune models using a validation set while keeping the test set for final evaluation.
	•	Compare results across different forecast horizons.
## Project Status:
Status: Initial forecasting experiments and evaluation completed. Preparing the repository for publication.
## Author: 
MSc Data Science Student
GitHub: https://github.com/himabindusagar/my-projects-.git
