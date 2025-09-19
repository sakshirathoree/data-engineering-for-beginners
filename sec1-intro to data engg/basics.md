## data engg covers many topics

- ETL
- Storage
- Data Modeling
- Data pipeline architectures

### SEC1

In section one, we start with the most basic question what exactly is data engineering?

Here's where we introduce you to one of the core ideas in data engineering the **data pipeline**.

This forms the foundation for everything we'll be talking about in this course.

It covers all parts of data engineering from **generation to ingestion, storage, transformation, and
finally serving.**

### SEC2



## 🛠️ Data Pipeline – Key Stages with AWS Examples

### 1. **Generation (Source Systems)**

Where data is generated.

* **Application databases** → Amazon RDS (Postgres, MySQL, Oracle), DynamoDB
* **Logs / events** → CloudWatch, CloudTrail, Application Logs
* **Third-party apps** → Stripe, Salesforce (via APIs / connectors)

---

### 2. **Storage**

Where raw/processed data is stored.
##### Types of storage systems:

* **File storage** → EFS, local FS (rare for data eng).
* **Object storage** → **Amazon S3** (most common data lake).


* **Row-based storage** → RDS (transactional systems).
* **Columnar storage** → Redshift, Parquet/ORC files in S3.


* **Data Warehouse** → **Amazon Redshift**, **Snowflake**.
* **Data Lakehouse** → **Databricks on AWS**, **Athena + Lake Formation on S3**.

- Right type of storage can have a performance difference of up to 100x!


⚡ Columnar + warehouse/lakehouse storage = huge performance boost (up to 100x).

---

### 3. **Ingestion**

- Batch vs streaming ingestion
- ETL vs ELT
- diff ways to ingest data from diff source systems.

Moving data from source → storage.

* **Batch ingestion**:

  * AWS Glue jobs
  * AWS Data Pipeline (older)
  * DMS (Database Migration Service)
* **Streaming ingestion**:

  * **Amazon Kinesis Data Streams / Firehose**
  * **MSK (Managed Kafka)**
* **ETL vs ELT**:

  * ETL → Glue (transform before storing in Redshift).
  * ELT → Load raw to S3/Redshift/Snowflake, then transform inside warehouse using SQL/dbt.

---

### 4. **Transformation**

Making data clean & analytics-ready.

- sql queries
- data modeling
- normalization

* **AWS Glue** (Spark-based transformations).
* **Athena** (SQL queries directly on S3).
* **Redshift / Snowflake SQL** (in-warehouse transformations).
* **dbt** (modern SQL-based transformation framework).
* **Normalization / Data Modeling** → Star schema, Snowflake schema.

---

### 5. **Serving**

Delivering data to users or apps.

- data analytics
- data scientists
- reverese ETL

* **BI tools**: Amazon QuickSight, Tableau, PowerBI.
* **Data scientists**: SageMaker (ML pipelines).
* **External apps (Reverse ETL)**:

  * Tools like Fivetran / Airbyte push warehouse data → Salesforce, HubSpot.
  * Can also use custom Lambda/API integrations.

---

✅ **Quick Flow with AWS services:**

* **Generation** → RDS, DynamoDB, Logs, APIs
* **Storage** → S3 (lake), Redshift/Snowflake (warehouse)
* **Ingestion** → Glue, Kinesis, DMS
* **Transformation** → Glue, dbt, Athena, Redshift
* **Serving** → QuickSight, SageMaker, Reverse ETL apps

---

### SEC3 shared components that underlie our data pipeline

shared components:
- DataOps
- Orchestration
- Security
- data Quality
- Data privacy

### SEC4 actual eg of data architectures for diff use cases.

Egs of data architectures:
- Business Analytics use case
- Streaming use case
- ML use case
- Deep Learning use case

