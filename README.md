# Customer_Segmentation_with_Unsupervised_Learning
## Table of Context
### 
- Business Problem

- Source of dataset

- Importing Dataset, Required Library and Functions

- Exploratory Data Analysis
    1. Overview
    2. Analysis of Categorical Variables
    3. Analysis of Numerical Variables
    4. Analysis of Correlation
    
    
- DATA PREPROCESSING
    1. Missing Values (Eksik Değerler) and Feature Extraction (Özellik Çıkarımı) 
    2. Outliers (Aykırı Değerler)
    3. LOG TRANSFORMATION
    4. Feature Scaling (Özellik Ölçeklendirme) 

- Modelling(KMeans)  
- Modelling(Hierarchical Clustering)    
- REPORTING

## Report
The project's objective is to perform Customer Segmentation using K-Means and Hierarchical Clustering by leveraging RFM Metrics, while also exploring alternative metrics to enhance the depth of clustering insights.

## Stages conducted within the scope of the project:

### 1. Importing and Loading Phase:
- Required Libraries and Functions imported and dataset read

### 2. via Exploratory Data Analysis:
- The structural information of the data set was examined.
- Descriptive statistics of the data set were examined.
- The size information of the data set has been reached.
- The types of categorical and numerical variables in the data set were examined and visualized.
- Categorical and numerical variables were analyzed.
- Correlation between variables observed and visualized.

### 3. In data preprocessing process:

- As a result of the outlier analysis, 3 variables(Recency,Frequency,Monetary) with outliers were observed  among the numerical variables and were suppressed by the threshold values determined by the IQR values.
- During the Feature Extraction phase, 3 new variables were produced.
- Before the modeling phase, the variables were scaled with the StandartScaler method.

### 4. In Model Building Phase:

This stage encompasses the process of constructing your model using data mining techniques to perform customer segmentation. To determine customer segments, we applied two different methods: K-Means Clustering and Hierarchical Clustering.

**K-Means Clustering**: Firstly, we scaled the data and utilized the "Elbow Method" to determine the optimal number of clusters. The K-Means algorithm was then executed with the determined optimal cluster count. Each customer was assigned to these clusters, resulting in the creation of the "KMeans_Segments" column, indicating the segment to which each customer belongs. Subsequently, the means and medians of Recency, Frequency, and Monetary values were calculated for each segment.

Additionally, box plots of "Monetary" values were drawn to visualize these segments.

**Hierarchical Clustering**: As the second method, a hierarchical clustering tree was constructed using the data. This tree was visualized using a dendrogram, and a specific similarity threshold at 1.2 was applied to cut the tree. This cut was used to partition customers into subgroups, and each customer was assigned a "Hierarchi_Segments" column, indicating their segment based on the results of hierarchical clustering.

Finally, means and medians of Recency, Frequency, and Monetary values were calculated for each hierarchical segment. Box plots of "Monetary" values were also drawn to visualize these segments.

These two distinct clustering methods assist in understanding customer behaviors and values, forming a crucial foundation for determining marketing strategies and objectives.

