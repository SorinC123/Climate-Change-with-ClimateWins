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

### **Machine Learning Techniques**

**Convolutional Neural Network (CNN):** Applied this model in various configurations to identify different weather stations across Europe.
The model was also used to recognize images representing different weather types (e.g., rain, sunshine, etc.).

**Random Forest:** Used to plot two different trees to determine which weather stations are most influential (Maastricht, Basel, and Debilt), and
which indicators from which weather stations are most important in determining whether a day will be pleasant or not (for Maastricht are: precipitation, maximum and mean temperature).

**Hierarchical clustering:** Used to find actionable weather categorizations which help detect whether unusual weather patterns are occurring.

For the thought experiments the following ML Techniques were considered:

**Generative Adversarial Networks (GAN)**, which can analyze regional sky imagery to predict the likelihood of precipitation.

**Isolation Forest**, that is suitable for real-time or near-real-time anomaly detection.

**Variational Autoencoder**, popular in tasks like image synthesis and synthetic data creation.


## Key Results

**CNN Model for Visual Classification:** Achieved a validation accuracy of 75% when classifying weather conditions from images.

**Random Forest Model:** Improved the accuracy to 73% using hyperparameter tuning techniques like grid search.

**Time-Series Analysis:** Demonstrated the capability to predict weather patterns using RNN, focusing on long-term climate trends.


### Thought Experiments for ClimateWins

**GAN for Simulating Future Weather Scenarios:** Use Generative Adversarial Networks (GANs) to create simulated weather maps, helping to visualize potential climate changes.

**Transfer Learning for Rare Weather Events:** Apply pre-trained models on new data to detect and analyze rare weather patterns, such as extreme heatwaves.

**Ensemble Learning for Enhanced Predictions:** Combine CNN, RNN, and Random Forest outputs to form an ensemble model for more accurate weather predictions.


## **Results & Conclusions**
Machine learning models like CNNs are effective for image-based weather classification, with promising accuracy levels.

Random Forest and other ensemble methods provide robust results for structured data.

Deep learning approaches like RNNs are valuable for time-series predictions, especially for long-term trends.


## Next Steps
