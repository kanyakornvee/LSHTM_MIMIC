# MIMIC-III Data Processing for ICU Length of Stay in Stroke Patient Analysis

This repository provides the SQL queries for preprocessing the MIMIC-III database to extract relevant data for stroke analysis.

The MIMIC-III (Medical Information Mart for Intensive Care III) database is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

## Data Processing

This script is a Python script for a data preprocessing pipeline used on this project. Here's an overview of what it does:

**1. Set Environment**: It loads necessary Python libraries and 
mounts the Google drive where the data is located.

**2. Load Dataset**: It loads the dataset from Google Drive.

**3. Change Columns**: It renames columns, resets indices, and pivots the DataFrame for better readability and usability.

**4. Join with Demographic Data**: It joins different dataframes based on common columns (`subject_id` and `hadm_id`) using a left join operation.

**5. Check Missing Values & Outliers**: It calculates the percentage of missing values, removes data with more than 20% missing values.

**6. Regroup ICD-9**: It categorizes `icd9_code` into groups for better understanding and diagnosis mapping.

**7. Normality Test**: It checks for the normality of numeric data by using the Shapiro-Wilk test.

**8. Data Imputation**: It replaces outliers and missing values with the mean for some columns.

**9. Save Data**: It saves the preprocessed data to a new CSV file on Google Drive. The data is then divided into separate tables based on the `mortality` status.

## Usage

To use these SQL queries, you need to have access to the MIMIC-III database. Please follow the instructions on the official MIMIC-III website (https://physionet.org/content/mimiciii/1.4/) to gain access. After gaining access, you can run these queries in your preferred SQL environment (like PostgreSQL, MySQL, etc.).

Please note that you may need to modify these queries according to your research question and analysis plan.

## Contribution

Contributions to this repository are welcome. If you find any issues or have suggestions, please open an issue or a pull request.

## Disclaimer

The MIMIC-III data should be used responsibly. Please ensure that you have completed the required training and agreed to the data use agreement before using the data. All the information used from the MIMIC-III database is de-identified. Always follow the data use agreement while handling the MIMIC-III data.
