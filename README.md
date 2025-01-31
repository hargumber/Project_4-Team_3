# Project_4-Team_3

- Title: A Multi-faceted Look at Storms: Trends, Impacts, and Public Sentiments

- Team members
Alexandra Kutz, Anvita Iyer, Daniel Allen, Hardeep Gumber and Krishan Pandey

- Objectives
The major objectives of this project are to analyze the storm events from the Atlantic basin and correlate the hurricane severity with damages and fatality. We analyzed the sentiments of the affected people as represented by their twitter tweets and correlated it with severity, damage and loss of life caused by major hurricanes. We used the data to train machine learning models and determine their accuracy.

- Data sources
The datasets containing storm events (1851-2024) at Atlantic basin were obtained from National Hurricane Center and Central Pacific Hurricane center, part of National Oceanic and Atmospheric Administration.

The dataset showing weather/climate disaster events (1980-2024) with more than $1 billion damages in the US was obtained from National Centers for Environmental Information, part of National Oceanic and Atmospheric Administration.

- Libraries used
matplotlib,  mpld3, numpy, pandas, plotly, quilt3, TroPYcal, 


- Data Analysis and Conclusions
1. There is an upward trend in the frequency of hurricanes occurring in the last 50 years.
2. Our results showed that damages and fatalities caused by hurricanes are dependent on multiple factors (e.g. socio-economic conditions, existing infrastructure and geographical locations), not just the hurricane severity.
3. Multiple models were developed and tested. 
4. For predicting Cost of Damage, RandomForestClassifier was used as a base model, and improved it by using XGBClassifier with RandomizedSearchCV. 82% Accuracy was achieved  to predict 1 from 3 classes,  
5. For predicting Number of Fatalities,  RandomForestClassifier was used as a base model and improved with XGBClassifier. 63% Accuracy was achieved to predict 1 from 4 classes and 96% Accuracy if it's a binary class
6. Sentiment analysis was also carried out using twitter data. 

Disclosure about AI usage

CHATGPT was used to make certain codes more succinct and concise.


**Project Overview 
(DANIEL ALLEN) 


As a member of TEAM 3, my primary objective was to ensure meteorological factors (e.g., wind speed, pressure, storm surge) were properly weighted against exposure-driven variables (e.g., population density, preparedness score). To create an optimized prediction model, the project involved extensive model testing, feature engineering, and bias mitigation strategies.   Unfortunately, because of the failures of the model development, the model I developed failed miserably when I measured its validity to another dataset of three cyclones/typhoons.   
**PROCESS 
1. Data Preprocessing & Feature Engineering o The dataset was cleaned and adjusted so all the numbers were on a similar scale. Using Standard Scale Gradient Boosting (GBM): Outperformed others regarding predictive accuracy and generalization.  
      Neural Networks: Showed poor performance due to dataset limitations. 
      Final Model: GBM with hyperparameter tuning (n_estimators=200, learning_rate=0.03, max_depth=6). 
2. Addressing Bias & Overfitting 
      Stratified Cross-Validation ensured balanced storm severity distribution across training and test sets. 
      Feature Weighting reduced Population Density’s dominance, improving model fairness. 
      Downsampling of high-population regions was attempted, but the feature importance was not sufficiently shifted. 
3. Final Model Performance 
      Gradient Boosting (GBM) Achieved:  
      Mean Squared Error (MSE): 3.4377 
      R² Score: 0.8331 
      BM demonstrated the best stability and predictive power in cross validation.
**REFERENCES: 
1. CHATGPT
2. Scikit-Learn Linear Regression: https://scikitlearn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html 
3. Seaborn Histplot: https://seaborn.pydata.org/generated/seaborn.histplot.html 
4. Mean Squared Error (Scikit-Learn): https://scikitlearn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html 
5. Python Module Reloading: https://stackoverflow.com/questions/76009840/how-toreload-a-module-in-python
6. CHATGPTSeaborn Heatmaps: https://seaborn.pydata.org/generated/seaborn.heatmap.html
7. TroPYcal library for plotting storm data.


