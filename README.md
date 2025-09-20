# Ingest-data-from-blob-to-ADLS-gen2-updated-by-third-party-vendors-regularly-
Here we are Ingesting the data from Source(Blob Storage) updated by third party vendors regularly, transferring and loading the data to Sink(ADLS GEN2).Products.csv will be updated by third party vendors regularly. Currently in the blob storage and we need to bring the products dataset to Datalake.
Steps to follow-
1) Create dashboard 
2) Create resource and resource group
3) create blob storage acc
4) Create ADLS Gen 2 acc --- Enable hierarchical namespace
5) After creating both storage accounts - Select individual storage acc-> settings-> configurations->enable "allow blob anonymous access" for both storage accounts.
6) create container in blob - "retail raw"-> upload "products.csv" (when you run the pipeline while debuging.
create container in ADLS -> "retail datasets"-> create directory "raw"
7) create Data factories
8)Create linked service for blob and ADLS
9) Create datasets for both
10) Create pipeline
11) "validation" added first
12) "get metadata"
13) if condition - copy data (true)
14) publish all and then debug 
