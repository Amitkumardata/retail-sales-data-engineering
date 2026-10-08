retail_data_platform/
|- README.md
|- docs/
    architecture
    architecture-inventory.md
    data-dontract.md
    scurity-and-access.md
    testing-strategy.md

|--ADF/
    pipeline
    dataset
    linked service
    trigger
Databricks
|- Bronze-to-silver
   silver-to-gold
   -audit table
   -validation

SQL/
|- unity catalog
   audit
gitignore   

## Unity catalog 

catalog: dbw_retail_de_dev
gold schema: dbw_retail_de_dev.gold
current owner: akumar123@gmail.com
explicit gold grants: None
account-level reporting group: pending administrator provisioning
permission model: Least privilage
planned reporting permision: 'USE CATALOG , USE SCHEMA AND SELECT
    
# unity catalog Hierarchy
METASTORE
   └── CATALOG
         └── SCHEMA
               └── TABLE / VIEW / VOLUME

# GRANT PATTERN
grant use catalog
on catalog dbw_retail_de_dev
to 'retail-reporting-readers'

GRANT USE SCHEMA
ON SCHEMA dbw_retail_de_dev.gold
TO `retail-reporting-readers`

GRANT USE SCHEMA
ON SCHEMA dbw_retail_de_dev.gold
TO `retail-reporting-readers`

## Pipeline failure recovery runbook

Job: retail_supply_chain_daily_pipeline

workflow:
bronze_to_silver -> silver_to_gold-> data validation

### check the failed task

open:
jobs & pipeline ->retail_supply_chain_daily_pipeline->Runs

Idenityfy:
Failed task name
Error message
Run start time
retry result

# 2 READ THE ERROR

common error:
source file/path exists
Required columns are present
cluster started correctly 
unity catalog permission are aviable
storage access is available

# Fix the cause
missing input file: correct the path or wait for deliveyr
data schema change: update the transformation mapping
Notebook schema: update the transformation mapping
Temporary compute failure: rerun the failed task

## Recover safely

use **repair run*** or rerun only the failed task after fixing the problem
