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

