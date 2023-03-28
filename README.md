# Detection-and-Handling-Outliers-In-Data
![image](https://user-images.githubusercontent.com/92606737/227701124-1c5371e9-c5c5-443e-9de4-e7be63815f0c.png)

# Outliers
Outliers are data points that are significantly different from the other data points in a dataset. These data points can be much higher or lower than the average value of the dataset and can sometimes be considered "noise" in the data.

## Impact of Outliers:
Outliers can have several negative impacts on machine learning models, including:

- __Skewed results__
   Outliers can cause statistical measures such as mean, median, and standard deviation to be skewed, resulting in inaccurate or biased results.

- __Increased error__

   Outliers can increase the variance of the data, leading to increased error in machine learning models.

- __Overfitting__
  
  Outliers can also lead to overfitting, where a model is overly complex and fits the noise in the data rather than the underlying patterns.

- __Misleading results__

   Outliers can mislead or obscure the underlying patterns in the data, leading to incorrect conclusions or predictions.

- __Reduced generalization__
   
   Outliers can also reduce the generalization of a model, making it less applicable to new data.

It is therefore important to detect and handle outliers appropriately in order to ensure the accuracy and validity of machine learning models.

## Method of Visiualizing the Outliers:
There are several types of plots that can be used to detect outliers in a dataset, including:
- Box plots
- Scatter plots
- Histograms
- QQ plots
- Violin plots

# 2 Methods for Dealing with Outliers:
- ## Trimming 

    Trimming involves removing a certain percentage of data points from the dataset, typically at the extremes of the distribution. For example, if 5% of the data points are to be trimmed from each end of the distribution, the top 5% and bottom 5% of data points would be removed. This can be an effective method for reducing the impact of outliers on statistical analysis, particularly if the outliers are suspected to be due to measurement error or other factors that are not relevant to the analysis.
    
- ## Capping 

   Capping involves setting a maximum or minimum value for the data points in the dataset. Data points that exceed the maximum or minimum value are replaced with the maximum or minimum value, respectively. For example, if the maximum value for a dataset is capped at 100, any data points above 100 would be replaced with 100. This can be an effective method for handling outliers that are due to extreme values that are still relevant to the analysis.
   
   
### Conclusion:

Both trimming and capping can be useful techniques for handling outliers in a dataset, but they should be used with caution. Removing or capping data points can alter the distribution and range of the dataset, and may lead to biased or inaccurate results in statistical analysis. Additionally, these techniques may not be appropriate for all datasets or types of analysis, and their use should be based on careful consideration of the underlying data and research question.


# Methods for handling and detecting the Outliers:
## Z-Score:
![image](https://user-images.githubusercontent.com/92606737/227702235-4736459f-ea95-4453-b40d-429eae0a4760.png)

The Z-score method is a statistical technique for detecting outliers in a dataset. The method involves calculating the Z-score for each data point, which is the number of standard deviations the data point is away from the mean of the dataset. Mathematically, the Z-score of a data point x is given by:

Z-score = (x - mean) / standard deviation

where "mean" is the mean value of the dataset and "standard deviation" is the standard deviation of the dataset.

Once the Z-scores have been calculated, data points with a Z-score above a certain threshold (often 3 or -3) are considered outliers. A Z-score of 3 means that the data point is three standard deviations away from the mean, which is a highly unlikely event in a normally distributed dataset.

### Handling using Z-Score:
To handle outliers using the Z-score method, 
- Trimming (you can simply remove the data points with Z-scores above the threshold)
- Capping (replace them with a more reasonable value)

#### Assumption 
Z-score method assumes that the dataset follows a normal distribution, and may not work well for datasets with other types of distributions. Additionally, the Z-score method may not work well for datasets with a small number of data points, as the mean and standard deviation may not be representative of the data.

# IQR (Interquartile Range)
![image](https://user-images.githubusercontent.com/92606737/227759238-a234d7bf-58d7-425d-86f9-04b9ca70e8de.png)

- This is used mostly when the data is not distributed normally.


The IQR (Interquartile Range) method is a technique for identifying and removing outliers from a dataset. It is based on the quartiles of the dataset and the concept of the interquartile range, which is the difference between the third quartile (Q3) and the first quartile (Q1).

To use the IQR method to remove outliers, we first calculate Q1, Q3, and IQR for the dataset. Then, we define a threshold value, typically 1.5 times the IQR, above and below which data points are considered to be outliers. Any data points that fall outside of this range are considered outliers and can be removed from the dataset.

#### Assumption
The IQR method is a robust method for identifying and removing outliers that does not assume any particular distribution of the data. It is also relatively easy to implement and does not require any assumptions about the underlying distribution of the data.

#### Conclusion
However, the IQR method can be quite conservative in identifying outliers, especially in datasets with a small number of observations. In addition, the threshold value used to define outliers is somewhat arbitrary and can be adjusted based on the specific needs of the analysis. Finally, the IQR method may not be appropriate for all datasets and may need to be supplemented with other techniques for identifying and handling outliers.

