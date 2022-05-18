# Spark Lab
## Spark Installation
```
$ cd ~
$ wget https://dlcdn.apache.org/spark/spark-3.2.1/spark-3.2.1-bin-hadoop3.2.tgz
$ tar -xvf spark-3.2.1-bin-hadoop3.2.tgz
$ ln –s spark-3.2.1-bin-hadoop3.2 spark
```
## Spark path 추가
```
echo "export PATH=\$PATH:~/spark/bin" >> ~/.bashrc
```
```
//동작 확인
$ spark-submit --version
```
## Lab
```
//기존 lab repository를 update
$ cd ~/DataEngineering
$ git pull
```
## WordCount
```
//programming
$ cd ~/DataEngineering/lab.spark
$ vi src/WordCount.java

//build
$ ant

//run
$ spark-submit --class JavaWordCount  build/spark-project.jar ~/hadoop/README.txt output
```
