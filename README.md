# Truck-delay-prediction-project

Project Description:

The project addresses a critical challenge faced by the logistics industry. Delayed truck shipments not only result in increased operational costs but also impact customer satisfaction. Timely delivery of goods is essential to meet customer expectations and maintain the competitiveness of logistics companies.
By accurately predicting truck delays, logistics companies can:
•	Improve operational efficiency by allocating resources more effectively
•	Enhance customer satisfaction by providing more reliable delivery schedules
•	Optimize route planning to reduce delays caused by traffic or adverse weather conditions
•	Reduce costs associated with delayed shipments, such as penalties or compensation to customers

We will utilize PostgreSQL and MySQL in AWS RDS to store the data, set up an AWS Sagemaker Notebook, perform data retrieval,  conduct exploratory data analysis, create feature groups with Hopsworks, data processing, and feature engineering. We aim to build a pipeline that prepares the data for model building.

Note:  AWS Usage Charges:

This project leverages the AWS cloud platform to build the end-to-end machine learning pipeline. While using AWS services, it's important to note that certain activities may incur charges. We recommend exploring the AWS Free Tier, which provides limited access to a wide range of AWS services for 12 months. Please refer to the AWS Free Tier page for detailed information, including eligible services and usage limitations.

The primary objective of this project is to create an end-to-end machine learning pipeline for truck delay classification. This pipeline will encompass data fetching, creating a feature store, data preprocessing, and feature engineering.

 
Project Breakdown:

•	Database Setup and Data Analysis: We explore driver data, truck data, traffic weather analysis, and route data.

•	Data Retrieval and Python Analysis: We set up AWS SageMaker, fetch data in Python, and analyze driver, truck, traffic, weather, and route data using Python.
 
•	Data Preprocessing and Feature Engineering is done for insights into the Hopsworks, creating feature groups, data preprocessing, and feature engineering.
 
•	Final Steps: They cover final data merging, storing features.
