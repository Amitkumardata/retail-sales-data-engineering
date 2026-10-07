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
    
