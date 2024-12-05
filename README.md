### Predicting Customer Churn for SyriaTel: Identifying Key Factors and Reducing Attrition
### Business Understanding
The data for this project was obtained from Kaggle. The primary stakeholders for this project include the marketing and customer service teams at SyriaTel, as well as senior management. SyriaTel, is a prominent telecommunications company, that faces significant revenue losses due to customer churn. This project aims to build a predictive model to identify customers at risk of churning by analyzing various features such as customer demographics, usage patterns, and billing information. By understanding the key factors influencing churn and predicting which customers are likely to leave, SyriaTel can implement targeted retention strategies, improve customer satisfaction, and ultimately enhance business sustainability. This approach not only helps in retaining valuable customers but also optimizes marketing efforts and reduces the costs associated with customer acquisition.

### Problem Statement:
SyriaTel faces significant revenue losses due to high customer churn. This project aims to develop a predictive model to identify at-risk customers and implement effective retention strategies.

### Business Objectives
Based on the problem statement, SyriaTel company has to set some objectives in order to curb the problem of customer churning. These are the objectives that will be resolved after creating a model that will address the business churning problem:

- To identify the primary factors influencing customer churn at SyriaTel.

- To determine whether predictive model can accurately identify customers who are likely to churn.

- To determine whether the insights gained from the churn prediction model be used to enhance customer retention strategies.

- To identify what business processes or interventions can be implemented based on the churn predictions to reduce customer attrition.

### Data Understanding
The dataset for this analysis includes features related to customer demographics, usage patterns, and billing information. Key features include the state of residence, length of account, area code, international plan, voice mail plan, total minutes and charges for calls made during the day, evening, and night, as well as the number of customer service calls. The target variable, churn, indicates whether a customer has left the service. This data provides a comprehensive overview of customer interactions, helping to identify patterns and factors that contribute to churn, enabling effective predictive modeling.

### Data Preparation 
Data Preparation involves transforming raw data into a suitable format for analysis. This step includes data cleaning, handling missing values, encoding categorical variables, normalizing numerical features, handling outliers, and creating new features through feature engineering. Proper data preparation ensures that the dataset is consistent and ready for the modeling phase, improving the performance and accuracy of the models.

### Exploratory Data Analysis (EDA)
This is a crucial step in the data science process that involves systematically exploring and summarizing the major features of a dataset. This includes summarizing the data, visualizing distributions, identifying patterns and relationships, and detecting anomalies or outliers. EDA helps in gaining insights into the data, guiding feature selection, and informing subsequent data preparation and modeling steps. Common techniques i used here include histograms, bar plots, scatter plots, box plots, and correlation heatmaps.The aim here is to gain a deeper understanding of the data, identify patterns, relationships and anomalies.

### Data Visualization

I have used various visuals to explain the trend in customer churn.
1. ##### Distribution of international plan:
This bar plot visualizes the distribution of customers based on their subscription to the international plan. By grouping the data by the "international plan" feature and plotting the sizes of each group, the chart clearly shows the number of customers who have subscribed to the international plan compared to those who have not. The x-axis represents whether a customer has an international plan ("yes") or does not ("no"), and the y-axis shows the number of customers in each category. The title of the plot, "Distribution of International Plan," indicates the focus of this visualization. This plot helps identify if there's a significant difference in the number of customers with or without the international plan, which can be crucial for understanding customer preferences and tailoring marketing strategies. 

2. ##### Distribution of mail voice plan
This bar plot visualizes the distribution of customers based on their subscription to a voice mail plan. By grouping the data by the "voice mail plan" feature and counting the number of customers in each group, the chart provides a clear comparison between the two categories. The x-axis represents whether a customer has a voice mail plan ("yes") or not ("no"), while the y-axis shows the number of customers in each category. The title of the plot, "Distribution of Voice Mail Plan," indicates the focus of this visualization. The bars, colored in light coral, help illustrate the popularity of the voice mail plan among customers, allowing stakeholders to quickly assess the proportion of customers who have subscribed to this feature versus those who have not. This insight can be valuable for making decisions related to customer service and feature offerings.

3. ##### Number of customers by state
This count plot provides a visual representation of the number of customers in each state. By grouping the data based on the 'state' column and counting the number of customers, the plot highlights which states have the highest or lowest customer counts. The x-axis represents the states, sorted in descending order of customer count, and the y-axis shows the number of customers in each state. The plot is particularly useful for identifying patterns of market penetration, indicating where the company has the strongest or weakest presence. The plot's title, "Number of Customers by State," sets the context for the visualization, and the rotated state labels on the x-axis make the chart easier to read. This insight can help stakeholders make strategic decisions regarding regional marketing efforts and resource allocation.

4. ##### Number of customers by area code
This count plot visualizes the number of customers based on their area code, providing a clear understanding of the geographic distribution of the customer base. The x-axis represents the different area codes, and the y-axis shows the number of customers within each area code. The plot is a useful tool for identifying which regions have higher concentrations of customers, allowing for targeted marketing strategies and resource allocation. By analyzing the number of customers across different area codes, stakeholders can better understand regional preferences and tailor their marketing efforts to specific areas with more precision. The title, "Number of Customers by Area Code," succinctly describes the focus of the plot, making it easy for viewers to grasp the insights it provides. This visualization helps highlight geographic trends and patterns in customer distribution.


5. ##### Distribution of total day minutes
This histogram visually represents the distribution of total day minutes used by customers. By plotting the frequency of different usage levels, the histogram helps in understanding how much time customers spend on calls during the day. The x-axis represents the total day minutes, divided into 20 bins, and the y-axis shows the frequency of customers within each usage range. The title, "Distribution of Total Day Minutes," succinctly captures the focus of the plot, while the labels on the axes provide clarity on the measured variables. This visualization is valuable for identifying patterns in customer behavior, such as common usage levels and potential outliers, which can inform decisions related to service plans and customer segmentation.

6. ##### Distribution of total eve minutes
This histogram illustrates the distribution of total evening minutes used by customers. By plotting the frequency of different usage levels, the histogram helps in understanding how much time customers spend on calls during the evening. The x-axis represents the total evening minutes, divided into 20 bins, and the y-axis shows the frequency of customers within each usage range. The title, "Distribution of Total Eve Minutes," clearly indicates the focus of the plot, while the labels on the axes provide clarity on the measured variables. The maroon color adds visual distinction to the chart. This visualization is valuable for identifying evening usage patterns, such as common usage levels and potential outliers, which can inform decisions related to service plans and customer engagement strategies during the evening hours.

7. ##### Box plot of total day minutes by churn
This histogram illustrates the distribution of total evening minutes used by customers. By plotting the frequency of different usage levels, the histogram helps in understanding how much time customers spend on calls during the evening. The x-axis represents the total evening minutes, divided into 20 bins, and the y-axis shows the frequency of customers within each usage range. The title, "Distribution of Total Eve Minutes," clearly indicates the focus of the plot, while the labels on the axes provide clarity on the measured variables. The maroon color adds visual distinction to the chart. This visualization is valuable for identifying evening usage patterns, such as common usage levels and potential outliers, which can inform decisions related to service plans and customer engagement strategies during the evening hours.

8. ##### Box plot of total night minutes by churn
This box plot compares the distribution of total night minutes for churned versus non-churned customers, providing insights into potential differences in night-time usage that might be linked to customer churn. On the x-axis, it distinguishes between customers who have churned (True) and those who have not churned (False). The y-axis represents the total night minutes.

The box plot highlights key statistical measures such as the median (the line inside each box), the interquartile range (the box, representing the middle 50% of data), and possible outliers (points outside the whiskers). The median gives an idea of the central tendency for each group, while the spread of the interquartile range shows the variability in night-time usage.

This visual comparison helps identify if churned customers have different night-time usage patterns compared to non-churned customers. Such insights can be crucial for tailoring customer retention strategies, potentially revealing if high or low night-time usage correlates with a higher likelihood of churn. Additionally, spotting outliers can indicate unique usage behaviors that might require special attention.

9. ##### Correlation heatmap
This heatmap visualizes the correlation between different features in the dataset, providing valuable insights into the relationships among variables. The correlation coefficient values, ranging from -1 to 1, indicate the strength and direction of the relationships.

- A value close to 1 implies a strong positive correlation, meaning as one feature increases, the other tends to increase as well.

- A value close to -1 implies a strong negative correlation, meaning as one feature increases, the other tends to decrease.

- A value close to 0 suggests no significant linear relationship between the features.

The color gradient in the heatmap, ranging from cool (blue) to warm (red) colors, visually represents the correlation coefficients. Features like Total Day Minutes and Total Day Charge, Total Eve Minutes and Total Eve Charge, Total Night Minutes and Total Night Charge, and Total Intl Minutes and Total Intl Charge show very high correlation, as indicated by their darker red colors and values close to 1. This strong correlation is expected because these features are directly derived from each other (e.g., charges are calculated based on usage).

Additionally, identifying features that are highly correlated with the target variable (churn) can guide feature selection and engineering for predictive modeling. For example, if Total Day Minutes shows a significant correlation with churn, it might be a valuable predictor in the churn prediction model.

Overall, the heatmap serves as a crucial tool for understanding feature interdependencies, simplifying the feature selection process, and enhancing the overall model performance by avoiding multicollinearity issues.

10. ##### Propotion of churned versus non-churned customers
This pie chart visualizes the proportion of customers who have churned compared to those who have not. By displaying the data in a circular graph divided into segments, it provides a quick and clear overview of the churn rate within the dataset. The chart is divided into two segments: one representing customers who have churned (colored in orange) and the other representing those who have not churned (colored in green). The sizes of the segments are proportional to the number of customers in each category, and the percentage labels give precise information about the distribution. The title, "Proportion of Churned vs. Non-Churned Customers," succinctly describes the focus of the chart. This visual is valuable for stakeholders to quickly assess the overall churn rate and understand the balance between retaining and losing customers, which is crucial for planning retention strategies and improving customer satisfaction.

11. ##### Pairplots of selected features
This pair plot visually explores relationships between multiple features—total day minutes, total evening minutes, total night minutes, and total international minutes—and their association with customer churn. By plotting each feature against the others, the pair plot helps identify patterns, trends, and potential interactions between features and the target variable (churn).

In this plot:

- The x-axis and y-axis represent different combinations of the selected features.

- Each point in the scatter plots represents an individual customer, with different colors indicating whether the customer has churned or not (as specified by the 'hue' parameter).

- The diagonal plots show the distribution of each feature for churned and non-churned customers, providing insight into how these distributions compare.

The title, "Pair Plot of Selected Features," describes the focus of the visualization. By examining these relationships, stakeholders can better understand how various usage metrics interact and how they might collectively influence customer churn. This can guide feature selection and engineering in predictive modeling, as well as help in identifying key factors that contribute to customer churn. The interactive nature of the pair plot makes it a powerful tool for exploratory data analysis, revealing complex relationships that may not be evident from univariate analysis alone.

### Modelling
Modeling data is crucial because it aids in understanding patterns, relationships, and trends within the dataset. Additionally, it enables businesses and researchers to make informed choices, predict future outcomes, optimize processes, and identify insights that might not be immediately apparent. Modelling can also help us to test hypotheses, quantify uncertainty, and improve accuracy in decision-making. Ultimately, data modeling transforms raw data into valuable, actionable information. 
I used various modelling function to predict customer churn. For instance, i used logistic regression model, decision tree model, random forest classifier, and k-nearest neigbors. 

#### Logistic Regression Model Results
The Logistic Regression model achieved an overall accuracy of 85.6%, indicating it correctly predicted 85.6% of the cases in the test set. However, the detailed evaluation metrics reveal significant challenges in predicting customer churn. The precision for the "True" class (customers who churn) is high at 1.00, but the recall is extremely low at 0.01, which means the model correctly identifies only 1% of the actual churners. This suggests the model is heavily biased towards predicting non-churn cases (False), as evidenced by its perfect recall of 1.00 for the "False" class. The weighted average of precision, recall, and F1-score further indicates this imbalance. The confusion matrix shows that out of 145 actual churn cases, only 1 was correctly predicted, while the remaining 144 were misclassified as non-churn. These results highlight the need for further tuning or addressing class imbalance to improve the model's ability to accurately predict churners.

#### Decision Tree Model
The Decision Tree model achieved an overall accuracy of 93%, indicating it correctly predicted 93% of the cases in the test set. The model shows strong performance with high precision and recall for both churn and non-churn cases. For non-churn cases (False), the precision is 0.94 and recall is 0.98, meaning the model accurately identifies a large majority of non-churn customers. For churn cases (True), the precision is 0.83 and recall is 0.66, which is a significant improvement compared to the Logistic Regression model. The F1-scores, which balance precision and recall, are 0.96 for non-churn and 0.73 for churn cases, demonstrating the model's overall effectiveness. The confusion matrix shows that out of 145 actual churn cases, the model correctly identified 95 and misclassified 50 as non-churn. These results highlight the Decision Tree model's capability to handle class imbalance better than the Logistic Regression model, making it a more reliable option for predicting customer churn.

#### Random Forest Classifier
he Random Forest model achieved an overall accuracy of 88.9%, which indicates that it correctly predicted 88.9% of the cases in the test set. The model shows excellent performance in predicting non-churn cases (False), with a precision of 0.89 and a perfect recall of 1.00, meaning it identified all non-churn customers correctly. However, the performance for churn cases (True) is less satisfactory. The precision for churn cases is 0.95, which indicates that when the model predicts a customer will churn, it is correct 95% of the time. Nonetheless, the recall is quite low at 0.25, meaning it correctly identified only 25% of the actual churners.

The F1-score for non-churn cases is 0.94, demonstrating strong overall performance in this category. Conversely, the F1-score for churn cases is only 0.39, highlighting the model's struggle with detecting churn cases accurately. The confusion matrix reveals that out of 145 actual churn cases, only 36 were correctly identified, while 109 were misclassified as non-churn.

These results suggest that while the Random Forest model is robust in predicting non-churn cases, it requires further tuning or methods to address class imbalance to improve its ability to predict churn cases effectively.

#### K-Nearest Neighbors (KNN)
The K-Nearest Neighbors (KNN) model achieved an overall accuracy of 86%, indicating it correctly predicted 86% of the cases in the test set. The performance metrics show a significant disparity between the prediction of non-churn and churn cases. For non-churn cases (False), the precision is 0.86 and recall is 1.00, meaning the model accurately identifies all non-churn customers. However, for churn cases (True), the precision is 0.78, but the recall is extremely low at 0.05. This indicates the model struggles to identify actual churners, correctly predicting only 5% of the churn cases.

The F1-score for non-churn cases is 0.92, reflecting strong performance in this category, while the F1-score for churn cases is only 0.09, highlighting the model's poor performance in predicting churn. The confusion matrix reveals that out of 145 actual churn cases, only 7 were correctly identified, while 138 were misclassified as non-churn.

These results suggest that the KNN model is heavily biased towards predicting non-churn cases, and like the Logistic Regression model, it requires further tuning or methods to address class imbalance to improve its ability to predict customer churn effectively.


### Evaluation
While the Logistic Regression model achieved an accuracy of 85.6%, it struggles with predicting customer churn accurately, showing low recall and precision for churn cases. The Decision Tree model stands out with a 93% accuracy, demonstrating strong performance in predicting both churn and non-churn cases. The Random Forest model also shows high accuracy at 88.9%, with excellent precision for non-churn cases, but it needs further improvement for churn predictions. Similarly, the K-Nearest Neighbors (KNN) model, although accurate at 86%, has difficulty with churn prediction, similar to the Logistic Regression model. Overall, the Decision Tree model is the most effective for predicting customer churn among the models evaluated, though there is room for enhancement in all models to better handle class imbalance and improve churn prediction accuracy.

### Conclusion
In this project, we built predictive models to identify at-risk customers for SyriaTel, with the Decision Tree model showing the best performance at 93% accuracy. Feature engineering and EDA helped enhance the dataset for better modeling. Key recommendations include targeted marketing and proactive support to reduce churn. Overall, the project provides actionable insights to improve customer retention.

### Recommendations

- To enhance customer satisfaction and reduce churn, stakeholders should:

- Implement targeted marketing campaigns and personalized offers for at-risk customers.

- Offer proactive support and improved training for customer service representatives which are crucial in assisting customers.

- Gather and act on customer feedback to drive product and service improvements.

- Increase customer engagement through personalized communication and maintaining transparency in billing to build trust and satisfaction.

- Regular monitoring and updating the churn prediction model to ensure its accuracy, allowing for data-driven decisions. Foster cross-departmental collaboration and exploring partnerships to add value and strengthen customer retention efforts.






>>>>>>> origin/main
