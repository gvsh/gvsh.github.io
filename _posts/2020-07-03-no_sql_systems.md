# NoSQL Systems


## The Need for MapReduce

Relational Database Management Systems have been in use since 1970s. They provide the SQL language interface.

They are good at needle in the haystack problems – finding small results from big datasets.

They provide a number of advantages:

    A declarative query language
    Schemas
    Logical Data Independence
    Database Indexing
    Optimizations Through Use of Relational Algebra
    Views
    Acid Properties (Atomicity, Consistency, Isolation and Durability)

They provide scalability in the sense that even if the data doesn’t fit in main memory, the query will finish efficiently.

However, they are not good at scalability in another sense – that is, having multiple machines available, or multi-cores available will not reduce the time the query takes.

The need thus arose for a system which gives scalability when more machines are added and is thus able to process huge datasets (in 50 GB or more range).

The NoSQL databases give up on atleast one of the ACID properties to achieve better performance on parallel and/or distributed hardware.

## Introduction to Hadoop

Apache Hadoop is a software framework for distributed processing of very large datasets.

It provides a distributed storage system Hadoop Distributed File System (HDFS)), and a processing part of the system MapReduce.

The system is so designed so as to recover from hardware failures in some nodes that make up the distributed cluster.

Hadoop is itself written in Java. There are interfaces to use the framework from other languages.

Files on hadoop system are stored in a distributed manner. They are split into blocks which are then stored on different nodes.

The map and reduce functions that a user of hadoop framework writes are packaged and sent to different nodes where they are processed in parallel.
Architecture

The Hadoop framework is composed of the following four modules:

    Hadoop Common: – The libraries needed by the other Hadoop modules;
    Hadoop Distributed File System (HDFS):  A distributed file-system that stores data on commodity machines.
    Hadoop YARN: A platform responsible for managing computing resources in clusters.
    Hadoop MapReduce: A programming model for large scale data processing.

## HDFS

Files in HDFS are broken into blocks. The default block size is 64MB.

An HDFS cluster has two types of nodes – namenode (it works as the master node) and a number of datanodes (these work as the worker nodes).

The namenodes manages the filesystem namespace, maintains the filesystem tree, and the metadata of each file.

The user does not directly have to interact with the namenode or datanodes. A client does that on the user’s behalf. The client also provides a POSIX like filesystem interface.
MapReduce Engine

The MapReduce Engine sits on top of the HDFS filesystem. It consists of one JobTracker and a TaskTracker. The MapReduce jobs of the client applications are submitted to the JobTracker, which pushes the work to the available TaskTracker nodes in the cluster.

The filesystem is designed such that the JobTracker can know the nodes that contain the data, and how far they are.

The TaskTracker communicates with the JobTracker every few minutes to check its status.

The Job Tracker and TaskTracker expose their status and information through Jetty. This can be viewed from a web browser.

By default Hadoop uses FIFO scheduling. The job scheduler in modern versions is separate and it is possible to use an alternate scheduler (eg. Fair scheduler , Capacity scheduler).
The Hadoop Ecosystem

The term “Hadoop” now refers not just to the 4 base modules above, but also to the ecosystem, or collection of additional software packages that can be installed on top of or alongside Hadoop.

Examples of these are

Apache Pig,

Apache Hive,

Apache HBase,

Apache Spark,

Apache ZooKeeper,

Impala,

Apache Flume,

Apache Sqoop,

Apache Oozie,

Apache Storm.
