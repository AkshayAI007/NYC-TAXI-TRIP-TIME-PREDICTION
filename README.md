# AlmaBetter Certified Project :
![image](https://github.com/AkshayAI007/NYC-TAXI-TRIP-TIME-PREDICTION/assets/110448324/619ea78e-b37b-4ef0-aef8-c2c7ea1cf0d2)


# NYC-TAXI-TRIP-TIME-PREDICTION
![lexi-anderson-G8wPrJyNqWQ-unsplash](https://github.com/AkshayAI007/NYC-TAXI-TRIP-TIME-PREDICTION/assets/110448324/7669b096-0a69-46b2-a06f-d20193c438b9)

# Project Overview :
# Problem statement :
New York City is one of the most populous cities in the world, and its transportation system is a critical aspect of its infrastructure. Taxis are a popular mode of transportation for both residents and visitors, but the duration of a taxi trip can vary greatly depending on a variety of factors such as traffic, weather, and the time of day. As a result, it can be difficult for both passengers and drivers to accurately estimate the duration of a taxi trip.

The goal of this project is to develop a machine learning regression model that can predict the duration of a taxi trip in New York City based on various input features such as the pickup and dropoff locations, the time of day, and the distance of the trip. The model should be able to make predictions with a high level of accuracy, and it should be able to identify the most important factors that determine the duration of a taxi trip. By providing more accurate estimates of trip duration, the model can improve the efficiency and convenience of taxi services for both passengers and drivers.

# Project summary :
The NYC Taxi Trip Duration project is centered around a machine learning regression model designed to predict the duration of taxi trips in New York City. This prediction relies on various input features, including the pickup and dropoff locations, the time of day, and the trip's distance. The primary aim of the project is to enhance the efficiency and convenience of taxi services by furnishing more precise estimates of trip durations, benefiting both passengers and drivers.

The project utilizes historical data on NYC taxi trips, encompassing details like pickup and dropoff coordinates, timestamps, and trip distances. These datasets undergo preprocessing to address missing values and convert categorical variables, such as location names, into numerical representations. Feature engineering techniques are applied to derive additional insights, such as the day of the week, the time of day, and the spatial distances between locations.

For model development, diverse regression algorithms, such as linear regression, Random Forest, and XGBoost, are employed. Hyperparameter tuning is executed to optimize model performance. Evaluation metrics, including mean absolute error and R-squared, are used to assess model accuracy. Ultimately, the LightGBM Regression model emerges as the top-performing choice among the models tested.

The model is subjected to testing using a separate hold-out test dataset and demonstrates the capability to predict trip durations with remarkable precision. The results indicate that the model's predictions deviate by less than 10 minutes from actual trip durations on average.

The project delves into identifying key features influencing taxi trip durations. The findings emphasize that pickup and dropoff locations, time of day, and trip distance are the most influential factors determining trip duration.

In summary, the NYC Taxi Trip Duration project effectively develops a machine learning regression model for predicting trip durations in New York City. This model stands to benefit taxi companies by improving service efficiency and convenience through precise trip duration estimates for both passengers and drivers. Passengers can use this information for trip planning and informed decision-making.

Future enhancements for the model may involve integrating additional data sources, such as weather and traffic data, to account for external factors affecting trip durations. Furthermore, integrating real-time mapping and routing services could enable the provision of up-to-the-minute trip duration estimates based on current traffic conditions.

# Project workflow :

#  Problem Statement
#  Data Exploration
* Libraries
* Import Dataset
* Explore Data
# Exploratory Data Analysis
# Univariate Analysis
 1. Id
 2. Vendor Id
 3.Passenger
 4.Trip Duration
 5. Distance
 6. Speed
# Bivariate Analysis
 7. Trip Duration per Hour
 8. Trip Duration per Week
 9. Trip Duration per Month
 10. Trip Duration per Vendor
 11. Distance per hour
 12. Distance per WeekDay
 13. Distance per Month
 14. Distance per Vendor
 15. Distance v/s Trip Duration
 16. Average Speed per Hour
 17. Average Speed per WeekDay
 18. Passenger count per Vendor
 19. Pick Up v/s Dropoff Points
 20. Correlation Heatmap (Multivariate Analysis)
# Hypothesis Testing :

Hypothesis 1: Weekends has more traffic as compared to week days.

Hypothesis 2: Traffic hours on weekdays are different than traffic hours on weekends.

Hypothesis 3: Passengers which are travelling at a time is changing with change in vendor.
# Feature Engineering
Handling Missing values
Handling Outliers
Catagorical encoding
Feature Manipulation & Selection
Data Transformation
Data scaling
Dimensionality reduction
Data splitting
Handling imbalanced data

# 5. ML Model Implementation
Linear Regression
Lasso Regression
Reidge Regression
Elastic Net Regression
Decision Tree Regression
Random Forest Regression
Light Gradient Boost Machine
XGBoost Regression
# Performance Evaluation 
![Screenshot 2023-09-13 134019](https://github.com/AkshayAI007/NYC-TAXI-TRIP-TIME-PREDICTION/assets/110448324/6c584194-701f-4e9f-ae1d-89af5431d150)
# Conclusion :

# Conclusion from EDA:
Exploratory Data Analysis (EDA) is a crucial part of data analysis that enables an initial investigation of the dataset to identify patterns, anomalies, and relationships, detect potential issues, and inform advanced analytical methods. EDA also provides a thorough understanding of the data for informed decision-making and guides further analysis. After performing EDA we have drawn the following conclusions:

1) Vendor 2 is slightly more popular than Vendor 1 with similar number of trips.

2) Most trips have 1 or 2 passengers and the trip duration ranges from 10-20 minutes.

3) Average trip distance is 3.5 km, with highest distance recorded on Sundays.

4) Trip demand is stable throughout the year.

5) Average trip duration is shortest at 6 AM and longest during peak hours at 3 PM.

6) Trip duration increases from Monday to Thursday and then decreases until Sunday.

7) Average trip duration is highest in the 6th month and lowest in February.

8) Vendor 2 has higher average trip duration by 200 seconds compared to Vendor 1.

9) Trip distance is highest in early morning hours.

10) Average speed of taxis is higher on weekends and peaks at 5 AM.

11) Vendor 2 has higher average passenger count compared to Vendor 1.

12) Pickups are mostly concentrated in Manhattan while drop-offs are more spread out.

13) Also from hypothesis we get to know that, Weekend trips are more frequent than weekdays. Weekday and weekend traffic hours differ. Passenger count and vendor id are related.

# Conclusion from ML Model :
Effective implementation of an ML model requires proper data selection and preprocessing, regular evaluation and tuning, use of appropriate evaluation metrics, integration for easy maintenance, consideration of ethical and legal factors, appropriate algorithm choice, efficient hyperparameter tuning, and transparency in results.

We conducted a regression analysis starting with Linear Regression and exploring other non-linear models. For each model, we fine-tuned the hyperparameters in an effort to reduce errors and arrived at the following conclusions:

1)Our Linear Regression model achieved an accuracy of approximately 82.26%, however, it only captured 55% of the variance in the target variable (trip_duration). This suggests that the relationship between the features and the target is not a perfect linear dependence, even after using regularization techniques.

2)The Decision Tree model resulted in an accuracy of approximately 85.71% with a maximum depth of 16. Beyond this depth, the model began to suffer from overfitting and resulted in a MAPE (mean absolute percentage error) of 14.28%, which increased the overall error.

3) Focusing on each variable individually can lead to improved accuracy, as smaller subsets can still yield a high accuracy percentage. Using an ensemble technique, such as Random Forest, has demonstrated an accuracy of approximately 86.83% with 100 trees in the forest and after performing hyperparameter tuning.

4) I also tried the gradient boosting technique with LightGBM and obtained the best results of approximately 86.99%. The advantage of using LightGBM was that it utilized all available cores and reduced processing time. When training large datasets, one should consider using LightGBM for efficient and effective results in a shorter amount of time.

5)Finally, I implemented XGboost and achieved an accuracy of 86.89% with a mean absolute percentage error of only 13%.

"The optimal model was found to be LightGBM and its performance can be further improved by incorporating the concept of PCA for feature selection. The duration of trips may also be impacted by temporal factors, such as weather conditions. If this information is taken into account, it may result in even more accurate results."
