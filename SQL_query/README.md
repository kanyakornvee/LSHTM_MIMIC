# MIMIC-III Data Processing for ICU Length of Stay in Stroke Patient Analysis

This repository provides the SQL queries for preprocessing the MIMIC-III database to extract relevant data for stroke analysis.

The MIMIC-III (Medical Information Mart for Intensive Care III) database is a large, freely-available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012.

## Data Extraction and Preprocessing

The SQL queries perform the following operations:

1. Create a table (`full_criteria`) with specific columns selected from different tables in the MIMIC-III database with necessary filters applied (like age, admission type, ICD-9 code, etc.).

2. Create a table (`first_icu_stay`) that contains information on the first ICU stay of each patient.

3. Create a table (`full_criteria_demographic`) by joining `full_criteria` and `first_icu_stay`. This table also contains additional demographic information, such as gender, ethnicity, insurance status, ICU length of stay, etc.

4. Create a table (`ranked_CBC`) with relevant lab test results (CBC: Complete Blood Count) for the first ICU stay of each patient. This table is then used to create another table (`lab_CBC`) that contains the first test result of each lab test for each patient.

5. Similar to `ranked_CBC` and `lab_CBC`, tables (`ranked_chem` and `lab_chem`) are created to store relevant chemistry lab test results.

6. Create a table (`ranked_clinical`) with relevant clinical item data for the first ICU stay of each patient. This table is then used to create another table (`item_clinical`) that contains the first recorded value of each clinical item for each patient.

## Usage

To use these SQL queries, you need to have access to the MIMIC-III database. Please follow the instructions in the official MIMIC-III website to gain access. After gaining access, you can run these queries in your preferred SQL environment (like PostgreSQL, MySQL, etc.).

Please note that you may need to modify these queries according to your research question and analysis plan.

## Contribution

Contributions to this repository are welcome. If you find any issues or have suggestions, please open an issue or a pull request.

## Disclaimer

The MIMIC-III data should be used responsibly. Please ensure that you have completed the required training and agreed to the data use agreement before using the data. All the information used from the MIMIC-III database is de-identified. Always follow the data use agreement while handling the MIMIC-III data.
