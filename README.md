# HadoopExamples

# Hadoop Examples 

![HortonWorks](https://github.com/jims6602/ImageForWiki/blob/main/Logos/hortonworks.PNG)

## Introduction   
Hadoop is a open software platform for distributed stoarge and ditributed processing of very large data sets on computer clusters build from commodity hardware.

## Why Hadoop?  
* Data's too darn big - terabytes per day
* Vertical scaling does not cut it   
         1. Disk seek times    
         2. Hardware failures    
         3. Processing times    
* Horizontal scaling is linear    
* Hadoop: It is not just for batch processing anymore  


### Core Hadoop Ecosystem

<img 
src="https://github.com/jims6602/ImageForWiki/blob/main/HadoopExamples/CoreHadoopEcosystem.PNG" 
alt="Angular Start Page" 
height="300px"/>


* **Apache Hadoop HDFS**     

Hadoop File System was developed using distributed file system design as core part of Apache Hadoop. It is run on commodity hardware. Unlike other distributed systems, HDFS is highly faulttolerant and designed using low-cost hardware.   

HDFS holds very large amount of data and provides easier access. To store such huge data, the files are stored across multiple machines. These files are stored in redundant fashion to rescue the system from possible data losses in case of failure. HDFS also makes applications available to parallel processing. 

* **Apache Hadoop MapReduce**      

As core part of Apache Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel on large clusters (thousands of nodes) of commodity hardware in a reliable, fault-tolerant manner.      

A MapReduce job usually splits the input data-set into independent chunks which are processed by the map tasks in a completely parallel manner. The framework sorts the outputs of the maps, which are then input to the reduce tasks. Typically both the input and the output of the job are stored in a file-system. The framework takes care of scheduling tasks, monitoring them and re-executes the failed tasks.


* **Apache Hadoop YARN** (Yet Another Resource Negotiator)  

As core part of Apache Hadoop YARN is to split up the functionalities of resource management and job scheduling/monitoring into separate daemons. The idea is to have a global ResourceManager (RM) and per-application ApplicationMaster (AM). An application is either a single job or a DAG of jobs.   

The ResourceManager and the NodeManager form the data-computation framework. The ResourceManager is the ultimate authority that arbitrates resources among all the applications in the system. The NodeManager is the per-machine framework agent who is responsible for containers, monitoring their resource usage (cpu, memory, disk, network) and reporting the same to the ResourceManager/Scheduler.   

The per-application ApplicationMaster is, in effect, a framework specific library and is tasked with negotiating resources from the ResourceManager and working with the NodeManager(s) to execute and monitor the tasks.     

* **MESOS**

Apache Mesos is an open-source project to manage computer clusters. Alternative to Apache Hadoop YARN.

* **Apache Ambari** 

The Apache Ambari project is aimed at making Hadoop management simpler by developing software for provisioning, managing, and monitoring Apache Hadoop clusters. Ambari provides an intuitive, easy-to-use Hadoop management web UI backed by its RESTful APIs.

* **Pig**

The language for this platform is called Pig Latin. Pig can execute its Hadoop jobs in MapReduce, Apache Tez, or Apache Spark. Pig Latin abstracts the programming from the Java MapReduce idiom into a notation which makes MapReduce programming high level, similar to that of SQL for relational database management systems. Pig Latin can be extended using user-defined functions (UDFs) which the user can write in Java, Python, JavaScript, Ruby or Groovy and then call directly from the language.     

* **Hive**

Apache Hive is a data warehouse software project built on top of Apache Hadoop for providing data query and analysis. Hive gives a SQL-like interface to query data stored in various databases and file systems that integrate with Hadoop. Traditional SQL queries must be implemented in the MapReduce Java API to execute SQL applications and queries over distributed data. Hive provides the necessary SQL abstraction to integrate SQL-like queries (HiveQL) into the underlying Java without the need to implement queries in the low-level Java API. Since most data warehousing applications work with SQL-based querying languages, Hive aids portability of SQL-based applications to Hadoop

* **Tez**

Apache™ Tez is an extensible framework for building high performance batch and interactive data processing applications, coordinated by YARN in Apache Hadoop. Tez improves the MapReduce paradigm by dramatically improving its speed, while maintaining MapReduce’s ability to scale to petabytes of data. Important Hadoop ecosystem projects like Apache Hive and Apache Pig use Apache Tez, as do a growing number of third party data access applications developed for the broader Hadoop ecosystem.

* **Spark**

Apache Spark has as its architectural foundation the resilient distributed dataset (RDD), a read-only multiset of data items distributed over a cluster of machines, that is maintained in a fault-tolerant way. The Dataframe API was released as an abstraction on top of the RDD, followed by the Dataset API. In Spark 1.x, the RDD was the primary application programming interface (API), but as of Spark 2.x use of the Dataset API is encouraged even though the RDD API is not deprecated. The RDD technology still underlies the Dataset API.

* **Apache HBASE**

Use Apache HBase™ when you need random, realtime read/write access to your Big Data. This project's goal is the hosting of very large tables -- billions of rows X millions of columns -- atop clusters of commodity hardware. Apache HBase is an open-source, NoSQL, distributed, versioned, non-relational database modeled 

* **Apache Storm**

Apache Storm is a free and open source distributed realtime computation system. Storm makes it easy to reliably process unbounded streams of data, doing for realtime processing what Hadoop did for batch processing. Storm is simple, can be used with any programming language, and is a lot of fun to use!

* **Zookeeper**

ZooKeeper is a centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services. All of these kinds of services are used in some form or another by distributed applications. Each time they are implemented there is a lot of work that goes into fixing the bugs and race conditions that are inevitable. Because of the difficulty of implementing these kinds of services, applications initially usually skimp on them, which make them brittle in the presence of change and difficult to manage. Even when done correctly, different implementations of these services lead to management complexity when the applications are deployed.

* **Oozie**

Oozie is a workflow scheduler system to manage Apache Hadoop jobs.  

Oozie Workflow jobs are Directed Acyclical Graphs (DAGs) of actions.    

Oozie Coordinator jobs are recurrent Oozie Workflow jobs triggered by time (frequency) and data availability.    

Oozie is integrated with the rest of the Hadoop stack supporting several types of Hadoop jobs out of the box (such as Java map-reduce, Streaming map-reduce, Pig, Hive, Sqoop and Distcp) as well as system specific jobs (such as Java programs and shell scripts).   

Oozie is a scalable, reliable and extensible system.   

#### Data Ingestion
* **Sqoop**  

Apache Sqoop is a tool designed for efficiently transferring bulk data between Apache Hadoop and structured datastores such as relational databases.

* **Flume**

Apache Flume is a distributed, reliable, and available software for efficiently collecting, aggregating, and moving large amounts of log data. It has a simple and flexible architecture based on streaming data flows. It is robust and fault tolerant with tunable reliability mechanisms and many failover and recovery mechanisms. It uses a simple extensible data model that allows for online analytic application.

* **Kafka**

The project aims to provide a unified, high-throughput, low-latency platform for handling real-time data feeds. Its storage layer is essentially a "massively scalable pub/sub message queue designed as a distributed transaction log, making it highly valuable for enterprise infrastructures to process streaming data. Additionally, Kafka connects to external systems (for data import/export) via Kafka Connect and provides Kafka Streams, a Java stream processing library.

### External Data Storage   

<img 
src="https://github.com/cusey/ImageForWiki/blob/master/HadoopExamples/ExternalDataStorage.png" 
alt="/ExternalDataStorage" 
height="300px"/>

* **MySql**

MySQL is an open source relational database management system. MySQL is a component of the LAMP web application software stack (and others), which is an acronym for Linux, Apache, MySQL, Perl/PHP/Python. MySQL is used by many database-driven web applications, including Drupal, Joomla, phpBB, and WordPress.

* **Cassandra**

Apache Cassandra is a free and open-source, distributed, wide column store, NoSQL database management system designed to handle large amounts of data across many commodity servers, providing high availability with no single point of failure. Cassandra offers robust support for clusters spanning multiple datacenters,[1] with asynchronous masterless replication allowing low latency operations for all clients.

* **Mongo DB**

MongoDB is a cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schemata. 


### QueryEngines 

The full definition of an SQL query engine is a piece of software that   

* Recognizes and interprets the SQL language.    
* Implements data access, both reading and writing, for a relational database, in a way that can be controlled by a user's SQL queries. 
* Enforce a variety of other resources and data integrity policies necessary for a relational data model and database management system.  
<img 
src="https://github.com/cusey/ImageForWiki/blob/master/HadoopExamples/QueryEngines.png" 
alt="/QueryEngines" 
height="300px"/>

* **Apache Drill**
* **Apache Phoenix**
* **Apache Zeppelin**
* **Hue**
* **Presto**



## Login
To login into Ambari is (If you have problems login to Ambari check the Windows Services in your Control Panel make sure Oracle database is not running on port 8080. You can stop OracleServiceXE and change the startup type to manual so the next time login in your computer the Oracle Service is not running.) :
* Username : maria_dev
* Password : maria_dev

## Install Instructions
[Getting Started with Horton Works](https://hortonworks.com/tutorial/hadoop-tutorial-getting-started-with-hdp/)
