# Database

-> optimized for a purpose and come with different features, shapes and constraints

## Relational DB

-> looks just like Excel spreadsheets, with links between them

-> can use the SQL language to perform queries / lookups

## NoSQL DB

-> non relational databases

-> have flexible schemas for building modern applications

# Types of Databases

## Amazon RDS

-> stands for Relational Database Service

-> use SQL as a query language

-> allows you to create databases in the cloud that are managed by AWS

* Postgres
* MySQL
* MariaDB
* Oracle
* Microsoft SQL Server
* IBM DB2
* Aurora (AWS Proprietary database)

-> you can’t SSH into your instances

![rds](..\materials\images\rds.png)

### Amazon Aurora

-> proprietary technology from AWS

-> PostgreSQL and MySQL are both supported as Aurora DB 

-> Aurora is “AWS cloud optimized” and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postgres on RDS

-> Serverless: no capacity planning needed

### RDS Deployment

* Read Replicas:

    * Scale the read workload of your DB
    * Can create up to 15 Read Replicas
    * Data is only written to the main DB

    ![rds_replica](..\materials\images\rds_replica.png)

* Multi-AZ:

    * Failover in case of AZ outage (high availability)
    * Data is only read/written to the main database
    * Can only have 1 other AZ as failover

    ![rds_multi_az](..\materials\images\rds_multi_az.png)

* Multi-Region (Read Replicas):

    * Disaster recovery in case of region issue
    * Local performance for global reads
    * Replication cost

    ![rds_multi_region](..\materials\images\rds_multi_region.png)

## Amazon ElastiCache

-> same way RDS is to get managed Relational Database

-> get managed Redis or Memcached

-> in-memory databases with high performance, low latency

-> reduce load off databases for read intensive workloads

![elasticache](..\materials\images\elasticache.png)

## DynamoDB

-> fully managed highly available with replication across 3 AZ

-> NoSQL database

-> scales to massive workloads, distributed “serverless” database

-> fast and consistent in performance, low latency retrieval

-> integrated with IAM 

### DynamoDB Accelerator - DAX

-> fully managed in-memory cache for DynamoDB

-> 10x performance improvement

-> secure, highly scalable & highly available

-> DAX is only used for and is integrated with DynamoDB, while ElastiCache can be used for other databases

![dynamoDB_dax](..\materials\images\dynamoDB_dax.png)

### Global Tables

-> accessible with low latency in multiple-regions

-> Active-Active replication (read/write to any AWS Region)

![dynamoDB_global](..\materials\images\dynamoDB_global.png)

## Redshift

-> based on PostgreSQL, but it’s not used for OLTP (online transfer processing), int's OLAP (online analytical processing => analytics and data warehousing)

-> load data once every hour, not every second

-> 10x better performance than other data warehouses 

-> SQL interface for performing the queries

-> Massively Parallel Query Execution 

-> Serverless: run analytics workloads without managing data warehouse infrastructure

-> reporting, dashboarding applications, real-time analytics

## Amazon EMR

-> Elastic MapReduce, helps creating Hadoop clusters (Big Data) to analyze and process vast amount of data

-> clusters can be made of hundreds of EC2 instances

-> supports Apache Spark, HBase, Presto, Flink

-> data processing, machine learning, web indexing, big data

## Amazon Athena

-> serverless query service to analyze data stored in Amazon S3

-> uses standard SQL language to query the files

-> supports CSV, JSON, ORC, Avro, and Parque

## Amazon QuickSight

-> serverless machine learning-powered business intelligence service to create interactive dashboards

-> fast, automatically scalable, embeddable, with per-session pricing

## DocumentDB

-> MongoDB (which is a NoSQL database)

-> store, query, and index JSON data

-> fully managed, highly available with replication across 3 AZ

## Amazon Neptune

-> fully managed graph database

-> highly available across 3 AZ, with up to 15 read replicas

-> highly available with replications across multiple AZs

## Amazon Timestream

-> fully managed, fast, scalable, serverless time series database

-> automatically scales up/down to adjust capacity

-> built-in time series analytics functions (helps you identify patterns in your data in near real-time)

## Amazon Managed Blockchain

-> blockchain makes it possible to build applications where multiple parties can execute transactions without the need for a trusted central authority

-> compatible with the frameworks Hyperledger Fabric & Ethereum

## AWS Glue

-> managed extract, transform, and load (ETL) service

-> useful to prepare and transform data for analytics

![glue](..\materials\images\glue.png)

-> can be used by Athena, Redshift, EMR 

-> Glue data catalog is a central repository to store structural and operational metadata for data assets 

## Database Migration Service (DMS)

-> quickly and securely migrate databases to AWS, resilient, self healing

-> the source database remains available during the migration

![dms](..\materials\images\dms.png)