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
3. Atleast 8GB RAM configured for your VM

Make sure you download Apache Kylin to `/opt/` folder  
```
sudo tar -xvzf apache-kylin-1.5.2.1-cdh5.7-bin.tar.gz  
sudo ln -s apache-kylin-1.5.2.1-bin/ apache-kylin  
vim ~/.bash_profile  
export KYLIN_HOME=/opt/apache-kylin (Add this line to ENV variables)  
source ~/.bash_profile  
sudo bin/kylin.sh start  
```
   
 
![Installation Procedure](install.gif)  





#### Building Cubes


#### Some Issues
Difficult to export cube meta data from one Kylin system to another (trakced by *KYLIN-1605*).  
Spark engine is an experimental phase as it did not achieve a better performance when compared to MapReduce engine (tracked by *KYLIN-744* and *KYLIN-1094*).  
Some GC related issues (tracked by *KYLIN-1861* and *KYLIN-1692*).  
Currently there are more than 400 outstanding issues out of which around 75% of them have been tagged as major issues. I am sure they will be ironed. This projct has a strong [open source community](https://github.com/apache/kylin/graphs/contributors) which alsoe includes the support of orginizations like eBay.

#### Conclusion
Currently Kylin has been deployed in production at eBay and is processing extremely large datasets. The platform has demonstrated great performance benefits and has proved to be a better way for analysts to leverage data on Hadoop with a more convenient approach using their favorite tool. Even open source projects like [Apache Zeppelin](https://zeppelin.apache.org/) leverage the Kylin interpreter.


References:  
* [Apache Kylin Website](http://kylin.apache.org/)
* [Apache Kylin JIRA](https://issues.apache.org/jira/browse/KYLIN)