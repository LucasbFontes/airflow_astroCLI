# Context

This project was made during the workshop given by [The Plumbers](https://theplumbers.com.br/) and I made it alongside with the instructor. The goal of this project is to perform
an ETL process orchestrated by Apache Airflow. It involves extracting data from the raw layer of minIO, transforming it, and loading it into a curated layer within minIO.
The data will later be served on postgresDB.


# Technologies

## minIO

MinIO is a open source object store that uses S3 protocol and can be used as a Data Lake as well as run on-premise or on any cloud. One of its main characteristics is the High 
Performance being the worlds fastest object storage and also a Kubernets-Native tool. It was chosen to be a part of this project due to its open-source nature and its
ability to emulate an S3 bucket.

## Astro Python SDK

Astro Python SDK is a open source tool and python package to develop DAG, it's maintained by Astronomer(which is also Airflow maintainer), the goal is to remove the complexity of writing
DAGs in Apache Airflow. In this project I use it mainly to move files from different storages and also to clean the data. In comparison to Apache Airflow, Astro Python SDK is easier to
use, given that it uses less Airflow configurations. Hence, it was chosen to be in this project to help orchestrate the pipeline.

## Great Expectations

Great Expectations is a python library focused in data quality and it's used to automate unit tests. It provides several functions to evaluate the data from differents perspectives. This
library can help the engineer by doing the tests during the pipeline execution, and throwing an error when the criteria is not met.

## Postgres

An open-source object-relational database and uses most of the time the SQL standard(except when does not contradict tradicional features), and can be extensible since it's possible to
define the user own data type, build custom functions and write different programmin languages without recompiling the database.

# The project 


<img width="1130" alt="Screen Shot 2023-05-18 at 12 12 00" src="https://github.com/LucasbFontes/airflow_astroCLI/assets/68716835/b6b222d7-4e3b-455a-ad77-3c3a58805990">
