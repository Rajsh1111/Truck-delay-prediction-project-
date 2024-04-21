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

Data Description:
The project involves the following data tables:
 
•	City Weather: Weather data for various cities
•	Routes: Information about truck routes, including origin, destination, distance, and travel time
•	Drivers: Details about truck drivers, including names and experience
•	Routes Weather: Weather conditions specific to each route
•	Trucks: Information about the trucks used in logistics operations
•	Traffic: Traffic-related data
•	Truck Schedule: Schedules and timing information for trucks



Tech Stack:
•	Language: Python, SQL
•	Libraries:  NumPy, Pandas, PyMySQL , Psycopg2, Matplotlib, Seaborn
•	Data Storage: PostgreSQL,MySQL, AWS RDS, Hopsworks
•	Data Visual Tool(SQL): MySQL Workbench, Pgadmin4
•	Feature Store: Hopsworks
•	Cloud Platform: AWS Sagemaker


•	Database Setup:
o	Creating AWS RDS instances for MySQL and PostgreSQL
o	Setting up MySQL Workbench and pgAdmin4 for database management

•	Data Analysis:
o	Performing data analysis using SQL on MySQL Workbench and pgAdmin4

•	AWS SageMaker Setup:

•	Exploratory Data Analysis (EDA):
o	Conducting exploratory data analysis to understand essential features and the dataset's characteristics

•	Feature Store:
o	Understanding the concept of a feature store and its significance in machine learning projects
o	Understanding how Hopsworks works to facilitate project creation and feature group management

•	Data Retrieval from Feature Stores
 
•	Fetching data from feature stores for further analysis

•	Data Preprocessing and Feature Engineering

•	Data Storage:
o	Storing the final engineered features in the feature store for easy access and consistency

