# Layoffs 2022 Data Cleaning and EDA Project

This project focuses on cleaning and performing Exploratory Data Analysis (EDA) on the "Layoffs 2022" dataset from Kaggle (https://www.kaggle.com/datasets/swaptr/layoffs-2022). The dataset contains information about company layoffs, including company details, industry, location, date, and number of employees laid off.

## Project Structure

-   **README.md**: This file, providing an overview of the project.
-   **layoffs_cleaning_eda.sql**: The SQL script containing the data cleaning and EDA queries.

## Data Cleaning Process

The data cleaning process involved the following steps:

1.  **Creating a Staging Table**: A staging table was created as a copy of the original table to preserve the raw data.
2.  **Removing Duplicates**: Duplicate rows were identified and removed using `ROW_NUMBER()` and `PARTITION BY` clauses.
3.  **Standardizing Data**:
    -      Industry names were standardized (e.g., consolidating variations of "Crypto").
    -      Country names were standardized (e.g., removing trailing periods from "United States.").
    -      Date format were converted to date type.
    -   Null and empty values for industry were populated when possible.
4.  **Handling Null Values**: Null values were assessed, and decisions were made on whether to retain or modify them.
5.  **Removing Unnecessary Columns and Rows**: Redundant or unusable data was removed.

## Exploratory Data Analysis (EDA)

The EDA focused on identifying trends and patterns in the cleaned data, including:

-      Identifying companies with the largest single layoffs and total layoffs.
-      Analyzing layoffs by location, country, year, and industry.
-      Examining the distribution of layoffs over time.
-   Calculating rolling totals of layoffs per month.

## Key Findings (Examples)

-   Companies with the most significant layoffs were identified.
-   Geographical concentrations of layoffs were determined.
-   The industries most affected by layoffs were analyzed.
-   Temporal trends in layoffs were observed.
-   Startups with 100% layoff rates were examined, including those with substantial funding.
