Description
This repository contains a series of SQL commands designed to create new data tables for a hypothetical research study using the MIMIC-III (Medical Information Mart for Intensive Care III) database. The research study aims to explore patient admissions due to stroke and examine various demographic, clinical, and laboratory parameters.

Prerequisites
Access to the MIMIC-III database: MIMIC-III (Medical Information Mart for Intensive Care III) is a large, freely available database comprising deidentified health-related data associated with over forty thousand patients who stayed in critical care units of the Beth Israel Deaconess Medical Center between 2001 and 2012. More information about obtaining access to the database can be found here: https://mimic.mit.edu/iii/gettingstarted/.

SQL environment: All commands in this repository are written in SQL, a standard language for managing and manipulating databases. Any SQL environment (e.g., MySQL, PostgreSQL, SQLite, etc.) can be used to execute these commands, provided that the MIMIC-III database has been correctly imported into this environment.

Code Details
The provided SQL code aims to create multiple tables that will streamline data extraction and analysis for the research study. The final output includes demographic information, diagnostic codes, ventilation status, age group, ethnicity, insurance type, ICU length of stay, laboratory test results, and more.

The code includes the following steps:

Create a new table (full_criteria) including patients aged 20-80 admitted for stroke (ICD-9 codes between '430' and '438', excluding '435%'), excluding specific types of stroke and admission types. It also calculates the time from Emergency Room to ICU admission.

Identify the first ICU stay for each patient and store it in a new table (first_icu_stay).

Create a new table (full_criteria_demographic) including demographic data and hospital admission details, as well as information about whether patients had a stroke previously, their insurance type, ventilation status, ICU length of stay, and mortality.

Create tables (ranked_CBC and lab_CBC) including laboratory results for complete blood count (CBC).

Create tables (ranked_chem and lab_chem) including laboratory results for certain chemistry tests.

Create tables (ranked_clinical and item_clinical) including other clinical items.

Usage
To utilize this code, you should run the SQL commands in the same order they appear in the file. This is necessary because later commands may depend on tables created by earlier commands. If you encounter an error, ensure that you have correctly set up your environment and that all the prerequisite steps have been completed.
