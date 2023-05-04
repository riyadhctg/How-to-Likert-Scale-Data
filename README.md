## Notes on Statistics for Research Publications

### Ask yourself these questions first:
- Based on the data I collected, what can it tell me and what are the kinds of questions I can ask? 
- What's my research questions? 
- How will the dataset help me answer my research question? 

### Descriptive: 
Percentages are good to visualize. Generally, `stacked bar charts` are very good for visualizing the patterns in the data. You can describe how the data is distributed and summarize the trends. 

In addition to percentages to summarize the data, means, standard deviations, and medians are considered measure of central tendency, which are good to report.
 
### Comparison:
As for doing statistical tests, it depends if you have anything to compare and what to compare. For example, a chi square allows you to compare 2 nominal variables (to see if there is a relationship between them) -- e.g., marital status (single, married, diverced) and education (high school, bachelors, masters). 
 
For ordinal data, more can be done. For example, you might like to compare if the responses are above the midpoint. Depending on the distribution, you may like to run a Wilcoxon one-sample test if the distribution of the data looks skewed, but if the distribution is normal, you might like to run a one-sample t-test. 

### Hypothesis test:
Typically, a null hypothesis state that: `there is no difference between groups or no relationship between variables`

Reject the null hypothesis when the p-value is less than or equal to your significance level. 

Example:
If the p-value is more than the significance level (typically 0.05 or 0.01), the null hypothesis for the Shapiro-Wilk test is that a variable is normally distributed in some given population. Therefore, if the p-value is less or equal to the significance level, then it is not a normal distribution.
 
&nbsp;
&nbsp;
---

## Quick Statistic Refresher
- https://www.youtube.com/watch?v=4q5UZwwidRI&ab_channel=CSSLOhioStateU 

&nbsp;
&nbsp;
---

## Using SPSS to analyze the data

### How to input Likert data into SPSS:
https://www.youtube.com/watch?v=UxdWZzG42R8&ab_channel=Dr.ToddGrande 

&nbsp;
### Check If Normal or Skewed:
The `skewness` and `kurtosis` statistics value should be within ± 1.0 to be considered normal or as close to zero as possible.
However, in reality, data can be often skewed and kurtotic. A small departure from zero should not be a big issue, as long as the measures are not too large compare to their standard errors. Consequently, we need to divide the measure (Skewness and Kurtosis) by the standard error, which should give its z-value, which should be somewhere between -1.96 and +1.96.

Useful link: https://www.youtube.com/watch?v=IiedOyglLn0&ab_channel=KentL%C3%B6fgren 

We can also use Shapiro-Wilk Significance test for this. Here the null hypothesis is that the data is normally distributed, and if the p-value is equal or less than the significance level (e.g., 0.05), then we reject the null hypothesis.

**SPSS Steps**:
- Analyze > Descriptive Statistics > Explore
- Fill in the dependent variable (keep the factors empty so check normality of the entire dataset)
- In "Plots" - select Normality plots with test (for Shapiro-Wilk test)
- Look for Skewness and Kurtosis score

&nbsp;
### Descriptive statistics, percentages etc.:
Median, mode, mean etc. (Median is more appropriate for Likert scale data, since it is ordinal and distance between each Likert scale labels cannot be determined… though many assume the likert labels have equal distance, therefore use the mean anyway)

**SPSS Steps**:
- Analyze > Descriptive Statistics > Explore
- Fill in the dependent variable 
- Fill in the independent variable
- Observe the various data on the output

**SPSS steps: For overall percentage:**
- Analyze > Descriptive Statistics > Frequencies
- Statistics button > select the statistics needed
- Charts button > Select Bar charts and Percentages

**SPSS steps: Getting Stacked bar:**
- Short introductory video: https://www.youtube.com/watch?v=-Vzogn3NeSk
- Graphs > Graph Builder (drag it)
- *We can probably play with few variations and generate few graphs based on the need*
- For example:
	 - For x-axis > we can drag one of the factors
	 - For Stack > set color > we can drag the dependent variable (i.e, likert scale data / labels)
	 - For element properties > variable statistics > we can select percentage or count (or other option as appropriate)

&nbsp;
### Chi square:
**Good short tutorial to watch:**
https://www.youtube.com/watch?v=rW6u-tvYmGE&ab_channel=EasyStatisticsNow

**SPSS Steps:**
- Analyze > Descriptive Statistics > CrossTabs
- Put dependent variable(s) in Row, and independent ones (i.e., factors) in Column
- Statistics button > Select Chi-square. Select Phi and Cramer’s V
- Cells button > Select Observed and Expected


&nbsp;
### Wilcoxon signed rank test:
This test can be used for ordinal data, to check if the `hypothesized` median is the same as the `observered` median. 

**Good short tutorials to watch**:
- https://www.youtube.com/watch?v=prH4RJRyWnc&ab_channel=KnowHow
- https://www.youtube.com/watch?v=qTmfCjcRKls&ab_channel=stikpet

**SPSS Steps:**
- Analyze > Nonparametric test > One sample
- Then, in Objective > (select automatically compare….)
- In Fields > Keep the likert field in the test fields
- In Setting > Select customize test, select Wilcoxon signed-rank test, input hypothesized median


&nbsp;
### Paired t-test and Related-samples Wilcoxon signed-rank test
Example use case:
Use a paired t-test when each subject has a pair of measurements, such as a before and after score.

If your data is normal, then use paired t-test. Otherwise, you can use Related-samples Wilcoxon signed-rank test.

**Good short tutorials to watch**:
- https://www.youtube.com/watch?v=lAqbc8_t6fA&ab_channel=MohamedBenhima 

**SPSS Steps for Paired t-test:**
- Analyze > Compare Means > Paired Sampel T-Test
- Drag the variables that you want to test (i.e., two columns with each set of likert responses)

**SPSS Steps for Related-samples Wilcoxon signed-rank test:**
- Analyze > Non parametric test > Related Samples 
- From options you can select Wilcoxon test


&nbsp;
### Correlation (ICC, Pearson, Kendall, Spearman):
Example use case:
Compare responses of the same survey from two raters to check if their answers are correlated to each other

**SPSS Steps for ICC**
- Analyze > Scale > Reliability Analysis
- Drag the variables to Items
- Select Intraclass correlation coefficient at the bottom. Optionally, select other items in descriptive, summaries and inter-item if required
NOTE:
- The ICC score is between 0 and 1. A score of 0.5 indicate poor reliability, between 0.5 and 0.75 moderate reliability, between 0.75 and 0.9 good reliability, and any value above 0.9 indicates excellent reliability.
- It doesn't have any significance score.
- Short and useful video: https://youtu.be/1Avl7DzKmnc 

**SPSS Steps for Pearson / Kendall / Spearman**
- Analyze > Correlale > Bivariate 
- Drag the variables you want to compare from the left to right
- Select Pearson AND/OR Kendall's tau-b AND/OR Spearman
NOTES: 
- Pearson is for arametric data whereas Spearman and Kendall are both for non-parametric. Kendall is based on concordant and discordant pairs. It's more strict and usually same data yields less correlation score with Kendall compared to Spearman which calculates score based on deviations/distance.
- The coeffecient score is between +/-1. -1 means pure negative correlation, +1 means pure positive correlation. Anything positive typically suggests some correlations.
- It has a significance score that indicates whether the correlation is significant or not.



---
> ### Acknowledgement:
> Thanks to Dr. Chan for guidelines and tips.
