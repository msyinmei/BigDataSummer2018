JAB 473, NYU

#Agenda

```
10-12 Spark ML on IBM cloud
12-2 Lunch
2-4 AdHoc Questions

1) Address questions you have
2) local install of mongo
3) Cloud related questions
4) P2 questions
```
#Morning Topics:

On the White Board:

```
ML: Demo of 1 Algorithm
Take ML algo, run in Spark and run in R to compare. 

Scenario 2 - Using R
1) Random #
2) Create training/test
3) Run Algo
4) Capture Performance mcbits (AUI, Accuracy)

Scenario #2
1) Write spark code, compile, and run

Final Goal
1) compare results #1 and #2
```

###
---

I. INTRODUCTION
#Concurrent Distributed Computing & Tuple Space maintenance:
Background: If you go to IBM, they have a big presence in multiple continents. 
IBM has one of the biggest research projects require 64 days of running: 
Avogadro's Number: 6.023 * 10^23, Better fiber optic etc. 
How do they do it? They use tools to help them. 

Condor:
"Allows users to harness the power of a pool of machines while using otherwise wasted CPU cycles"
The Condor is a hunting bird aka it harnesses the process of a hunter. Condo hunts for free un-utilized cpu cycles. 

Linda: namespace (names)

ISIS: temporally ordered, distributed systems. 
https://www.cs.cornell.edu/Info/Projects/Isis/

PVM: high VM

Each of these tools create value for computing big data, our goal is to understand what is required to make these 


###
---

II. Maven Exercise

#Workshop 1 
About Maven: a project management tool based on a project object model (perhaps binary classifiers?)

Practice Round 1:
Steps Taken: 
0) set working directory as src directory 
1) mvn clean
2) mvn compile
3) mvn install
4) running spark-submit

Shell Commands
```sh
cd /home/examples/spark.rk/TitanicGBT
which spark-submit
which mvn
mvn clean
mvn compile
mvn clean
```

Practice Round 2 to use TitanicGBT as template and rename it:
Steps Taken:
0) create directory wrkshp072018
1) copy recursively (-R) the TitanicGBT directory into new directory
2) enter copied directory (TitanicGBT)
3) check that mvn is available
4) check that java is available
5) change directory to parent directory (wrkshp072018)
6) check if spark-submit is available
7) like it is not, so copy the sparkpath.sh file into the wrkshp072018 directory
8) run ./sparkpath.sh
9) check if spark-submit is available, it should now show you the path
10) change directory into TitanicGBT 
11) run mvn clean, mvn compile and mvn install
12) run spark-submit with correct parameters (as shown below)
13) 


Shell Commands
```sh
mkdir wrkshp072018
cd wrkshp072018/
cp -R /home/examples/spark.rk/TitanicGBT/ . 
cd TitanicGBT/
ls
  commands.txt  pom.xml  src  TitanicGBT.iml  titanic_test.csv  titanic_train.csv
which mvn
  /usr/local/maven/bin/mvn
mvn -version
  Apache Maven 3.5.2 (138edd61fd100ec658bfa2d307c43b76940a5d7d; 2017-10-18T03:58:13-04:00)
  Maven home: /usr/local/maven
  Java version: 1.8.0_141, vendor: Oracle Corporation
  Java home: /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.141-2.b16.el7_4.ppc64le/jre
  Default locale: en_US, platform encoding: UTF-8
  OS name: "linux", version: "3.10.0-229.ael7b.ppc64le", arch: "ppc64le", family: "unix"
which java
  /usr/bin/java
java -version
  openjdk version "1.8.0_141"
  OpenJDK Runtime Environment (build 1.8.0_141-b16)
  OpenJDK 64-Bit Server VM (build 25.141-b16, mixed mode)
cd ..
which spark-submit
  /usr/bin/which: no spark-submit in (/usr/lib64/qt-3.3/bin:/home/2018/summer/nyu/6513/ym1524/perl5/bin:/usr/local/maven/bin:/usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/2018/summer/nyu/6513/ym1524/.local/bin:/home/2018/summer/nyu/6513/ym1524/bin)
pwd
  /home/2018/summer/nyu/6513/ym1524/wrkshp072018/
cp /home/examples/spark.rk/sparkpath.sh .
ls
  sparkpath.sh  TitanicGBT
. ./sparkpath.sh
which spark-submit
  /home/examples/spark.rk/sparkpath.sh (or perhaps some other path)
cd TitanicGBT/
mvn clean
mvn compile
mvn install
./spark-submit --master local[*] --class GBTTitanicClassification <~/TitanicGBT-1.0-SNAPSHOT.jar replace with your own path, located in the first line of the install messages> 

If breaks, run ./sparkpath.sh again 

spark-submit --master local[*] --class GBTTitanicClassification /home/2018/summer/nyu/6513/ym1524/.m2/repository/com/bigdata/project2/TitanicGBT/1.0-SNAPSHOT/TitanicGBT-1.0-SNAPSHOT.jar
```

#Maven
https://maven.apache.org/guides/introduction/introduction-to-the-pom.html

```sh
cd wrkshp072018/TitanicGBT/
emacs -nw pom.xml
cd
cd .m2
cd  repository/
cd com
cd bigdata/
cd project2/
cd TitanicGBT/
cd 1.0-SNAPSHOT/
ls
maven-metadata-local.xml  _remote.repositories  TitanicGBT-1.0-SNAPSHOT.jar  TitanicGBT-1.0-SNAPSHOT.pom
pwd
/home/2018/summer/nyu/6513/ym1524/.m2/repository/com/bigdata/project2/TitanicGBT/1.0-SNAPSHOT
```

Examine the POM file: 
emacs the TitanicGBT-1.0-SNAPSHOT.pom

How to use as a template?
1) copy recursively
2) rename
3) change pom file. 


```sh
cp -R ../TitanicGBT/ .
mv TitanicGBT/ Challenger/
grep -i titanic pom.xml
    <artifactId>TitanicGBT</artifactId> 
```

Decision Tree exercise:
```
mkdir DecisionTree; cd DecisionTree;
wget https://github.com/apache/spark/blob/master/examples/src/main/java/org/apache/spark/examples/ml/JavaDecisionTreeClassificationExample.java
```


