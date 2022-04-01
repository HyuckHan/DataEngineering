# WordCount 실행
## 코드 작성
```
편집기를 이용해서 WordCount.java 코드 작성
```
## 코드 컴파일 (ant를 이용)
```
$ cd ~/ DataEngineering/lab
$ ant
```
## input data upload
```
$ hadoop fs -mkdir input
$ hadoop fs -copyFromLocal ~/hadoop/*.txt input
```
## WordCount 실행
```
$ cd ~/ DataEngineering/lab
$ hadoop jar build/hadoop-project.jar WordCount input output
```
## 결과 확인
```
$ hadoop fs -cat output/part-r-00000
```
