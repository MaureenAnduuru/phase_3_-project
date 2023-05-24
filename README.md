# phase_3_-project
# Tanzania water well
#Overview
This project aims to create a classifier that predicts the condition of water wells in Tanzania. Tanzania, as a developing country, faces difficulties in providing its population with clean, a water, the population of over 57 million people. Many of the existing water points require repair, have failed completely or are fully working, Data Understanding
The dataset consists of two files:
- `Training set values.csv`: Contains the training data for building the model.
- `Test set values.csv`: Contains the test data for evaluating the model and visualization.
In completing this analysis, I did not use any additional datasets as what had been provided by the stakeholders was adequate for the level of analysis we were carrying out.
Moreover, I created functions to support in the data understanding.

# The columns in the dataset are outlined below: 
Column Names and Descriptions for the Dataset
•	Amount tsh - Total static head (amount water available to waterpoint)
•	date_recorded - The date the row was entered
•	funder - Who funded the well
•	gps_height - Altitude of the well
•	installer - Organization that installed the well
•	longitude - GPS coordinate
•	latitude - GPS coordinate
•	wpt_name - Name of the waterpoint if there is one
•	num_private -
•	basin - Geographic water basin
•	sub village - Geographic location
•	region - Geographic location
•	region_code - Geographic location (coded)
•	district_code - Geographic location (coded)
•	lga - Geographic location
•	ward - Geographic location
•	population - Population around the well
•	public_meeting - True/False
•	recorded_by - Group entering this row of data
•	scheme_management - Who operates the waterpoint
•	scheme_name - Who operates the waterpoint
•	permit - If the waterpoint is permitted
•	construction_year - Year the waterpoint was constructed
•	extraction_type - The kind of extraction the waterpoint uses
•	extraction_type_group - The kind of extraction the waterpoint uses
•	extraction_type_class - The kind of extraction the waterpoint uses
•	management - How the waterpoint is managed
•	management_group - How the waterpoint is managed
•	payment - What the water costs
•	payment_type - What the water costs
•	water_quality - The quality of the water
•	quality_group - The quality of the water
•	quantity - The quantity of water
•	quantity_group - The quantity of water
•	source - The source of the water
•	source_type - The source of the water
•	source_class - The source of the water
•	waterpoint_type - The kind of waterpoint
•	waterpoint_type_group - The kind of waterpoint

# Data Cleaning:

Data cleaning was required, there were no duplicates in the data provided, some missing values were dropped.

# Data Analysis
Objective 1:  I plotted a graph waterpoint condition distribution and it showed that water wells constructed from 2007 to 2013 are functioning well as compared to wells in 1960.![image](https://github.com/MaureenAnduuru/phase_3_-project/assets/126090291/8d36055b-0341-4d64-ba6e-c55303256c4e)

Objective 2: A correlation matrix can be used to identify variables that are strongly correlated with each other, and may therefore be important predictors of a target variable. This can help in feature selection for predictive modeling tasks.![image](https://github.com/MaureenAnduuru/phase_3_-project/assets/126090291/85ca4320-9f0b-444b-b432-4a285681324e)


Objective 3:the graph shows the more the population the better the well is maintained and they are
fully functioning as compared to  places with low population![image](https://github.com/MaureenAnduuru/phase_3_-project/assets/126090291/54fd7add-b3bb-49ae-89d1-57d2d7e50550)


Explain your stakeholder audience and dataset choice here
The proposed audience for this solution includes NGOs focused on identifying wells in need of repair and the Tanzanian government, which can use the model to detect patterns in non-functional wells and inform future well construction.i chose this project because it aims to make a positive impact on water accessibility and contribute to the well-being of the Tanzanian population.


Model analysis
 I used logistic regression which showed the precision, recall, and F1-score for each class, and provides the accuracy of the model overall. the model achieved an accuracy of 0.60, with varying performance across the different classes. The model's performance is below average. It performs relatively well in predicting the "functional" class, but poorly in identifying instances that need repair ("functional needs repair" class). Overall, the model has difficulty recognizing instances that require repair, indicating the need for improvement. that's why we use the next model.
The KNN classifier achieved an accuracy of 0.70 when making predictions on the test data. The precision, recall, and F1-score for each class are provided in the classification report. The "support" column represents the number of samples in each class. In summary, the model's overall performance is decent, with better performance for the “functional" and "nonfunctional" classes compared to the "functional needs repair" class. However, there is room for improvement, particularly in correctly identifying instances requiring repair. We used the below model,
The Random Forest Classifier was trained on the training data and evaluated on the test data using the Tanzania water wells dataset. Here is a report on the performance of the Random Forest Classifier: The accuracy of the model on the test data is 0.79, indicating that it correctly predicted the condition of the water wells in 79% of the cases. The precision for the "functional" class is 0.81, which means that when the model predicts a water well as functional, it is correct 81% of the time. For the "functional needs repair" class, the precision is 0.49, indicating that the model has a lower accuracy in identifying wells that need repair. The precision for the "nonfunctional" class is 0.81, suggesting that the model performs well in identifying non-functional wells. The recall for the "functional" class is 0.86, indicating that the model correctly identifies 86% of the actual functional wells. The recall for the "functional needs repair" class is 0.35, suggesting that the model has difficulty in correctly identifying wells that need repair. The recall for the "nonfunctional" class is 0.78, indicating that the model identifies 78% of the actual non-functional wells. F1-Score: The F1-score combines precision and recall into a single metric. The F1-score for the "functional" class is 0.83, while for the "functional needs repair" class, it is 0.40. The F1-score for the "nonfunctional" class is 0.79. In summary, the Random Forest Classifier shows relatively good performance in predicting the condition of water wells, with higher accuracy, precision, recall, and F1-score for the "functional" and "nonfunctional" classes compared to the "functional needs repair" class.  there is room for improvement in identifying wells that need repair

# Evaluation


Based on the Classification Report, the final selected model has an overall accuracy of 0.80, which means that it correctly predicts the target variable 80% of the time.
precision metric measures the proportion of correctly predicted positive observations (true positives) out of all predicted positive observations. The recall metric measures the proportion of correctly predicted positive observations out of all actual positive observations. The f1-score is the harmonic mean of precision and recall.
The results show that the model performs well in predicting the functional and non functional classes with f1-scores of 0.84 and 0.80, respectively. However, the model performs poorly in predicting the functional needs repair class with an f1-score of 0.41. This indicates that the model has difficulty distinguishing between functional needs repair and non functional classes.
Overall, the weighted avg metric shows that the model has a precision of 0.79 and a recall of 0.80, which means that the model has a good balance between precision and recall across all classes.
In summary, the final selected model appears to perform well in predicting two out of the three target classes, but may require further improvement in predicting the functional needs repair class.

# Conclusion

 In conclusion, the Random Forest Classifier shows relatively good performance in predicting the condition of water wells, with higher accuracy, precision, recall, and F1-score for the "functional" and "nonfunctional" classes compared to the "functional needs repair" class.  there is room for improvement in identifying wells that need repair.
