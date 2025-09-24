# Ingest-data-from-blob-to-ADLS-gen2-updated-by-third-party-vendors-regularly-
Here we are Ingesting the data from Source(Blob Storage) updated by third party vendors regularly, transferring and loading the data to Sink(ADLS GEN2).Products.csv will be updated by third party vendors regularly. Currently in the blob storage and we need to bring the products dataset to Datalake.
Steps to follow-
1) Create a dashboard
2) Create a resource and a resource group
3) Create a Blob Storage account
4) Create an ADLS Gen2 account and enable the Hierarchical Namespace
5) For both storage accounts, go to Settings → Configurations and enable “Allow blob anonymous access.”
6) In Blob Storage, create a container named retail-raw → upload products.csv
(While debugging the pipeline, create a container in ADLS named retail-datasets → inside it, create a directory called raw).
7) Create Azure Data Factory
8) Create Linked Services for both Blob Storage and ADLS Gen2
9) Create Datasets for both sources
10) Build the Pipeline:
a) Add the Validation activity first
b) Add Get Metadata activity
c) Use an If Condition activity to check and proceed to Copy Data (if true)
11) Publish all changes and then Debug the pipeline
