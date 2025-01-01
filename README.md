## Sebokeng Air Pollution Clustering
This repository contains the methods followed to perform data clustering of the air pollution dataset 
based on similarities through the utilization of the machine learning algorithm called K-means clustering.
The process taken to find the correct number of groups (Elbow-Method) to cluster this data is mentioned without
overlooking the scaling of the data to ensure balanced input from all attributes of the dataset plus the distribution
and relationships of all the attributes. 

## Features
The dataset was given and there was no null values and duplicates to take care of. Based on the goal at hand which is to
group the air pollution data into different clusters depending on similarity, the type of algorithm that will be used is 
the K-means algorithm. Before the implementation of this algorithm, data had to be scaled using the standard scaler so
that that there is no datapoints that will have a much greater influence than the other attributes.

**State of the data**
The data consists of different types of air pollution concentrations that was recorded in 
each day including the measurement of their respective diameters. This data has 3347 
columns and 5 rows without any null values and duplicates. The state of the data can be 
seen in the table below.

![image](https://github.com/user-attachments/assets/b595e282-846a-4e37-a31a-c2fedf317e8a)

**Variable Description**
The variables of the dataset are all numerical(float) as can been seen in the above table. 
Statistics of the variables can be seen in the table below of which it includes the mean, 
standard deviation, minimum record, maximum record, 1st quartile, 2nd quartile and 3rd 
quartile for each attribute.

![image](https://github.com/user-attachments/assets/052740dd-3a5b-4c3b-bef4-3ec31d51f52f)

As can be seen in the table above that O3 has the greatest mean in comparison to other 
pollutants (SO2 and NO2) whilst the diameter with the greater mean is PM10 in comparison 
to the other diameter which is PM2.5.

**Correlation**
The relationship between the attributes of the data can be seen in the correlation 
heatmap below. The O3 attribute seems to have the weakest correlation with each and 
every attribute. The most common correlation values based on the heatmap are between 
0.2 – 0.8. 

![image](https://github.com/user-attachments/assets/f9c118cf-0af8-4cc7-92f6-ee4259e7817c)

Based on the heatmap above, the strongest correlation is 0.87 between the diameter 
attributes of the pollutants which are PM2.5 and PM10, and the weakest correlation can 
be found on any attribute correlated with O3.

**Elbow Method**
To determine the ideal number of clusters to use in the k-means algorithm, a method 
called the elbow method was implemented. And before the implementation of this method,
the data frame was scaled as mentioned previously. After the scaling was done, 11 clusters
were created with an aim to calculate the sum of squares error (SSE) and plot those sum of
squares error with an intention to visualization how does the change in the sum of squares
error decreases with an increase in the number of clusters. The sum of squares error against
the number of clusters is shown below.

![image](https://github.com/user-attachments/assets/09810a95-023f-4bca-8942-80e08706123f)

As can be seen in the plot above, the elbow is between cluster 2 and cluster 3. There is a 
huge SSE difference from the starting point to cluster 2 and then the SSE changes very 
slowly as the clusters increases of which this indicates that there is no huge difference 
between the clusters after cluster 2. Therefore, the ideal number of clusters is 2 hence 
the SSE does not change drastically in comparison to the beginning.

**K-Means Clustering**
After the number of suitable clusters has been selected, the scaled data is fitted in the k
means algorithm and the data records are predicted to their specific clusters. The predicted
clusters are injected in the scaled data frame as a column and the final data frame that has
the clusters is exported as an excel spreadsheet. The data clustering of each attribute 
against the other is shown in the figure below.

![image](https://github.com/user-attachments/assets/2a3bfbdc-c490-4045-9a62-60f9f06b57cd)

**Results**
The crucial step in this task of air pollution data clustering was the ability to choose the 
appropriate number of clusters utilizing the elbow method. The figure above shows that 
the data is grouped into cluster 1 and cluster 2 but these clusters are very close to one 
another meaning that an addition of other clusters will not be useful hence we already 
have clusters that have datapoints that are very close to one another. Therefore, the air 
pollution data was best grouped into two clusters and the figure above supports that.

### Requirements
To run the project, ensure you have the following installed:

- **Python 3.8+**
- **Libraries**
  - **pandas**
  - **numpy**
  - **matplotlib**
  - **seaborn**
  - **scikit-learn**



