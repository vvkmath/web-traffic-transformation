# web-traffic-transformation
Data processing pipeline to transform web traffic data to aggregate by user_id

## Objective
The primary objective of this project is to aggregate web traffic data across multiple CSV files into a single, consolidated view that highlights user engagement across different pages of a website.
The orignal data files have web traffic data in a time-record format, where each row represents a page view. The transformed data would aggregate data for each user_id where each row represents a different user, with columns indicating the time spent on each webpage (path). 

## Installation
To run this project, we will need Python installed on our machine, along with the pandas and requests libraries. The **requests** library is used to send http requests. 
Use **!pip install pandas requests** in Jupyter notebook

## Usage
The pipeline can be run by cloning and running the Jupyter notebook (Web Traffic Transformation.ipynb) in the repo.

## Pipeline Steps
The aggregation of web traffic data is carried out as below.
•	Step 1: Setup and define base URL and file Names. The base-url can be changed without impacting the running of the pipeline.
•	Step 2: Download and load the (CSV files) data; iterate through list comprehension.
•	Step 3: Pre-process the data; Use dropna() to remove all rows with NULL values from the DataFrame.
•	Step 4: Transform and aggregate the data by user_id and the length of time spent by each user on each path. Pivot the table to have user_id as rows and paths as columns.
•	Step 5: Export data as csv
•	Step 6: Chart the distribution of the average time spent on each path

