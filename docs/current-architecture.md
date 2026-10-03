# Current Data Architecture

## Purpose

This document records the data platform components and data flow that have been implement and validated

## Implemented Data Flow

Test
Retail Sales CSV File 

Azure data Lake Storage Gen2 - loading

Azure Data factory pipeline 

Azure data lake storage gen2 -bronze

## Source location

text
Landing/copy of retail-supply-chain-sales-dataset_2.csv

--## Bronze location

text
retail_sales/bronze/oracle/orders/load_date=2026-10-02/

Component                    | Responsiblity                        | Status
Azure data lake storage gen2 | store source and bronze -layer files | Implemented
Azure data factory           | Orechestrates Landing to bronzze ingestion | Implemented and validated

azure databricks | transformation data later layer










