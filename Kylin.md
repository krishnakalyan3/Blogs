# Introduction to Apache Kylin

Kylin is an open source Distributed Analytics Engine from eBay Inc. that provides SQL interface and multi-dimensional OLAP analysis on Hadoop supporting extremely large datasets. 
If you want to do multi-dimension analysis on large data sets with low query latency (sub-seconds), Kylin is a good option. It also provides seamless integration with existing BI tools such as Tableau.

To get started with Kylin you will need

1. [Download Cloudera Sandbox](http://www.cloudera.com/downloads/quickstart_vms/5-7.html)
2. [Download Apache Kylin](http://wwwftp.ciril.fr/pub/apache/kylin/apache-kylin-1.5.2.1/)


## Some Major Issues
Currently we cannot export cube meta data from one Kylin system to another (trakced by *KYLIN-1605*). 
The spark engine is an experimental phase, It did not achieve better performance compared to map-reduce engine (tracked by *KYLIN-744* and *KYLIN-1094*).
There are also GC related issues (tracked by *KYLIN-1861*)



References

* [Apache Kylin Official Website](http://kylin.apache.org/)
* [https://issues.apache.org/jira](https://issues.apache.org/jira/browse/KYLIN)
