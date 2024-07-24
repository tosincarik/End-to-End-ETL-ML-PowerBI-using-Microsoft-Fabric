## Company 'X' Sportwears Product Performance and Analysis

---
## Introduction
This is a Power BI Report on product sales performance for company 'X'. The project is to analyse and drive insights to answer crucial business questions and help make the store make data-driven decisions

**_Disclaimer: All datasets and reports  do not represent any company or institution but just a dummy dataset to demonstrate the capablities of Power BI_**

## Problem Statement
1. What is the sales performance of current year
2. Comparison of sales with previous year
3. Yearly Percentile change on profit
4. Best performimng product category, sub-category
5. Demographic performance
---
## Skills Demonstrated
Some of the power BI skills demonstrated are;



## End to End ETL Solution in Fabric

Hi there,  welcome to my page . I am so glad you stumbled on this article today.

I will be exploring and taking a depper dive into building a text sentiment analysis using public data from the internet using an end to end solution in Microsoft Fabric.

Some of the skills to be learnt covers Microsoft fabric data store type (lakhouse in particular), Spark , MLops , Power BI, Azure Data Factory, Notebooks & Pipeline all incorporated in this piece.

# Scope of the project:

The environment is setup by creating the workspace with the right permissions granted.For the purpose of this project, we will be using a trial iicense of Fabric which has access to the F64 capcity, this guarantees enough computing resource for the workload.

The project looks to anlayse data from bing by connecting to the live data through API source . We will set up connection to BING REST API by using the copy activity feature of Microsoft Fabric. Using the copy activity is a fast way of loading data with the highest thoroughput as it does not require transformation.

After loading the data to our data store (lakehouse), using the copy activity in ADF(azure data factory), the data which is collected and stored as a json format is cleaned, transformed and saved as dataframe table and then to a delta table format in the same lakhouse using a notebook environment.

After storing the clean data, the data is imported into another notebook for machine learning sentiment analysis.Here the data is trained on the ML model included in synapse.

The trained data tells us the sentimnent of the news on either negative or positive and a report is developed.

All the series of processes are connected serially in pipeline to run concurrently and schedueld for a daily data refresh with only incremental load of Slowly changing dimension 1


# Step 1: Setting up the environment in Fabric
Create a new workspace named "LH Bronze" which is lake


