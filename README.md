# NYPD_Data_Analysis
 NYPD-Shooting-Incidents-Data-Analysis
 
 
### Introduction and Background

Analyzing NYPD shooting incidents is crucial for understanding crime patterns and informing public safety strategies. This analysis can provide actionable insights to law enforcement and policymakers to address crime hot spots, allocate resources effectively, and develop targeted interventions to reduce gun violence.

### Objective of the Analysis

Our analysis aims to evaluate the usefulness of the NYPD shooting incident data since 2006 and to provide actionable insights and recommendations for improving this process in the future.

### NYPD Shooting Incident Data (Historic)

#### Metadata Updated: April 26, 2024

This dataset contains records of every shooting incident that occurred in NYC from 2006 through the end of the previous calendar year. The data is manually extracted quarterly and reviewed by the Office of Management Analysis and Planning before being posted on the NYPD website. Each record includes information about the event, location, time of occurrence, and suspect and victim demographics. This dataset can be used by the public to explore the nature of shooting/criminal activity.

Source: NYPD Shooting Incident Data (Historic) <https://catalog.data.gov/dataset/nypd-shooting-incident-data-historic>

#### NYPD Shooting Incident Data Sample

The following is the first 10 lines of the NYPD Shooting Incident dataset.

-   We will download the information from the website here: <https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8/about_data>.

### Column Names, Descriptions, Types of data and other related information:

NYPD Shooting Incident Level Data Footnotes

1.  Information is accurate as of the date it was queried from the system of record, but should be considered a close approximation of current records, due to revisions and updates.

2.  Data is available as of the date that technological enhancements to information systems allowed for data capture. Null values appearing frequently in certain fields may be attributed to changes on official department forms where data was previously not collected. Null values may also appear in instances where information was not available or unknown at the time of the report and should be considered as either “Unknown/Not Available/Not Reported.”

3.  A shooting incident can have multiple victims involved and as a result duplicate INCIDENT_KEY’s are produced. Each INCIDENT_KEY represents a victim but similar duplicate keys are counted as one incident.

4.  Shooting incidents occurring near an intersection are represented by the X coordinate and Y coordinates of the intersection Shooting incidents occurring anywhere other than at an intersection are geo-located to the middle of the nearest street segment where appropriate.

5.  Any attempt to match the approximate location of the incident to an exact address or link to other datasets is not recommended.

6.  Many other shooting incidents that were not able to be geo-coded (for example, due to an invalid address) have been located as occurring at the police station house within the precinct of occurrence.

7.  Shooting incidents occurring in open areas such as parks or beaches may be geo-coded as occurring on streets or intersections bordering the area.

8.  Shooting incidents occurring on a moving train on transit systems are geo-coded as occurring at the train’s next stop.

9.  All shooting incidents occurring within the jurisdiction of the Department of Correction have been geo-coded as occurring on Riker’s Island.

10. X and Y Coordinates are in NAD 1983 State Plane New York Long Island Zone Feet (EPSG 2263).

11. Latitude and Longitude Coordinates are provided in Global Coordinate System WGS 1984 decimal degrees (EPSG 4326).

12. Errors in data transcription may result in nominal data inconsistencies.

13. The CSV file should be opened using an appropriate tool for data exploration, e.g. SPSS, SAS, Tableau, etc. If using MS Excel, be sure to use the tools for importing external data, otherwise inconsistencies may occur when viewing the data.

14. Only valid shooting incidents resulting in an injured victim are included in this release. Shooting incidents not resulting in an injured victim are classified according to the appropriate offense according to NYS Penal Law.

-   Note: The previous information is provided from the following website. <https://data.cityofnewyork.us/api/views/833y-fsy8/files/e4e3d86c-348f-4a16-a17f-19480c089429?download=true&filename=NYPD_Shootings_Incident_Level_Data_Footnotes.pdf>

15. Field Names and Descriptions are as follows:

| Column Name             | Description                                                                                                                                                                            | Type        |
|--------------------------|------------------------------|-----------------|
| INCIDENT_KEY            | Randomly generated persistent ID for each arrest                                                                                                                                       | Plain Text  |
| OCCUR_DATE              | Exact date of the shooting incident                                                                                                                                                    | Date & Time |
| OCCUR_TIME              | Exact time of the shooting incident                                                                                                                                                    | Plain Text  |
| BORO                    | Borough where the shooting incident occurred                                                                                                                                           | Plain Text  |
| LOC_OF_OCCUR_DESC       | Description of the location of occurrence                                                                                                                                              | Plain Text  |
| PRECINCT                | Precinct where the shooting incident occurred                                                                                                                                          | Number      |
| JURISDICTION_CODE       | Jurisdiction where the shooting incident occurred. Jurisdiction codes 0(Patrol), 1(Transit), and 2(Housing) represent NYPD<br>whilst codes 3 and more represent non-NYPD jurisdictions | Number      |
| LOC_CLASSFCTN_DESC      | Location classification description                                                                                                                                                    | Plain Text  |
| LOCATION_DESC           | Location of the shooting incident                                                                                                                                                      | Plain Text  |
| STATISTICAL_MURDER_FLAG | Shooting resulted in the victim’s death which would be counted as a murder                                                                                                             | Checkbox    |
| PERP_AGE_GROUP          | Perpetrator’s age within a category                                                                                                                                                    | Plain Text  |
| PERP_SEX                | Perpetrator’s sex description                                                                                                                                                          | Plain Text  |
| PERP_RACE               | Perpetrator’s race description                                                                                                                                                         | Plain Text  |
| VIC_AGE_GROUP           | Victim’s age within a category                                                                                                                                                         | Plain Text  |
| VIC_SEX                 | Victim’s sex description                                                                                                                                                               | Plain Text  |
| VIC_RACE                | Victim’s race description                                                                                                                                                              | Plain Text  |
| X_COORD_CD              | Midblock X-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet<br>(FIPS 3104)                                                                  | Plain Text  |
| Y_COORD_CD              | Midblock Y-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet<br>(FIPS 3104)                                                                  | Plain Text  |
| Latitude                | Latitude coordinate for Global Coordinate System, WGS 1984, decimal degrees<br>(EPSG 4326)                                                                                             | Number      |
| Longitude               | Longitude coordinate for Global Coordinate System, WGS 1984, decimal degrees<br>(EPSG 4326)                                                                                            | Number      |
| Lon_Lat                 | Longitude and Latitude Coordinates for mapping                                                                                                                                         | Point       |

-   Note: The table name, description and data types are provided at the following website. <https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8/about_data>.

### Summary Information by Column

Each of the columns listed below has a large percentage of NA/null values. The main focus of this analysis is to identify causes and suggest improvements in the data collection process to reduce the number of missing values.

Columns are analyzed in this section for NA and null values. The column names are unchanged from the original dataset, but the descriptions are provided in the title section as follows:

-   LOC_CLASSFCTN_DESC: Classification of the location of the incident.
-   LOCATION_DESC: Description of the location of the incident.
-   PERP_AGE_GROUP: Age group of the perpetrator.
-   PERP_SEX: Sex of the perpetrator (M-male/F-female/U-unknown).
-   PERP_RACE: Perpetrator by racial group.
-   VIC_AGE_GROUP: Age group of the victim.
-   VIC_SEX: Sex of the victim (M-male/F-female/U-unknown).
-   VIC_RACE: Victim by racial group.

#### Percentages of NA/Null Values for each column.

The following is a summary of the percentage of NA and null values for each of the columns listed above. By analyzing these percentages, we can identify potential issues with data collection and quality. Most of the missing data is from the perpetrators. A large number of NA and null values also show up in the Location Classification, Location Description, and the Location of Occurrence columns.

### Data Cleaning and Transformation

The following steps outline how the data is cleaned and transformed for analysis.


### Incident Distribution by Precinct

The following table shows the distribution of shooting incidents by precinct.

### Distribution by Perpetrator Age Group, Sex, and Race

This section analyzes the distribution of perpetrators by age group, sex, and race.

### Distribution by Victim Age Group, Sex, and Race

This section analyzes the distribution of victims by age group, sex, and race.

### Contingency Table: Precinct vs. Statistical Murder Flag

This section presents a contingency table showing the relationship between precincts and whether an incident resulted in a murder.

### Chi-Squared Test: Precinct vs. Statistical Murder Flag

The following code performs a chi-squared test to evaluate the relationship between precincts and whether an incident resulted in a murder.

### Seasonality of Shooting Incidents

This section examines the seasonality of shooting incidents by plotting the number of incidents per month.

### Clustering Analysis: NYPD Shooting Clusters

This section performs k-means clustering on the latitude and longitude coordinates of the shooting incidents to identify clusters.

### Temporal Analysis by Year

Analyze trends over multiple years to understand long-term changes in shooting incidents.

### Predictive Modeling with Logistic Regression

Let's add an example of how to set up a logistic regression model to predict whether an incident results in a murder.

### Confusion Matrix

The confusion matrix shows the performance of the classification model by comparing the predicted labels to the actual labels. The rows represent the predicted classes, while the columns represent the actual classes.

### Model Performance Metrics

Additional performance metrics for the logistic regression model, such as ROC-AUC, precision, recall, and F1-score, to provide a more comprehensive evaluation.

### Predicted Probability Graph Explanation

The following graph shows the predicted probability of an incident resulting in a murder based on the logistic regression model. The x-axis represents the predicted probability, while the y-axis shows the number of incidents with that probability.


### Bias Analysis in NYPD Shooting Incident Data Analysis

When analyzing sensitive data such as the NYPD Shooting Incident Data, it's crucial to recognize potential biases that may influence the results and interpretations. Here are several key areas where bias could be present in the provided analysis:

#### Selection Bias

The data only includes shooting incidents that were reported and recorded by the NYPD. Incidents that were not reported or recorded accurately are missing, leading to an incomplete picture. Filtering out categories with exactly one occurrence may remove significant but rare events, introducing bias by focusing only on more frequent incidents.

#### Survivorship Bias

Analysis may disproportionately focus on certain precincts or demographics that have higher reporting rates, thereby neglecting areas or groups with lower reporting rates.

#### Reporting Bias

There could be discrepancies in how different precincts or officers report incidents, which may affect the data consistency. For instance, some precincts might be more diligent or have different criteria for reporting.

#### Measurement Bias

The way data is recorded might introduce errors. For example, inaccuracies in recording the exact location, time, or demographics can lead to skewed results. The "STATISTICAL_MURDER_FLAG" relies on accurate determination of whether a shooting resulted in a murder, which might be influenced by subjective judgment or administrative decisions.

#### Sample Size Bias

Removing rows with NA values might lead to a reduced dataset that does not fully represent the original population, especially if NA values are not randomly distributed.

#### Imbalance in Data

The dataset might have an imbalance in the number of incidents across different categories (e.g., more incidents in certain boroughs or involving certain demographics), which can lead to biased model predictions. The confusion matrix indicates a high imbalance between non-murder and murder cases, which affects the model's ability to accurately predict rare events.

#### Model Bias

Logistic regression and other machine learning models may inherit and amplify existing biases in the data. If the training data is biased, the model predictions will also be biased. The choice of features and how they are encoded (e.g., converting categorical variables to dummy variables) can influence the model's performance and fairness.

### Suggestions to Address Bias

#### Data Augmentation and Cleaning

Insure thorough cleaning and preprocessing of data to minimize errors and inconsistencies. Consider imputation methods for handling NA values rather than simply removing them. Augment the dataset with additional relevant features that might help reduce bias, such as socioeconomic indicators or historical crime rates.

#### Balanced Sampling

Use techniques like oversampling, undersampling, or synthetic data generation (e.g., SMOTE) to address class imbalances in the dataset.

#### Bias Detection and Mitigation

Implement fairness-aware algorithms and bias detection techniques to identify and mitigate biases in the model. Regularly evaluate the model's performance across different demographic groups to ensure fairness and equity.

#### Transparency and Documentation

Clearly document the data sources, preprocessing steps, and any assumptions made during the analysis to enhance transparency and reproducibility. Provide contextual information about potential biases and limitations of the analysis to inform stakeholders and decision-makers.

#### Engage with Stakeholders

Collaborate with community stakeholders, law enforcement, and subject matter experts to validate findings and ensure that the analysis considers diverse perspectives and real-world implications.

### Conclusions from the NYPD Shooting Incident Analysis

The NYPD Shooting Incident Analysis provides valuable insights into the distribution, temporal trends, and demographic patterns of shooting incidents in New York City. While the analysis highlights significant patterns and potential areas of intervention, it also underscores the need for continuous improvement in data quality, model performance, and bias mitigation. By addressing these recommendations, the analysis can provide more accurate, fair, and actionable insights to help reduce shooting incidents and improve public safety in New York City.

### Recommendations

-   Improve Data Quality: Enhance the accuracy and completeness of the data collection process. Addressing missing values through advanced imputation techniques and ensuring consistent reporting across precincts can improve the reliability of the analysis.

-   Enhance Model Performance: Consider using more advanced machine learning models and techniques to improve specificity and overall model performance. Techniques such as ensemble methods or incorporating additional features could help in better distinguishing between non-murder and murder incidents.

-   Address Biases: Implement strategies to detect and mitigate biases in the data and model. Regularly evaluate the model's fairness across different demographic groups and ensure transparency in reporting the analysis.

-   Stakeholder Collaboration: Engage with community stakeholders, law enforcement, and experts to validate findings and incorporate diverse perspectives. Collaborative efforts can lead to more effective and equitable interventions.

-   Regular Updates and Monitoring: Update the analysis regularly to reflect the most recent data and monitor trends over time. This will help in identifying emerging patterns and making timely adjustments to strategies and policies.
