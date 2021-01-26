# Food_And_Service_Restaurant_Recommendation_Engine

## Project Description

The analysis explored the Yelp business reviews data set https://www.yelp.com/dataset. 

Filtering for only restaurants and culinary businesses in Toronto, topic modeling was used to cluster data and mine for service-standard reviews. Once the clusters had been generated, singular value decomposition (SVD) was used to create two recommendation engines. One engine for all standard-based reviews (service and food) and another for food standard-based reviews. 

Having completed the above, a recommendation dashboard app using plotly and dash was created. The dashboard allows the user to have the choice if he/she wants to be recommended restaurants basis all standards or simply basis food standards. The recommendation dashboard app retruns 10 recommendations.

Anyone looking to explore and get a deeper look into Toronto's restaurants can use this app.

## Methods Used

1) Descriptive Statistics - used for preliminary data exploration.
2) Topic Modeling - Used to cluster reviews by their context
3) Singular Value Decomposition (SVD) - used to create 2 restaurant recommendation engines basis all standards or food standards 

## Results 

### Descriptive stats after cleaning and data preprocessing 

* **number of businesses** - 911
* **number of users** - 4,045
* **number of reviews** - 100,763

### Topic modeling

![](ReadMe_Images/Topics.png)

* **Topic0 AKA Topic1** - Service
* **Topic1 AKA Topic1** - Food
* **Topic2 AKA Topic1** - Food
* **Topic3 AKA Topic1** - Food

All topics generated represented the reviews they were assigned to by proportions greater than >= 50% 67% of the time.

Topic0 AKA Topic1                     |  Topic1 AKA Topic2
:------------------------------------:|:------------------------------------:
![](ReadMe_Images/T1.png)             |  ![](ReadMe_Images/T2.png)

Topic2 AKA Topic3                     |  Topic3 AKA Topic4
:------------------------------------:|:------------------------------------:
![](ReadMe_Images/T3.png)             |  ![](ReadMe_Images/T4.png)

### Singular Value Decomposition

**All Standards train**:

  * RMSE - 0.94
  * MAE - 0.73

**All Standards test**:

  * RMSE - 0.96
  * MAE - 0.75
  
 **Food Standards train**:

  * RMSE - 0.86
  * MAE -  0.67

**Food Standards test**:

  * RMSE - 0.89
  * MAE - 0.69
  
### Dashboard

![](ReadMe_Images/Dash1.png)

https://food-dash-app.herokuapp.com/

**User Name** - data
**Password** - analyst

## Technologies 

1) Python 
2) Jupyter Notebook
3) Anaconda Environment
4) Pyspark

## Order of Analysis

1) **Topic_Modeling.ipynb**
2) **Singular_Value_Decomposition_Recommendation_Engine.ipynb**
3) **Singular_Value_Decomposition_Recommendation_Engine_Food.ipynb**
4) **Recommendation_Dashboard.ipynb**

## Directory Files

1) **Data_Preprocessing.ipynb** - Cleaning and perprocessing large data using pyspark.
2) **Recommendation_Dashboard_Data_Prep.ipynb** - Preprocessing data to accomodate the recommendation dashboard.
3) **Topic_Modeling.ipynb** - Topic modeling dashboard.
4) **Singular_Value_Decomposition_Recommendation_Engine.ipynb** - SVD model for all review standards.
5) **Singular_Value_Decomposition_Recommendation_Engine_Food.ipynb** - SVD model for food review standards.
6) **Recommendation_Dashboard.ipynb** - Plotly and dash code for the recommendation dashboard.
