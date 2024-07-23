End to End ETL Solutionand Machine Learning in Fabric

Hi, there , welcome to my page . I am so glad you stumbled on this article today.

I will be exploring and taking a depper dive into building a text sentiment analysis using public data from the internet.

Some of the skills to be learnt covers microsoft fabric data store (lakhouse in particular), pyspark , MLops , Power BI, Azure Data Factory, Notebooks, Pipeline all incorporated in this piece.

Scope of the project:

The environment is setup by creating the workspace with the right permissions granted.For the purpose of this project, we will be using a trial iicense of Fabric which has access to the F64 capcity, this guaranteed enough computing resource for the workload.

The project looks to anlayse data from bing by connecting to the live data with an API source . We will set up connection to bing REST API by using the copy activity feature of Microsoft Fabric. Using the copy activity is a fast way of loading data with the highest thoroughput as it does not require transformation.

After loading the data to our data store (lakehouse), usingthe copy activity in ADF(azure data factory), the data which is collected and stored as a json format is cleaned, transformed and saved as dataframe table and then to a delta table format in the same lakhouse using a notebook environment.
After storing the cleaned data, the data is passed into another notebook for machine learning sentiment analysis.Here the data is trained on the ML model included in synapse.

The trained data tells us the sentimnent of the news on either negative or positive and a report is developed.

All the series of processes are connected serially in pipeline to run concurrently and schedueld for a daily data refresh with only incremental load of Slowly changing dimension 1


Step 1: Setting up the environment in Fabric
Loading data into the lakehouse using copy activity


