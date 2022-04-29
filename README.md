

# Netflix Data Science Foundations Boot Camp Final Project
**Project Name**
Indicators-of-Heart-Disease-Analysis

**Project description**

By asking critical questions pertaining to heart disease and its associated risk factors, healthcare administration, healthcare workers, and policy makers will be able to better understand factors that affect heart disease, what areas of research should be focused on moving forward, and offer lifestyle changes to people without heart disease to lower the risk of developing a heart disease. 

This project is about statistically analyzing risk factors for heart disease and performing A/B testing, descriptive and inferential statistics to provide health care plans and strategies to better understand the risk factors assocaited with heart disease and give key insights into what factors contribute most heavily and least heavily to the development of heart disease. 


Technologies used:

Matplotlib,
Numpy,
Seaborn,
Matplotlib.style,
Plotly
for graphing

****Responsibilities:****

**Saad Iqbal**

Question 1: Does biological sex and BMI influence if someone develops a heart disease or not?
Hypothesis:
Biological sex and BMI will have a significant influence on the development of heart disease. 

We conducted a multiple linear regression, with BMI and biological sex as the independent variable and whether or not someone has a heart disease as the dependent variable. After running an OLS regression, we received a p-value of less than .01 and an adjusted R^2 value of .007. Thus, BMI and biological sex have a .07% variation in the development of heart disease. This is an extremely low percentage; therefore, even though the regression was significant, we should conduct further analysis on BMI and biological sex on its influence on the development of heart disease.

![Q1_Netflix](https://user-images.githubusercontent.com/94668201/165894270-ab25c831-2f8f-4302-902a-cc23a6ad01e2.png)


![Q1_Netflix_Saad](https://user-images.githubusercontent.com/94668201/165894282-f3968a34-4523-47f2-a139-793934769810.png)


**Jorge Angon**

Question 2: Does the amount of sleep a person gets influence if they will develop a heart disease?

Hypothesis: Less sleep time is correlated to the development of a heart disease

We began by dividing the entire dataset population into two samples: -people that reported no heart disease -people that reported having heart disease

First created a boxplot to compare the characteristics of the two samples

Both boxplots showed similar characteristics: Sample Median Sleep Time (hours) 0 - Reported no heart disease 7 1 - Reported heart disease 7

Since we saw the same median sleep time of 7 hours, we performed a 2-sample t-test to compare those samples and see if they have a statistically significant difference in means.

Test Samples P-Value 2 sample t-test Sleep time (h) of people that reported heart disease, sleep time (h) of people that didn’t report heart disease 2.492e-06

Based on the 2-sample t-test, we can reject the null hypothesis and say that there is a statistically significant difference between the means of the two samples.

Due to the results of the 2-sample t-test, we calculated the means of both samples for comparison: Sample Mean Sleep Time (hours) 0 - No heart disease 7.093 1 - Heart disease 7.136

Although we got statistically significant results from the 2-sample t-test, we can see that there is not a huge difference between the mean sleep time from both populations, therefore in this situation we need to consider other factors that could be affecting the results and look furthermore into this population to test our hypothesis.

To further investigate, we decided to get more samples based on the following age categories: • Young Adults: 18-44 • Middle-Aged Adults: 45-64 • Older Adults: 65+

We created a box plot to look more closely at the median sleep time of the samples in the young age category and we saw an hour difference between the median sleep time of the two samples, with the sample of people that reported heart disease having a lower median sleep time of 6 hours.

Young Adults Sample Median Sleep Time (hours) 0 – Reported no heart disease 7 1 - Reported heart disease 6

Since this aligned with our original hypothesis, we moved forward with a 2-sample t-test.

Test Young Adults Sample P-Value 2 sample t-test Sleep time (h) of young adults that reported heart disease, sleep time (h) of young adults that didn’t report heart disease 3.0132e-32

Due to the results of the 2 sample t-test above, we calculated the means of both samples for comparison:

Young Adults Samples Mean Sleep Time (hours) 0 - Reported no heart disease 6.963 1 – Reported heart disease 6.504

We obtained a very small p value that allowed us to conclude that there is a statistically significant difference between the means of the two samples. However, we when looked at the actual means, we saw that it was only about a half hour difference.

In the middle-aged adults population, which we defined as people in the age range of 45-64, we obtained the same sleep time median of 7 hours from a box plot of the two samples.

Middle-Aged Adults Sample Median Sleep Time (hours) 0 – Reported no heart disease 7 1 - Reported heart disease 7

Next, we performed a 2-sample t-test to see if there is a statistical difference between the distribution means from the two samples.

Test Middle-Aged Adults Sample P-Value 2 sample t-test Sleep time (h) of middle-aged adults that reported heart disease, sleep time (h) of middle-aged adults that didn't report heart disease 1.824e-32

Based on the 2-sample t-test, we can reject the null hypothesis and say that there is a statistically significant difference between the mean sleep time of samples of middle-aged adults that reported heart disease and that didn’t report heart disease.

Due to the results of the 2 sample t-test above, we calculated the means of both sampless for comparison:

Middle-Aged Adults Sample Mean Sleep Time (hours) 0 - Reported no heart disease 6.986 1 – Reported heart disease 6.786

Again, although we got statistically significant results from the 2-sample t-test, we can see that there is not a huge difference between the mean sleep time from both populations of middle-aged adults.

In the older adults population, which we defined as people 65 and older, we got the same results as the middle-aged adults for the median sleep time hours for our two samples.

Older Adults Sample Median Sleep Time (hours) 0 – Reported no heart disease 7 1 - Reported heart disease 7

Next, we performed a 2-sample t-test to see if there is a statistical difference between the distribution means from the two samples.

Test Older Adults Samples P-Value 2 sample t-test Sleep time (h) of older adults that reported heart disease, sleep time (h) of older adults that didn’t report heart disease 0.0347

The p-value for this test was barely small enough to pass the 5% confidence level, but it was still small enough to reject the null hypothesis and conclude that there is a statistically significant difference between the mean sleep time of samples of older adults that reported heart disease and that didn’t report heart disease.

Due to the results of the 2 sample t-test above, we calculated the means of both samples for comparison: Older Adults Sample Mean Sleep Time (hours) 0 - Reported no heart disease 7.350 1 – Reported heart disease 7.325

Again, although we got statistically significant results from the 2-sample t-test, we can see that the difference between the mean sleep time from both samples was extremely small.

To round out this analysis, we performed an ANOVA test to compare the mean sleep times across all age groups for people that didn’t report heart disease and we got a small enough p value (<0.01) to conclude there is a statistical difference between the means of each sample.

We also performed an ANOVA across all age groups for people that reported heart disease and again got a small p – value (7.229 e-147) that allowed us to conclude that there is a statistical difference between the means of each sample.

Overall, we can only conclude that less sleep time is correlated with the development of a heart disease in young adults aged 18-44, since that was the only instance where we saw a difference of ~30min in sleep time with the lower sleep time corresponding to the sample of people that reported heart disease. However, since we got statistically significant results in all our tests, this leads us to conclude that sleep time is only one of many contributing factors that could lead to the development of heart disease.

![Jorge1](https://user-images.githubusercontent.com/94668201/165894631-a48c4f4c-d5c4-447d-b31c-f74959eccba2.png)

![Jorge2](https://user-images.githubusercontent.com/94668201/165894642-ae2f8111-1192-4e44-b9a5-c12c736da204.png)
![Jorge3](https://user-images.githubusercontent.com/94668201/165894648-e0d5cdff-2f06-40d4-aa36-579abe120e61.png)
![Jorge4](https://user-images.githubusercontent.com/94668201/165894656-d7ca870a-4d0f-4964-b2c4-d6a6f6e25403.png)

**Frank King**

Question: Is there a relationship between age, stroke, and heart disease? 

Hypothesis: There will be a strong positive relationship, between age, stroke and heart disease.

In this section of the report, the age of individuals, stroke and heart disease were analyzed using the Chi-Squared Test. This test was used due to the data being categorical in nature. The figures in the section are as follows: The first table shows the original dataframe data and its values. The second table shows the dataframe that was filtered to categorize the values, count them and display them in a numerical form so that the data can be analyzed. The scatter plot shows the result of the data plotted on the same axis. This data was random in nature, which is a prerequisite for this test. Random in this context means, randomly chosen and there is no preset order to the data, it is unique, and the data does not mimic a gaussian distribution.

The data was placed in a function from the sci-py library which tests for the statistical value, the p-value and the degrees of freedom. The p values on the table, which is the last figure in this section, states that the null hypothesis needs to be rejected and that there is a significant association between the categories.

Unfortunately, This test does not show the different affects per age on either heart disease or stroke. In order to see this a post-hoc test would have to be used.

![Frank1](https://user-images.githubusercontent.com/94668201/165894707-a0b11407-078c-4d73-a636-695f0f04b754.png)


**Elliott Einstein**

Queestion 1: Can we identify which variables has the most influence on the development of heart disease?

Question 2: Can we classify if a person will have heart disease or not based on the given dataset?

Machine Learning Model

Used 3 Machine Learning Classifiers and compared their results against each other, to identify the best model for the classification prediction. 
Random Forest &AdaBoost makes predictions by applying multiple decision trees to every sample and combining the predictions made by individual trees. However, rather than taking the average of the predictions made by each decision tree in the forest (or majority in the case of classification), in the AdaBoost algorithm, every decision tree contributes a varying amount to the final prediction.Extra tree classifier implements a meta estimator that fits a number of randomized decision trees (a.k.a. extra-trees) on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting.


Machine Learning Classifiers

1. RandomForestClassifier
2. ExtraTreesClassifier
3. AdaBoostClassifier

Data Pre-Processing
The pie chart indicates that the ratio of people who have or do not have heart diseases is very imbalanced. In the 302,823 observations, only 9% of people actually have cardiac diseases.
If the algorithm was trained based on the original data, it is highly likely to create a model with extremely high accuracy, since the prediction tends to diagnose cases as negative and the majority of the data is also the negative case (HeartDisease = No).
In order to avoid the above-mentioned issue, one of the approaches is to ensure the percentage of the positive and negative cases is as similar as possible. In this case, we can either delete the negative samples or generate new synthetic samples as the following.
Undersampling can be defined as removing some observations of the majority class. This is done until the majority and minority class is balanced out.
Undersampling can be a good choice when you have a ton of data. But a drawback to undersampling is that we are removing information that may be valuable.


Confusion Matrix

True Negative 	False Positive


False Negative	True Positive

Classification Report

Provided Classification Reports of for each model.

Model Comparisons
Although the Random Forest and Extremely Random models performed at an accuracy of ~75%, AdaBoost achieved a higher score of 77% through the ensemble learning from the basic Decision Tree models. Among all three models, we can conclude that the AdaBoost model is the winner because it had the best accuracy (77%) and precision (70%) of positive predictions. 


![Elliott1](https://user-images.githubusercontent.com/94668201/165894737-623c6edf-2a8f-4852-aacd-80925a84e520.png)

![Elliott2](https://user-images.githubusercontent.com/94668201/165894741-46968660-8d39-4a03-b7a6-b43a616e6b07.png)

![Elliott3](https://user-images.githubusercontent.com/94668201/165894748-883ecbb7-d40c-4a79-9d06-2170b4b9b01c.png)

![Elliott Identifiers](https://user-images.githubusercontent.com/94668201/165894779-f3ae57b3-0527-414f-9e5d-0001b0e5dedd.png)

![Elliott CM1](https://user-images.githubusercontent.com/94668201/165894760-64df3bd2-25ab-4833-acfc-28754340cb52.png)
![Elliott CM2](https://user-images.githubusercontent.com/94668201/165894770-7c451e9d-358f-496a-baa1-48617ba7f975.png)
![Elliott CM3](https://user-images.githubusercontent.com/94668201/165894774-c347c1ca-6c49-489a-ad6c-d4501233a6eb.png)

**Team Members:** 

Saad Iqbal / https://github.com/zele-2198

Frank King / https://github.com/inventor-2-developer

Jorge Angon / https://github.com/jorgeangon

Elliott Einstein / https://github.com/Elliott-dev

