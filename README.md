# NYC-Taxi-Trip-Time-Prediction-Project


**PROBLEM STATEMENT**

To Build a machine learning model that predicts the duration of NYC taxi trip using the dataset which includes pickup time, geo-coordinates, the number of passengers, and several other variables.

**APPROACHES**

**Step 1:**

To begin the data exploration and cleaning process, we first imported the required libraries, mounted the drive (if applicable), and stored the data in variables for further analysis. Checking for the presence of null values was crucial to avoid potential errors in subsequent steps. By assessing the existence of null values, we ensured that we could proceed with meaningful insights without any data inconsistencies.

![11](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/1f3ef98e-8325-4e1c-9bb8-72a1e09e80b7)

Luckily our dataset did not have any null values.

**Step 2:**

As part of the preprocessing and feature engineering steps, we converted two columns from timestamp format to datetime format. In addition, we performed feature engineering by creating an additional column called "distance" using geodesic distance calculation.

**Step 3:**

In the subsequent stage of data analysis and visualization, we focused on identifying the peak hours for both pickup and drop-off activities. Additionally, we determined the months during which taxi services experienced the highest usage. Furthermore, we examined the weekdays that exhibited a surge in taxi usage. To address outliers in our dataset, we utilized the quartile method. Moreover, we conducted a correlation check for multicollinearity by employing heatmaps and calculating the variance inflation factor (VIF).

![12](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/440612ed-45dc-43a3-bf76-173b9d0c5ef8)



![13](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/84ec9b39-a1f2-46f0-ae3c-777b5d7dba9f)



![14](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/890048f3-726a-4614-bd80-eda72abe3da4)



![15](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/004b68c8-65f1-4889-bfbe-e70932e2245d)



![16](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/d1335f3d-9745-4b47-bee4-292d4d25ee49)



![17](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/4a00ecc6-7b0b-442f-8cf5-b1311c788ac0)



![18](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/0bfa2196-2f0b-4e1a-82f2-39dcd1a622b8)


**Step 4:**

In the final step of our model training, we employed five different algorithms, namely linear regression, decision tree, XGBoost, gradient boost, and random forest. We then evaluated the performance of each algorithm using various metrics. Based on the comparison of these evaluation metrics, we selected and finalized one algorithm to train our model.

**SCORES:**

![19](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/33e535e8-fadd-4348-9789-23cc1ca2a996)


**R2 SCORES:**

![20](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/887e57dc-dcf6-491b-8a6e-25a8a5a5e883)


**MSE SCORES:**

![21](https://github.com/KamalRawalCS/NYC-Taxi-Trip-Time-Prediction-Project/assets/138231554/5dd6c4ef-e628-4f34-b238-6543e66d2605)

**CONCLUSION**

**(EDA)**

After conducting exploratory analysis, several insights were gathered. It was observed that the demand for taxi services reaches its peak during the months of April and March. Additionally, Fridays and Saturdays were identified as the weekdays with the highest demand, indicating a possible correlation with weekend parties or celebrations. Furthermore, a breakdown of the data on an hourly basis revealed that the majority of pickups and drop-offs occur in the morning around 10 am and in the late evenings, suggesting that people primarily utilize taxi services for commuting to and from their workplaces. Moreover, the analysis indicated that most individuals prefer solo travel and do not opt for carpooling. Finally, it was found that Vendor 2 had a significantly higher number of bookings compared to Vendor 1.

**(Model Training)**

After experimenting with five different algorithms (Linear Regression, Decision Tree, XG Boost, Gradient Boost, and Random Forest) for model training, we evaluated their performance using various metrics such as R2, Adjusted R2, MSE, and RMSE. Among these algorithms, only XG Boost yielded the highest accuracy score of 71% and exhibited lower MSE scores, indicating better predictive performance. We took care to optimize the model's parameters to prevent overfitting and ensure its generalization ability. As a result, XG Boost emerged as the most promising algorithm for our specific task.

