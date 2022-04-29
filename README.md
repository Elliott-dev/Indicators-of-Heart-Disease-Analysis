

# Netflix Data Science Foundations Boot Camp Final Project
**Project Name**
:Indicators-of-Heart-Disease-Analysis

**Project description**

By asking critical questions pertaining to heart disease and its associated risk factors, healthcare administration, healthcare workers, and policy makers will be able to better understand factors that affect heart disease, what areas of research should be focused on moving forward, and offer lifestyle changes to people without heart disease to lower the risk of developing a heart disease. 

This project is about statistically analyzing risk factors for heart disease and performing A/B testing, descriptive and inferential statistics to health care plans and strategies to better understand the risk factors assocaited with heart disease and give key insights into what factors contribute most heavily and least heavily to the development of heart disease. 



Technologies used:

Matplotlib,
Numpy,
Seaborn,
Matplotlib.style,
Plotly
for graphing



**Table of Contents:**

Relationships to be analyzed
Regions : Platform Sales
Genre : Critic Ratings
Genre : User Ratings
User Scores: Sales
Platforms : Global Sales
Genre Rankings

Created a table with the total averaged user_score based on the rating and genre

What are the demands in each region for the different game platforms?

How do components such as Genre and Critic Rating change over time?

What is the highest user score by genre filtered by rating?-Elliot Einstein

What is the highest purchased games by genre filtered by rating?-Elliot Einstein

Which platform (game console) has the highest global sales per genre?

What is the ranking order by genre in NA, EU, and Japan?

Which platform (game console) has the highest global sales?

Which platform (game console) has the highest global sales?

What is the ranking order of Genre in NA, EU, and Japan?

Which platform (game console) has the highest global sales?

What is the ranking order of Genre in NA, EU, and Japan?

****Responsibilities:****

**Saad Iqbal**
Question 1: Does biological sex and BMI influence if someone develops a heart disease or not?
Hypothesis:
Biological sex and BMI will have a significant influence on the development of heart disease. 


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

**Frank King**




**Team Members:** 

Saad Iqbal / https://github.com/samanthaameza

Frank King / https://github.com/DavidEinstein

Jorge Angon / https://github.com/Elliott-dev

Elliott Einstein / https://github.com/Stephbetanzo

