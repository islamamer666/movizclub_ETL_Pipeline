# movizclub_ETL_Pipeline
 An end-to-end ETL Pipeline for Building User Behavior Metric Data Warehouse and Visualize Data by Metabase
## **Table of Contents**
* Architecture Diagram
* References
* License

### **Architecture Diagram**

![Architecture Diagram](https://user-images.githubusercontent.com/72258715/174892461-a18fbdd3-b05a-4364-9ac4-563cbba1a790.png)
**ETL Flow**
* Loading movie reviews into Amazon s3
* Classification process on movie reviews with Apache Spark
* Loading the classified movie reviews into the data warehouse
* Extract user purchase data from an OLTP database and load it into the data warehouse
* Joining the classified movie review data and user purchase data to get user behavior metric data





#### **Reference**
Inspired by following codes, articles and videos:
* [Pyspark documentation](https://spark.apache.org/docs/latest/api/python/)
* [Psycopg documentation](https://www.psycopg.org/docs/)
* [Apache Airflow Documentation](https://airflow.apache.org/docs/apache-airflow/stable/index.html)


##### **License**
Distributed under the MIT License. for more information see [Lisence](https://github.com/islamamer666/Wikibooks_ETL_Pipeline/blob/main/LICENSE)


