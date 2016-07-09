# Introduction to Apache Kylin

Kylin is an open source Distributed Analytics Engine from eBay Inc. that provides SQL interface and multi-dimensional OLAP analysis on Hadoop supporting extremely large datasets. 
If you want to do multi-dimension analysis on large data sets with low query latency (sub-seconds), Kylin is a good option. It also provides seamless integration with existing BI tools such as Tableau.

At a very high level Kylin  
* Reads data from HDFS using HIVE.
* Runs MapReduce jobs to process data.
* Stores results in HBase.

To get started with Kylin you will need

1. [Download Cloudera Sandbox](http://www.cloudera.com/downloads/quickstart_vms/5-7.html)
2. [Download Apache Kylin](http://wwwftp.ciril.fr/pub/apache/kylin/apache-kylin-1.5.2.1/)


#### Some Major Issues
Currently we cannot export cube meta data from one Kylin system to another (trakced by *KYLIN-1605*).  
Spark engine is an experimental phase, It did not achieve better performance compared to MapReduce engine (tracked by *KYLIN-744* and *KYLIN-1094*).  
There are also some GC related issues (tracked by *KYLIN-1861* and *KYLIN-1692*).  
Currently there are more than 400 outstanding issues out of which around 75% of them have been tagged as major issues. I am sure they will be ironed out soon as this projct has a strong [open source community](https://github.com/apache/kylin/graphs/contributors) and support of orginizations like eBay.

#### Conclusion
Currently Kylin has been deployed in production at eBay and is processing extremely large datasets. The platform has demonstrated great performance benefits and has proved to be a better way for analysts to leverage data on Hadoop with a more convenient approach using their favorite tool. Even open source projects like [Apache Zeppelin](https://zeppelin.apache.org/) leverage Kylin interpreter.


References

* [Apache Kylin Website](http://kylin.apache.org/)
* [Apache Kylin JIRA](https://issues.apache.org/jira/browse/KYLIN)