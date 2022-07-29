# BDA Written Assignment 1
Roll number: 1902085
Class: C2

# Q1] Explain the hadoop architecture.

## Introduction

- The Apache Hadoop software library is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models. 
- It is designed to scale up from single servers to thousands of machines, each offering local computation and storage.
- Hadoop is used to store and analyze data from a variety of sources, including databases, web servers, and file systems.
- Rather than rely on hardware to deliver high-availability, the library itself is designed to detect and handle failures at the application layer, so delivering a highly-available service on top of a cluster of computers, each of which may be prone to failures.
- It is designed to be scalable by distributing the processing of data across a large number of computers. 

---

## Modules in Hadoop


### 1) Hadoop Common
The common utilities that support the other Hadoop modules.

### 2) Hadoop Distributed File System (HDFS™)
A distributed file system that provides high-throughput access to application data.

### 3) Hadoop YARN
A framework for job scheduling and cluster resource management.

### 4) Hadoop MapReduce
A YARN-based system for parallel processing of large data sets.

---

## Architecture

### Hadoop Distributed File System [HDFS]

![image](https://user-images.githubusercontent.com/52416311/180464746-c5e977e9-45f1-4b05-a94c-b000ae9ffb54.png)


- The master node keeps track of the status of all the data nodes. If a data node goes down, the master node takes over the processing of that block.
- The slave nodes process the data on their own. HDFS requires a high-speed Internet connection. It is usually best to have at least a 10 Mbps network connection.
- HDFS works on a time-based algorithm, which means that every block is processed in a predetermined time interval. 
- This provides a high degree of scalability as all the nodes process the data in real-time.
- HDFS is a great solution for data warehouse and business intelligence tasks. It is also a good solution for high-volume, high-frequency data analysis.

### MapReduce

- MapReduce is a data processing language and a software framework that allows you to process large amounts of data in a reliable and efficient manner. 
- It is a great fit for data-intensive, real-time and/or streaming applications. Basically, MapReduce allows you to partition your data and process items only when they are needed.
- A map-reduce job consists of several maps and reduces functions. Each map function generates, parses, transforms, and filters data before passing it on to the next function.
- The reduce function groups, aggregates, and partitioning of this intermediate data from the map functions. 
- The map task runs on the same node as the input source. Map tasks are responsible for generating summary statistics about data in the form of a report. The report can be viewed on a web browser or printed.
- The output of a map task is the same as that of a reduced task. The only difference is that the map task returns a result whereas the reduced task returns a data structure that is applicable for further analysis. 
- A map task is usually repetitive and is triggered when the data volume on the source is greater than the volume of data that can be processed in a short period of time.

### Yarn
- YARN, also known as Yet Another Resource Negotiator, is a resource management and job scheduling/monitoring daemon in Hadoop.
- A resource manager in YARN isolates resource management from job scheduling and monitoring. A global ResourceManager oversees operations for the entire YARN network, including per-application ApplicationMaster. 
- A job or a DAG of jobs may be defined as an application. The ResourceManager manages resources for all the competing applications in the YARN framework. 
- The NodeManager monitors resource usage by the container and passes it on to ResourceManger. There are resources such as CPU, memory, disk, and connectivity, among others.
- To perform and monitor the application, the ApplcationMaster talks to the ResourceManager and the NodeManager to handle and manage resources.

