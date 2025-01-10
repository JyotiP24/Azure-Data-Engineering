# Azure-Data-Engineering
# Azure Data Factory Project: Step-by-Step Guide 🚀

## Overview
This repository documents the steps undertaken to create a complete Azure Data Factory project, including the setup of Azure services, pipeline creation, and real-world data scenarios.

---

## Steps Covered in the Project

### 1. Setting Up the Azure Environment
   - Created an Azure Free Account with $200 credits for first-time use.
   - Set up a Resource Group to organize all resources related to the project.
   - Provisioned a Storage Account for data storage:
     - Configured redundancy options like LRS (Locally Redundant Storage).
     - Enabled hierarchical namespace for Azure Data Lake functionality.

### 2. Uploading Data to Azure Data Lake
   - Created Source and Destination Containers in the storage account:
     - Source Container: Holds raw files uploaded for processing.
     - Destination Container: Receives processed files from the pipeline.
   - Uploaded sample files such as `fact_sales1.csv` to the Source Container.

### 3. Creating the Azure Data Factory (ADF)
   - Set up the Azure Data Factory service in the same resource group.
   - Launched the ADF Studio for pipeline creation and management.

### 4. Building the First Pipeline
   - Created a Pipeline in ADF to perform data movement:
     - Used the Copy Data Activity to transfer files from the source container to the destination container.
     - Configured Linked Services to establish connections between ADF and the storage account.
     - Created Datasets to specify the source and destination file locations.

### 5. Enhancing the Pipeline with Real-Time Scenarios
   - Scenario 1: Pulled data directly from an API (e.g., GitHub):
     - Configured an HTTP Linked Service to connect to an external GitHub repository.
     - Created a dataset to fetch the file `fact_sales2.csv` from GitHub.
     - Implemented a pipeline to move the file directly to Azure Data Lake.

   - Scenario 2: Filtered data for reporting:
     - Utilized the Get Metadata Activity to retrieve metadata for all files in a folder.
     - Implemented an **If Condition Activity** to filter files by name (e.g., files starting with `fact`).
     - Transferred filtered files to a new container named `reporting`.

### 6. Configuring Triggers
   - Set up Schedule Triggers to automate pipeline execution at specific intervals.
   - Configured a **Storage Event Trigger** to initiate the pipeline when new files were uploaded to the source container.

---

## Conclusion
This project demonstrates the comprehensive use of Azure Data Factory for data engineering tasks, covering:
- Data movement between Azure Data Lake containers.
- Integration with external APIs.
- Filtering and managing data for specific use cases.
- Automating pipelines with triggers.

