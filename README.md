# Mod-5-Project

## Categorizing Car Origin

### Research Question:
  Can we predict the origin of a car based off various characteristics of the vehicle? And, if so, how accurate are our predictions?
  
### Data:
  In order to gather enough data for the assignment, I used BeautifulSoup to webscrape from autoevolution.com. This website provided technical specifics on over 6,000 vehicles. This information includes Top Speed, Acceleration (from 0-62 mph or 0-100 kmh), Cylinder Type, Dimensions, Weight, Torque, and Towing Capacity. Using my discretion and feature engineering, I reduced the amount of variables to 9, including Year, Weight, Top Speed, Acceleration, Height, Length, Width, MPG, and Trunk Space, with the target variable of Domestic=1 vs. Foreign = 0. These variables were used due to their general lack of correlation, as well as because they are more continous varialbes instead of discrete. This allowed their ranges to be more clearly gauged against one another
  
### Modeling:
  
  I chose to run 3 different categorical models for my dataset in order to determine which style of modeling may produce the best outcome. My strongest models were with the Decision Tree and Boosting models giving me an overall accuracy measurement of around 75%. I believed accuracy was the metric most important to this particular modeling, because the overall grouping of the cars is more important than just making sure you get all of the domestic cars or missing any particular group of car.
  
  **Decision Tree:**
  
      Accuracy Score - 75.89%
      Recall Score - 80.68%
      F1 Score - 79.53%

  **Boosting: Adaboost vs Gradient Boost**
    
    Adaboost
    Training Metrics
      Accuracy: 0.7090773809523809
      F1-Score: 0.7090773809523809
    Testing Metrics
      Accuracy: 0.6676587301587301
      F1-Score: 0.6676587301587301

    Gradient Boost
    Training Metrics
      Accuracy: 0.798859126984127
      F1-Score: 0.798859126984127
    Testing Metrics
      Accuracy: 0.7490079365079365
      F1-Score: 0.7490079365079365
      
    Confusion Matrix
    
  **Support Vector Matrix**
  
    Precision Score: [0.48095238, 0.59649123]
    Recall Score: [0.23877069, 0.81367521]
    Accuracy Score: 0.5724206349206349
    F1 Score: [0.31911532, 0.68835864]
