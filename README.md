### Data Preprocessing Tool

In order to use the Data Preprocessing Tool, follow these steps:

1. Unzip the 'Tool' file on your personal computer
2. Find 'main.exe' in the 'main' folder and run it
3. The program pops up in a few second


-----------------------------
### Data Preprocessing Tool Help Document (Updated: 28 May 2024)


Table of Contents:

1. Introduction
|_______1.1 Overview
|_______1.2 Key Features

2. Getting Started
|_______2.1 Installation
|_______2.2 System Requirements

3. Using the Data Imputer
|_______3.1 STEP 1: Loading Data
|_______3.2 STEP 2: Choosing the Date-Time and Main Variable Columns
|_______3.3 STEP 3: Choosing the Daily, Weekly, and Yearly Periodicities
|_______3.4 STEP 4: Choosing the Number of Nearest Neighbors
|_______3.5 STEP 5: Running the Imputation
|_______3.6 STEP 6: Saving the Results

4. Troubleshooting
|_______4.1 Common Issues
|_______4.2 Error Messages

5. FAQs
|_______5.1 What is the K-Nearest Neighbor algorithm?
|_______5.2 What are daily, weekly, and yearly periodicities in time-series?
|_______5.3 What are the impacts of daily, weekly, and yearly periodicities on data imputation?
|_______5.4 How to interpret the imputed data?

6. Contact and Support
|_______6.1 Technical Support
|_______6.2 Feedback and Suggestions
|_______6.3 Contact Info




----------------------------------------------------------------------------------------------------------------------------------------------------------------------

1. Introduction


1.1 Overview

Welcome to the Data Preprocessing Tool, a powerful tool designed to: 
- Fill in missing data points in time series using the k-Nearest Neighbor algorithm. Whether you're dealing with incomplete datasets or want to enhance the accuracy of your time series data, this application provides an efficient and user-friendly solution.


1.2 Key Features

* Efficient Imputation: The application employs the k-Nearest Neighbor algorithm to intelligently impute missing data points, ensuring accuracy and reliability.
* User-Friendly Interface: Intuitive controls and a step-by-step process make it easy for users to load data, configure settings, and obtain imputed results.
* Flexibility: The application allows users to customize the imputation parameters, including choosing the value of k and selecting various periodicities in the data.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. Getting Started


2.1 Installation

This application is portable and you do not need to install it.


2.2 System Requirements

This application can work with any computer system with the Microsoft Windows 10 or later as the operation system.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. Using the Data Imputer


3.1 STEP 1: Loading Data

Utilize the application to import your time-series data, ensuring it is in CSV format. Employ the "Browse" button to locate and select your file on the computer system. The File Status indicator will promptly inform you whether a readable file with the correct format has been chosen. In the event of a successful selection, the indicator will display "File Uploaded!" Otherwise, it will indicate "Wrong File Type!" It is essential that your dataset contains, at a minimum, a column formatted with date and time and a column designated for the main variable. Users also have the option to integrate additional columns for other variables into the dataset, enhancing the imputation process according to their preferences. If other variables are present in the dataset, the algorithm will automatically consider their effects in the imputation procedure. Ensure all columns in the dataset have headers containing the variable names. The dataset must be clean, devoid of anomalies, at the time of uploading to maintain the quality of imputation. Additionally, the date-time column should not contain any missing values.


3.2 STEP 2: Choosing the Date-Time and Main Variable Columns 

Use the drop-down list of column names to select the date-time column and the main variable. In case of wrong selection of the date-time column, the imputation cannot be run and no result is presented.


3.3 STEP 3: Choosing the Daily, Weekly, and Yearly Periodicities

Daily, weekly, and yearly periodicities in time series data refer to the inherent patterns or cycles that occur at daily, weekly, and yearly intervals, respectively. Understanding these periodicities is essential in time series analysis as they often influence the overall trend and seasonality of the data. In this application, daily and yearly periodicities are discerned by extracting sine and cosine waves corresponding to the date-time values in the dataset. Additionally, weekly periodicity is considered through the incorporation of weekday numbers. Users have the flexibility to selectively incorporate the impact of specific periodicities into the imputation process, with all periodicities being selected by default. For additional information on these periodicities, please consult the FAQ section within this document.


3.4 STEP 4: Choosing the Number of Nearest Neighbors

Use the slider to choose the number of nearest neighbors (K). The default value is 5. In the K-NN imputer, 'K' represents the number of nearest neighbors considered during the imputation process. This parameter is pivotal as it directly influences the imputation accuracy and the algorithm's sensitivity to local variations in the dataset. A smaller 'K' value may result in imputed values that closely align with the nearest neighbors but could be more susceptible to noise. Conversely, a larger 'K' value captures a broader neighborhood, potentially smoothing out local patterns but offering robustness against noise. The choice of 'K' is a trade-off between precision and generalization, and it's crucial for users to carefully select a value based on the characteristics of their data, striking a balance that aligns with the underlying patterns and noise levels in the time series.


3.5 STEP 5: Running the Imputation

Initiate the imputation process by clicking the "RUN" button. Upon successful completion, the application displays a line plot showing both the original and imputed data (main variable), accompanied by key information such as the count of missing data points and the corresponding missing ratio in the result section (right column). For a detailed examination of the imputation, users can use the Zoomed View section (lower part of the right column). This section enables the selection of different start and end dates, with the zoomed plot updating seamlessly via the "UPDATE" button. By default, the application plots the initial 500 data points after executing the imputation process using the "RUN" button.


3.6 STEP 6: Saving the Results
 
Once you've arrived at the optimal parameter selection and are satisfied with the imputed values, use the "Browse" button to designate the location for saving the imputation results on your computer system. Subsequently, click the "SAVE" button to save the results. This action stores the primary line plot covering the entire duration of the time-series, along with a CSV file mirroring the original file's column configuration. In this new CSV file, the imputed values seamlessly replace the missing values for the main variable. Both these files are saved in the directory of your choice.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4. Troubleshooting


4.1 Common Issues

Refer to this section for guidance on resolving common issues encountered during the imputation process.


4.2 Error Messages

* Wrong File Type!: This error message will appear next to the "File Status" indicator if a readable CSV file is not selected by the user.
* Wrong Dates!: This error message will appear next to the "UPDATE" button if the selected dates for the zoomed plot fall outside the range of the dataset or if the "From" date is not earlier than the "To" date. 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

5. FAQs


5.1 What is the K-Nearest Neighbor algorithm?

The k-Nearest Neighbor (K-NN) algorithm is a machine learning technique used for classification and regression tasks. In essence, it operates on the principle that objects in a dataset are more likely to share similar characteristics if they are in close proximity to each other. For a given data point, the algorithm identifies its K-nearest neighbors based on a chosen distance metric, commonly Euclidean distance. In a regression context, the algorithm computes the average of the target values of its neighbors. The k-Nearest Neighbor (K-NN) algorithm calculates distances between data points to identify the K-nearest neighbors of a given query point. Typically employing Euclidean distance, the algorithm measures the geometric distance between the features of the query point and those of all other points in the dataset. The K-nearest neighbors are then determined based on the smallest distances. The choice of K, the number of neighbors considered, is a crucial parameter that influences the algorithm's sensitivity to local variations in the data. The flexibility and simplicity of the K-NN algorithm make it particularly useful for imputation tasks, where it excels at capturing local patterns in data.


5.2 What are daily, weekly, and yearly periodicities in time-series?

* Daily periodicity implies recurring patterns within a 24-hour cycle. For instance, data might exhibit different behaviors during daytime and nighttime. The K-NN imputer can consider these patterns when imputing missing values, taking into account the similarities between data points based on their temporal proximity.

* Weekly periodicity involves patterns that repeat on a weekly basis. For example, certain trends or behaviors may be more prevalent on specific days of the week. The K-NN imputer can consider the weekly patterns when estimating missing values, capturing the cyclic nature of the data.

* Yearly periodicity encompasses trends or cycles that repeat annually. This could include seasonal variations or events tied to specific times of the year. The K-NN imputer can incorporate the yearly patterns when imputing missing values, recognizing the cyclical nature of the data across different years.


5.3 What are the impacts of daily, weekly, and yearly periodicities on data imputation?

* Accuracy: Understanding periodicities is crucial for accurate imputation. The K-NN imputer uses the temporal relationships between data points, and considering periodic patterns enhances its ability to impute missing values more accurately.

* Parameter Tuning: Depending on the periodicity of the data, users might need to adjust parameters such as the number of neighbors (K) in the K-NN algorithm. Periodic data may require a different choice of K to effectively capture local patterns.

* Temporal Proximity: Daily, weekly, and yearly periodicities influence the definition of proximity in the imputation process. The imputer prioritizes neighbors that are temporally close, taking into account the specific periodic patterns associated with the data.


5.4 How to interpret the imputed data?

Interpreting imputed data from the K-NN imputation process involves understanding how missing values have been filled in and making informed decisions based on the results. Here's a guide on how to interpret and utilize imputed data from K-NN imputation:

* Review Imputed Values: Examine the imputed values to ensure they align with the expected patterns in your dataset. Check whether imputed values make sense in the context of the surrounding data.

* Assess Impact on Analysis: Evaluate the impact of imputed data on subsequent analyses or models. Consider running analyses with and without imputed data to understand variations in results.

* Consider Imputation Uncertainty: Acknowledge that imputed values come with a level of uncertainty, especially if the nearest neighbors have considerable variability. Explore methods to quantify and represent uncertainty in imputed values.

* Visualize Data: Visualize the original data and imputed data to observe trends and variations.

* Compare Against Original Data: Compare imputed data against the original data to identify areas where imputation might have introduced biases or anomalies. Use statistical measures such as mean squared error or correlation coefficients for a quantitative comparison.

* Sensitivity Analysis: Conduct sensitivity analyses by varying parameters, such as the number of neighbors (K), to understand how changes influence imputed results.

* Domain Knowledge Integration: Incorporate domain knowledge to validate imputed values. If certain values seem improbable or inconsistent, consider revisiting the imputation approach or seeking expert input.

* Documentation and Communication: Clearly document the imputation process, including parameters used and any assumptions made. Communicate the potential uncertainties and limitations associated with imputed data to stakeholders.

* Iterative Refinement: If the initial imputation results lead to unexpected outcomes, consider iteratively refining the imputation process based on feedback and additional insights.

By carefully considering these steps, you can ensure that the imputed data is used effectively in your analyses and decision-making processes, while being mindful of the inherent uncertainties associated with the imputation method.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

6. Contact and Support


6.1 Technical Support

For technical assistance, contact our support team at [info@hilat.ca].


6.2 Feedback and Suggestions

We value your feedback. Share your thoughts and suggestions to help us improve the Data Imputer Application for future releases.


6.3 Contact Info

High Latitude Energy Consulting
Address: 201-114 Titanium Way, Whitehorse, YT, Y1A 0E8
Website: https://www.hilat.ca/




Copyright 2023 High Latitude All Rights Reserved.