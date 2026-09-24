# jde10_final_project

This is a repository of our final project for Junior Data Engineer course with Generation Singapore (July-Oct 2026).

## Title: NHL Performance Predictor​

### Summary
We are assigned the NHL datasets from Kaggle for the project and the team decided to run to models from the dataset to make predictions on potential winning teams and players.

Using the Azure Fabric pipeline, we create a dataflow based on medallion architecture to ingest bronze tables, transform silver tables and final create the gold tables for consumption. The visualization are done on PowerBI after creating the semantic models.

### Contraints and Limitations

The entire project is done in Microsoft Azure Fabric under Free Account. This means after 30 days, the accounts and workspace are removed. Overtime, MS has made a lot more restrictions on usage on free/trial accounts. There are a number of limitations with personal accounts and free ON accounts such as creation of DevOps workspace and Data Factory. As such, the project is completed based on these constraints.

As such the repository here contains materials or source codes that can help recreate the pipeplines when needed and explain the project

### Tech stack

Platform: Microsoft Azure Fabric
- Fabric Pipeline
- Notebooks
  - PySpark
  - unittest
- ML models (Random Forest (RF) / Gradient Boosted Trees (GBT))
- DataLake tables
- PowerBI

### Pipeline

Due to our limitations, we have decided to put unit testing up front of the ETL. In other scenarios, unit testing is executed whenever changes to functions are made.

Core tables are tables from the input datasets with no additional columns, 
the datasets are cleaned and validated and are used to create additional silver 
used for modelling.

1. Testing
2. Extract (Bronze)
   - Load datasets from kaggle and ingest into bronze tables
3. Transform (Silver)
   - transform and create level 1 core silver tables
   - transform and create level 2 core silver tables
   - transform and create level 3 core silver tables
   - transform and create tables used for modeling based on core silver tables
4. Load (Gold)
   - create gold silvers 
