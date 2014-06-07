simple-yarn-app
===============

Simple YARN application to run n copies of a unix command - deliberately kept simple (with minimal error handling etc.)

Usage:
======

### Unmanaged mode

$HADOOP_PREFIX/bin/hadoop jar $HADOOP_PREFIX/share/hadoop/yarn/hadoop-yarn-applications-unmanaged-am-launcher-2.2.0.jar Client -classpath /home/rakesh/simple-yarn-app-1.0-SNAPSHOT.jar -cmd "java com.hortonworks.simpleyarnapp.ApplicationMaster /bin/date 2"

### Managed mode

$ bin/hadoop fs -copyFromLocal simple-yarn-app-1.0-SNAPSHOT.jar /apps/simple/simple-yarn-app-1.0-SNAPSHOT.jar

$ bin/hadoop jar simple-yarn-app-1.0-SNAPSHOT.jar com.hortonworks.simpleyarnapp.Client /bin/date 2 /apps/simple/simple-yarn-app-1.0-SNAPSHOT.jar
  
    
