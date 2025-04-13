# **Weather Conditions and Climate Change with ClimateWins**
Machine Learning predictions

## **Overview**
As climate change accelerates, global weather patterns are becoming more erratic, leading to a rise in extreme weather events that put countless communities at risk.
To safeguard human safety and well-being, the company is leveraging machine learning to pursue the following objectives:
* Identify weather patterns outside the regional norm in Europe;
* Determine if unusual weather patterns are increasing;
* Generate possibilities for future weather conditions over the next 20 to 50 years based on current trends;
* Determine the safest places for people to live in Europe over the next 25 to 50 years.

![Euro](Pics/Europe-sm.jpg)

Photo by DALL·E 3

## **Datasets**

For this project, the following datasets were used:

1. **Weather Conditions Dataset**  
   Downloaded from Kaggle, this dataset includes images of various weather conditions such as sunny, cloudy, rainy, and snowy.  
   [Download](https://www.kaggle.com/datasets/pratik2901/multiclass-weather-dataset)

2. **European Historical Weather Data**  
   This dataset includes historical weather data from various European cities used for training and testing weather prediction models.  
   [Download](https://s3.amazonaws.com/coach-courses-us/public/courses/da-spec-ml/Scripts/A1/Dataset-weather-prediction-dataset-processed.csv)

3. **Handwritten Digits (MNIST)**  
   The MNIST dataset was used to train and test handwriting recognition models. This dataset contains images of handwritten digits from 0 to 9.  
   [Download](https://en.wikipedia.org/wiki/MNIST_database)

4. **Answers Dataset for Pleasant Weather Prediction**  
   Provided by Career Foundry, this dataset labels "pleasant" days as `1` and "unpleasant" days as `0`. It was used to evaluate different machine learning models for predicting pleasant weather based on weather observations.  
   *(This dataset is proprietary.)*

## **Machine Learning Techniques**

**Convolutional Neural Network (CNN):** Applied this model in various configurations to predict the weather for different weather stations across Europe.
The model was also used to recognize images representing different weather types (e.g., rain, sunshine, etc.).

**Random Forest:** Used to plot two different trees to determine which weather stations are most influential (Maastricht, Basel, and Debilt), and
which indicators from which weather stations are most important in determining whether a day will be pleasant or not (for Maastricht are: precipitation, maximum and mean temperature).

**Hierarchical clustering:** Used to find actionable weather categorizations which help detect whether unusual weather patterns are occurring.

**Long Short-Term Memory (LSTM):** Used historical data to generate long-term predictions, since weather and climate depend on prior conditions.

For the thought experiments the following ML Techniques were considered:

**Generative Adversarial Networks (GAN)**, which can analyze regional sky imagery to predict the likelihood of precipitation.

**Isolation Forest**, that is suitable for real-time or near-real-time anomaly detection.

**Variational Autoencoder**, popular in tasks like image synthesis and synthetic data creation.


## Results

**CNN Model for Visual Classification:** Achieved a validation accuracy of 71% when classifying weather conditions from images.

**Random Forest Model:** Improved the accuracy to 70% in weather station recognition using hyperparameter tuning techniques like grid search.

**Time-Series Analysis:** Demonstrated the capability to predict weather patterns using LSTM, focusing on long-term climate trends.


## Thought Experiments for ClimateWins

**1. Identify weather patterns outside the regional norm in Europe** - ClimateWins employs unsupervised machine learning techniques—Isolation Forest and Autoencoders—to identify anomalies by analyzing real-time weather data (such as temperature and precipitation) against 25 years of historical climate patterns.
 
**2. Generating Possibilities for Future Weather Conditions Over 20-50 Years** - ClimateWins uses Generative Adversarial Networks (GANs) and Variable Autoencoders (VAEs) to generate weather scenarios for Europe from 2045-2075.

**3. Determining the Safest Places to Live in Europe Over the Next 25-50 Years** - To identify Europe’s safest places to live in the next 25-50 years, ClimateWins leverages Random Forest and Extreme Gradient Boosting (XGBoost) models, balancing climate risks (floods, heatwaves) and socio-economic factors (healthcare, GDP).

## **Recommendations**

In order to achieve its objectives, ClimateWins needs to employ different machine learning techniques, depending on the specific goal:

**Identifying Weather Patterns Outside the Regional Norm in Europe:**

- Use Isolation Forest as Primary Tool: Its strength lies in fast, unsupervised anomaly detection across high-dimensional weather data (temperature, precipitation, wind), ideal for Europe’s diverse climates. 
- Supplement with Autoencoders: The experiment noted Isolation Forest’s focus on sharp anomalies—slow shifts (e.g., humidity drops).

**Generating Possibilities for Future Weather Conditions Over 20-50 Years:**
  
- Use GANs as Primary Tool: GANs generate diverse, non-linear scenarios (hot/dry, wet/wild), critical for 20-50-year horizons where physics models falter.
- Augment with Variational Autoencoders (VAEs): GANs risk overfitting (Paris’s 40°C too sharp). VAEs add uncertainty bands (e.g., 38-42°C).

**Determining the Safest Places to Live in Europe Over 25-50 Years:**

- Use Random Forest as Core Tool: Their strength in handling diverse features (climate risks, socio-economic metrics) and interpretability suits safety rankings.
- Enhance with XGBoost: Random Forest miss complex interactions (Milan’s grid vs. heat). XGBoost’s gradient boosting lifts Milan’s score accuracy.




