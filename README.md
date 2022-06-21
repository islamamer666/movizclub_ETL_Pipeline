# movizclub_ETL_Pipeline
 An end-to-end ETL Pipeline for Building User Behavior Metric Data Warehouse and Visualize Data by Metabase
## **Table of Contents**
* Architecture Diagram
* References
* License

### **Architecture Diagram**

![Architecture Diagram](https://user-images.githubusercontent.com/72258715/174892461-a18fbdd3-b05a-4364-9ac4-563cbba1a790.png)
**ETL Flow**
* Data is captured by python wrapper from Kaggle API
* Data collected from the API is uploaded to landing zone Amazon s3 bucket
* Then data is moved to working zone
* Then spark job is triggered which reeds data from working zone and apply transformations and moved data to the processed zone
* Then data moved to Redshift staging tables
*  UPSERT operation is performed on the Data Warehouse tables to update the dataset
*  ETL job execution is completed once the Data Warehouse is updated
*  Airflow DAG is used to schedule and orchestrate job tasks


#### **Reference**
Inspired by following codes, articles and videos:
* [AWS and python: the boto3 package](https://towardsdatascience.com/aws-and-python-the-boto3-package-df495bb29cb3)
* [Pyspark documentation](https://spark.apache.org/docs/latest/api/python/)
* [Psycopg documentation](https://www.psycopg.org/docs/)
* [Apache Airflow Documentation](https://airflow.apache.org/docs/apache-airflow/stable/index.html)


##### **License**
Distributed under the MIT License. for more information see [Lisence](https://github.com/islamamer666/Wikibooks_ETL_Pipeline/blob/main/LICENSE)


