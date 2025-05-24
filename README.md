# Azure Data Factory and Databricks Project

This project addresses the problem of organizing and transforming uneven files of various formats stored in Azure Data Lake Storage Gen2. The solution includes creating a pipeline in Azure Data Factory (ADF) for file organization and using Databricks to process and store the data in Delta tables.

## Problem Statement
The Azure Data Lake Storage Gen2 contained multiple folders with files of varying formats, including:
- CSV
- Excel
- Parquet

The challenge was to:
1. Organize files into specific folders based on their extensions.
2. Process the data to create Bronze-level and Silver-level Delta tables.
3. Store the processed Delta tables in designated locations within Azure Data Lake Storage Gen2.

## Solution Overview
The solution was implemented using a combination of Azure Data Factory and Databricks:

### Azure Data Factory (ADF)
- **Pipeline Creation**: A pipeline was built in ADF to:
  - Identify and extract files from multiple folders.
  - Sort and move files into specific folders based on their file extensions (e.g., CSV files to a `csv` folder, Excel files to an `excel` folder, etc.).

### Databricks
- **Data Transformation**: A Databricks notebook was programmed to:
  - Read files from the organized folders.
  - Convert the data into Delta tables:
    - **Bronze Level**: Raw data was ingested and stored as-is in Delta format.
    - **Silver Level**: Data was cleaned and transformed for better usability and stored in Delta format.
  - Save the Delta tables in designated locations within Azure Data Lake Storage Gen2.

## Technologies Used
- **Cloud Storage**: Azure Data Lake Storage Gen2
- **Pipeline Orchestration**: Azure Data Factory (ADF)
- **Data Processing**: Databricks (Apache Spark)
- **Delta Lake**: For efficient storage and querying

## Steps to Reproduce
1. **Set Up Azure Data Lake Storage Gen2**:
   - Create folders for input and output.
2. **Build ADF Pipeline**:
   - Configure activities to extract and move files based on their extensions.
3. **Develop Databricks Notebook**:
   - Write code to read files, create Bronze and Silver Delta tables, and store results.
4. **Integrate ADF with Databricks**:
   - Trigger the Databricks notebook from the ADF pipeline.

## Outcomes
- Successfully organized files into designated folders based on their formats.
- Transformed and stored data in Delta tables at both Bronze and Silver levels.
- Achieved a systematic workflow for file organization and data processing.

## Contact
For questions or collaboration opportunities, feel free to reach out:
- **Email**: [siddhisudrania9001@gmail.com](mailto:siddhisudrania9001@gmail.com)
- **GitHub**: [siddhi-sudrania](https://github.com/siddhi-sudrania)

---

This project demonstrates expertise in cloud-based data orchestration and transformation using Azure services and Databricks. Feel free to adapt or extend this solution for similar use cases.
