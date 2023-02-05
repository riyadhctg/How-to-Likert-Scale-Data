## How to Analyze Likert Scale Data

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
The `skewness` and `kurtosis` statistics value should be less than ± 1.0 to be considered normal.

**SPSS Steps**:
- Analyze > Descriptive Statistics > Explore
- Fill in the dependent variable (keep the factors empty so check normality of the entire dataset)
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


### Paired t-test and Related-samples Wilcoxon signed-rank test
Example use case:
Comparing likert responses for the same question sets from two participants... or asking the same questions before and after and look for the differences.

If your data is normal, then use paired t-test. Otherwise, you can use Related-samples Wilcoxon signed-rank test.

**Good short tutorials to watch**:
- https://www.youtube.com/watch?v=lAqbc8_t6fA&ab_channel=MohamedBenhima 

**SPSS Steps for Paired t-test:**
- Analyze > Compare Means > Paired Sampel T-Test
- Drag the variables that you want to test (i.e., two columns with each set of likert responses)

**SPSS Steps for Related-samples Wilcoxon signed-rank test:**
- Analyze > Non parametric test > Related Samples 
- From options you can select Wilcoxon test



---
> ### Acknowledgement:
> Thanks to Dr. Chan for guidelines and tips.
