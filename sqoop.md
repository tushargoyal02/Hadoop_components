#   SQOOP
*   Problems of RDBMS
    *   Data import was tedious
    *   Handle large dataset
    *   Can't store ubstructured data
    *   Time consuming data

*   CLI for importing and exporting of data. Convert command to map-reduce.
Use yarn to import and export data to give fault tolerance

*   Start two letter from SQL and last three from hadoop

*   Tools to transfer data between HDFS & RDBMS

##  Feature of SQOOP

*   Full Load : Can load full table at once
*   Incremental load : can load parse table
*   Compression : We can compress the data
*   Load data to hive or HBASE


NOTE --> Reduce task doesn't occur in SQOOP.
*       Sqoop gives the task to the Map only, no reduce work ever occurs   

*   SQOOP Export - Return the hadoop files back into the RDBMS



### Configuration on local system

*   Extract the files 

*   mv sqoop-1.4.4.bin__hadoop-2.0.4-alpha /usr/lib/sqoop
*   export SQOOP_HOME=/usr/lib/sqoop export PATH=$PATH:$SQOOP_HOME/bin
*   $ cd $SQOOP_HOME/conf
*   $ mv sqoop-env-template.sh sqoop-env.sh
*   export HADOOP_COMMON_HOME=/usr/local/hadoop 
*   export HADOOP_MAPRED_HOME=/usr/local/hadoop


*   Extract the mysql connector 
*   cd mysql-connector-java-5.1.30
*   mv mysql-connector-java-5.1.30-bin.jar /usr/lib/sqoop/lib

Check with command " sqoop-version "

####    BASHRC files
*   Make this Entry in basrc file

        export HADOOP_MAPRED_HOME=$HADOOP_HOME
        export HADOOP_COMMON_HOME=$HADOOP_HOME
        export HADOOP_HDFS_HOME=$HADOOP_HOME
        export YARN_HOME=$HADOOP_HOME


        SQOOP_HOME=/usr/local/sqoop
        SQOOP_CONF_DIR=$SQOOP_HOME/conf
        SQOOP_CLASSPATH=$SQOOP_CONF_DIR


*   Go to /usr/local/sqoop/conf
    *   move file sqoop-env.template file to sqoop-env.sh file
    *   make entry to mapred files


