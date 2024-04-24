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

 Approach:
 Data Retrieval from Hopsworks:
    * Connecting Hopsworks with Python.
    * Retrieving data directly from the feature store.


* Train-Validation-Test Split

* One-Hot Encoding

* Scaling Numerical Features

* Model Experimentation and Tracking:
    * Weights and Biases Introduction
    * Setting up a new project and connecting it to Python


* Model Building
    * Logistic Regression
    * Random Forest
    * XGBoost


* Hyperparameter Tuning with Sweeps


* Streamlit Application Development and Fetching the Best Model


* Deployment on AWS EC2 Instance

## Data Relationship Structure
```
├─ Data
│  ├─ Database_backup
│  │  ├─ truck-eta-mysql.sql
│  │  └─ truck-eta-postgres.sql
│  ├─ data_description.pdf
│  └─ Training_data
│     ├─ city_weather.csv
│     ├─ drivers_table.csv
│     ├─ routes_table.csv
│     ├─ routes_weather.csv
│     ├─ traffic_table.csv
│     ├─ trucks_table.csv
│     └─ truck_schedule_table.csv
├─ Deployment
│  ├─ app.py
│  ├─ app_config.yaml
│  ├─ requirements.txt
│  ├─ truck_data_encoder.pkl
│  └─ truck_data_scaler.pkl
├─ Notebooks
│  ├─ Truck-Delay-Classification_Part_2.ipynb
│  └─ Truck_Delay_Classification_Part_1.ipynb
```


# Execution Instructions

# Python version 3.10

To create a virtual environment and install requirements in Python 3.10 on different operating systems, follow the instructions below:

### For Windows:

Open the Command Prompt by pressing Win + R, typing "cmd", and pressing Enter.

Change the directory to the desired location for your project:


`cd C:\path\to\project`

Create a new virtual environment using the venv module:


`python -m venv myenv`

Activate the virtual environment:

`myenv\Scripts\activate`


Install the project requirements using pip:

`pip install -r requirements.txt`

### For Linux/Mac:
Open a terminal.

Change the directory to the desired location for your project:

`cd /path/to/project`

Create a new virtual environment using the venv module:

`python3.10 -m venv myenv`


Activate the virtual environment:

`source myenv/bin/activate`

Install the project requirements using pip:

`pip install -r requirements.txt`

These instructions assume you have Python 3.10 installed and added to your system's PATH variable.

## Execution Instructions if Multiple Python Versions Installed

If you have multiple Python versions installed on your system, you can use the Python Launcher to create a virtual environment with Python 3.10. Specify the version using the -p or --python flag. Follow the instructions below:

For Windows:
Open the Command Prompt by pressing Win + R, typing "cmd", and pressing Enter.

Change the directory to the desired location for your project:

`cd C:\path\to\project`

Create a new virtual environment using the Python Launcher:

`py -3.10 -m venv myenv`

Note: Replace myenv with your desired virtual environment name.

Activate the virtual environment:

`
myenv\Scripts\activate
`

Install the project requirements using pip:

`pip install -r requirements.txt`


### For Linux/Mac:
Open a terminal.

Change the directory to the desired location for your project:

`cd /path/to/project
`
Create a new virtual environment using the Python Launcher:


`python3.10 -m venv myenv`


Note: Replace myenv with your desired virtual environment name.

Activate the virtual environment:

`source myenv/bin/activate`

Install the project requirements using pip:

`pip install -r requirements.txt`


By specifying the version using py -3.10 or python3.10, you can ensure that the virtual environment is created using Python 3.10 specifically, even if you have other Python versions installed.



## Run streamlit application

`streamlit run app.py`



# Streamlit Application Deployment on AWS EC2

## Overview

This guide provides step-by-step instructions for deploying a Streamlit application on an AWS EC2 instance. 

## Prerequisites

- AWS Account
- Basic knowledge of AWS EC2, SSH, and Streamlit


## Deployment Steps

### 1. Launching EC2 Instance

- Launch an EC2 instance on AWS with the following specifications:
  - Ubuntu 22.04 LTS
  - Instance Type: t2.medium (or your preferred type)
  - Security Group: Allow inbound traffic on port 8501 for Streamlit

- Create and download a PEM key for SSH access to the EC2 instance.

- Disable Inheritance and Restrict Access on PEM key For Windows Users:
    - Locate the downloaded PEM key file (e.g., your-key.pem) using File Explorer.

    - Right-click on the PEM key file and select "Properties."

    - In the "Properties" window, go to the "Security" tab.

    - Click on the "Advanced" button.

    - In the "Advanced Security Settings" window, you'll see an "Inheritance" section. Click on the "Disable inheritance" button.

    - A dialog box will appear; choose the option "Remove all inherited permissions from this object" and click "Convert inherited permissions into explicit permissions on this object."

    - Once inheritance is disabled, you will see a list of users/groups with permissions. Remove permissions for all users except for the user account you are using (typically an administrator account).

    - Click "Apply" and then "OK" to save the changes.


### 2. Accessing EC2 Instance

1. Use the following SSH command to connect to your EC2 instance:
  ```
  ssh -i "your-key.pem" ubuntu@your-ec2-instance-public-ip
  ```

2. Gain superuser access by running: `sudo su`

3. Updating and Verifying Python
  - Update the EC2 instance with the latest packages:
    `apt update`

  - Verify Python installation:
    `python3 --version`

4. Installing Python Packages
`apt install python3-pip`

5. Transferring Files to EC2
    Use SCP to transfer your Streamlit application code to the EC2 instance:

    ```scp -i "your-key.pem" -r path/to/your/app ubuntu@your-ec2-instance-public-ip:/path/to/remote/location```

6. Setting Up Streamlit Application
    Change the working directory to the deployment files location:

    `cd /path/to/remote/location`

    Install dependencies from your requirements file:

    `pip3 install -r requirements.txt`

7. Running the Streamlit Application
    Test your Streamlit application (Use external link):
    `streamlit run app.py`


    For a permanent run, use nohup:
    `nohup streamlit run app.py`

8. Cleanup and Termination
To terminate the nohup process:
  - `sudo su`
  - `ps -df`
  - `kill {process id}`




