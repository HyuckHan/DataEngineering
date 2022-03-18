# DataEngineering
## Hadoop Installation
```
$ cd ~
$ wget https://dlcdn.apache.org/hadoop/common/hadoop-3.3.2/hadoop-3.3.2.tar.gz
$ tar -xvf hadoop-3.3.2.tar.gz
$ ln -s hadoop-3.3.2 hadoop
```

```
/* password 없이 localhost에 ssh login하기 */
$ ssh-keygen -t rsa
$ cat ~/.ssh/id_rsa.pub >>  ~/.ssh/authorized_keys
```
## Lab
```
$ cd ~
$ git clone https://github.com/HyuckHan/DataEngineering.git
```

```
$ cd DataEngineering/lab
$ vi build.xml

build.xml에서 hadoop.dir property를 /home/<your id>/hadoop으로 변경한다.
 <property name="hadoop.dir" location="/home/hhyuck/hadoop/"/>
```

