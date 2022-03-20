# Java
## hadoop-env.sh
```
$ vi ~/hadoop/etc/hadoop/hadoop-env.sh
```
```
#export JAVA_HOME=
```
위의 내용을 아래와 같이 변경
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
1개의 가상 머신에서 Lab을 진행하기 때문에 replication factor를 1로 한다.

```
$ vi ~/hadoop/etc/hadoop/hdfs-site.xml
```
```
<configuration>
</configuration>
```
위의 내용을 아래와 같이 변경
```
<configuration>
    <property>
        <name>dfs.replication</name>
        <value>1</value>
    </property>
</configuration>
```