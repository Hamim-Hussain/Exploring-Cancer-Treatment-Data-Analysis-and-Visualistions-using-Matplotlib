# Matplotlib-Challenge
<img src="images/pharma.JPG" width="1000" height="491">

## Introduction 
In this project, I analysed an animal study on potential skin cancer treatments. 249 mice received various regimens, observing tumor development over 45 days. My roles were to generate: tables, figures, and a summary.

Tasked with data prep, I merged mouse_metadata and study_results DataFrames. Identifying duplicates, I created a clean DataFrame. Generating statistics, I calculated mean, median, variance, SD, and SEM for each drug regimen. Bar charts display row counts per regimen using both Pandas and Matplotlib. I also visualised gender distribution through pie charts.

For four treatment regimens (Capomulin, Ramicane, Infubinol, Ceftamin), I calculated final tumor volume, quartiles, IQR, and potential outliers. I created box plots to highlight outliers. A line plot showcases tumor volume over time for a specific mouse treated with Capomulin. A scatter plot reveals the correlation between mouse weight and tumor volume. Lastly, I calculated the correlation coefficient and plot a linear regression model for mouse weight and tumor volume.

## Source of Data
Within data folder in Pymaceuticals folder:
* Mouse_metadata.csv
* Study_results.csv

## Findings

### Summary Statistics
![summary_table_stats](images/summary_table_stats.JPG)

This table presents summary statistics for tumor volume based on different drug regimens. Each row corresponds to a specific drug regimen, and the columns represent various statistical measures:

1. Mean Tumor Volume: The average tumor volume for each drug regimen.
2. Median Tumor Volume: The middle value of tumor volume for each drug regimen.
3. Tumor Volume Variance: The variability of tumor volume values within each drug regimen.
4. Tumor Volume Std. Dev.: The standard deviation of tumor volume, indicating the spread of data around the mean.
5. Tumor Volume Std. Err.: The standard error of the mean, representing the uncertainty in the calculated mean.
   
For instance, looking at the "Capomulin" row:
- Mean Tumor Volume: 40.676
- Median Tumor Volume: 41.558
- Tumor Volume Variance: 24.948
- Tumor Volume Std. Dev.: 4.995
- Tumor Volume Std. Err.: 0.329

Comparing the effects of different drug regimens on tumor growth involves considering the mean tumor volume, which gives us an idea of the typical tumor size for each treatment. The median tumor volume is important because it's less sensitive to extreme values, providing a better representation of the central tendency of the data. We can gain insights into how different drug regimens affect tumor volumes. For instance, a lower mean and median, along with lower standard deviation and SEM, could indicate a more effective treatment in terms of reducing tumor size and keeping the sizes consistent. On the other hand, larger standard deviations and SEMs might suggest more variability and uncertainty in the treatment outcomes.

These statistics allow us to compare how tumor volumes behave under various drug regimens, understanding the average size, variability, and distribution of the tumors. This information aids in assessing the effectiveness of different treatments on tumor growth.

## Bar Chart
![bar2](images/bar2.JPG)

The bar plot showing the total number of timepoints for all mice tested for each drug regimen visualizes the amount of data collected over time for each specific drug treatment. Each drug regimen is represented on the x-axis, and the corresponding number of timepoints (measurements taken at different intervals) is depicted on the y-axis. This bar chart is important because it provides an understanding of the data density and distribution over the course of the study for each drug regimen. It helps us answer questions such as:

1. Data Collection Consistency: A consistent distribution of timepoints across different drug regimens suggests that the study was conducted rigorously and that each treatment group has a comparable amount of data. Inconsistent distributions might raise concerns about the reliability of the study's conclusions.
2. Treatment Duration: The chart can show whether all regimens had a similar duration for data collection. If some regimens have a significantly higher number of timepoints, it could indicate that the study lasted longer for those treatments, which could influence the analysis and conclusions.
3. Comparison of Regimens: By comparing the number of timepoints, we can assess which regimens were monitored more frequently and consistently. This could influence the reliability of observations and the effectiveness of the treatment.

The fact that the drug regimen 'Capomulin' has the highest number of timepoints while 'Propriva' has the lowest indicates 'Capomulin' to be a potential candidate that showed promising results (as shown in the statistic table above), prompting researchers to closely monitor its effects over time. On the other hand, 'Propriva' had fewer timepoints due to its lower perceived efficacy or less promising preliminary results.

## Pie Chart
![pie2](images/pie2.JPG)

The distribution of male and female mice is important because it provides insights into the composition of the study population and potential gender-related impacts on the research outcomes. Here's why the 51% male and 49% female distribution is significant:

1. Baseline Characteristics: Understanding the gender distribution ensures that the study is representative of both male and female mice, which are common in many preclinical studies. This helps in extrapolating the study results to a broader population.
2. Biological Differences: In certain medical conditions, such as cancer, there might be biological differences between genders in terms of susceptibility, disease progression, and response to treatment. An equal gender distribution allows researchers to analyze potential gender-specific effects.
3. Research Implications: If there's an imbalance in gender distribution, it could lead to biased results. For example, if there are more males than females, any observed effects might be specific to males and not applicable to females, and vice versa.
4. Clinical Relevance: The gender distribution also informs the relevance of the study findings to human patients. Understanding how different genders respond to treatments can influence clinical decisions in the future.
5. Regulatory Considerations: Regulatory bodies often require that preclinical studies have balanced gender distributions to ensure unbiased outcomes and to avoid overlooking potential gender-specific effects.
6. Data Interpretation: If the gender distribution is heavily skewed, it's important to consider the limitations in generalising the results to diverse populations, including both genders.

The 51% male and 49% female distribution is crucial for ensuring the study's validity, generalizability, and applicability to both genders, which is particularly important for cancer research where gender-related differences might impact treatment outcomes.

![boxplot](images/boxplot.JPG)

![line_chart](images/line_chart.JPG)

![scatter_plot](images/scatter_plot.JPG)

## Data Dictionary
1. **Mean** (Average): This column indicates the average tumor volume for each drug regimen. It gives an overall idea of the typical size of tumors under different treatments.
2. **Median**: The median tumor volume is the middle value in a set of tumor volumes sorted in ascending order. It's a measure of central tendency and is less influenced by outliers compared to the mean.
3. **Variance**: Variance measures the extent to which tumor volumes differ from the mean. A larger variance suggests greater variability among tumor sizes within a regimen.
4. **Standard Deviation**: This value indicates the spread or dispersion of tumor volumes around the mean. A higher standard deviation means more variability in tumor sizes.
5. **Standard Error of the Mean** (SEM): SEM quantifies the precision of the sample mean as an estimate of the population mean. It provides an estimate of how much the sample mean might vary from the true population mean.
