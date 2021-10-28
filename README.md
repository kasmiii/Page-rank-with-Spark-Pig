# Page-rank-with-Spark-Pig
Page rank with Spark/Pig

**Apache Spark**
Spark is a unified analytics engine for large-scale data processing. It provides high-level APIs in Scala, Java, Python, and R, and an optimized engine that supports general computation graphs for data analysis. It also supports a rich set of higher-level tools including Spark SQL for SQL and DataFrames, pandas API on Spark for pandas workloads, MLlib for machine learning, GraphX for graph processing, and Structured Streaming for stream processing.

I used Spark for processing data and map reduce operations.

**Environment Installation** 

I followed these steps:
1. Installing Hadoop
2. Installing Apach Spark and Python
3. configuring .bachrc(linux file) for spark environment variable.

**Data used for processing**

I didn't found a data that contains website Urls, Thus, I used a text file that contains a graph of nodes , the data is in format: 

node_number  adjacent_node
node_number  adjacent_node
node_number  adjacent_node
....

Which node_number represents a wenbsite URL (URl website is supposed as a node number).
Nodes represent web pages and directed edges represent hyperlinks between them. The data was released in 2002 by Google as a part of Google Programming Contest.
This data is of size 104 MB

**Cluster configuration**

Région: us-central1
Zone: us-central1-a
Autoscaling
Nœud maître Standard (1 nœud maître, N nœuds de calcul)
Type de machine: n1-standard-4
Nombre de GPU: 0
Taille du disque principal: 500 Go
Nœuds de calcul: 3
Type de machine: n1-standard-4
Version d'image: 2.0.22-debian10

**Data Storage**

I put the data in my google storage because it's too large to put it to Git, and Git does not support data that exceeds 100MB (data is of 104 MB) and this is the link 
Link to data: https://drive.google.com/file/d/1Z1AqRWUokkPVsCeCfe_8tVnpAw2kDLU4/view?usp=sharing

**Execution**

To execute the project , we proceed to this command in a Operating system terminal: python3 pr.py data.txt 1

Where : 

**pr.py** the python script
**data.txt** is the data file text
**1** is the number of page ranking iterations

The general command syntax: python3 pr.py <path/to/data> <number of iterations>

**Notes:** 
  
I did not finish all the work because I am alone in the group, and therefore I found it difficult to complete everything
