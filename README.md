# DataEngineering
## Basic Requirements (Ubuntu {18|20}.04 기준)
```
$ sudo apt update
$ sudo apt install openjdk-8-jdk ant vim build-essential openssh-server
```

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

