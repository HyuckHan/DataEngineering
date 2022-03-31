# Java
## hadoop-env.sh
```
$ vi ~/hadoop/etc/hadoop/hadoop-env.sh
```
```
#export JAVA_HOME=
```
위의 내용을 아래와 같이 변경 (Java Home 디렉토리를 hadoop 환경 스크립트에 반영)
```
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/
```
# HDFS
## core-site.xml
```
$ vi ~/hadoop/etc/hadoop/core-site.xml
```
```
<configuration>
</configuration>
```
위의 내용을 아래와 같이 변경
```
<configuration>
    <property>
        <name>fs.defaultFS</name>
        <value>hdfs://localhost:9000</value>
    </property>
    <property>
        <name>hadoop.tmp.dir</name>
        <value>${user.home}/hadoop/tmp</value>
    </property>
</configuration>
```

## hdfs-site.xml

```
$ vi ~/hadoop/etc/hadoop/hdfs-site.xml
```
```
<configuration>
</configuration>
```
위의 내용을 아래와 같이 변경 (1개의 가상 머신에서 Lab을 진행하기 때문에 replication factor를 1로 한다.)
```
<configuration>
    <property>
        <name>dfs.replication</name>
        <value>1</value>
    </property>
</configuration>
```
# MapReduce
## mapred-site.xml
```
$ vi ~/hadoop/etc/hadoop/mapred-site.xml
```
```
<configuration>
</configuration>
```
위의 내용을 아래와 같이 변경 (yarn 스케쥴러를 사용하도록 설정.)
```
<configuration>
    <property>
        <name>mapreduce.framework.name</name>
        <value>yarn</value>
    </property>
</configuration>
```
## yarn-site.xml
```
$ hadoop classpath

/home/bigdata....... 이 내용을 아래의 xml 파일에 copy & paste한다.
```
```
$ vi ~/hadoop/etc/hadoop/yarn-site.xml
```
```
<configuration>
</configuration>
```
위의 내용을 아래와 같이 변경
```
<configuration>
    <property>
        <name>yarn.nodemanager.aux-services</name>
        <value>mapreduce_shuffle</value>
    </property>
    <property>
        <name>yarn.application.classpath</name>
        <value> 위의 hadoop 명령어의 결과를 copy & paste한다. </value>
    </property>
</configuration>
```
