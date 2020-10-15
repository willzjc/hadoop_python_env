# Running a localized Hadoop environment with a Python pipeline
winutils.exe hadoop.dll and hdfs.dll binaries for hadoop on windows

# Instructions

## Base installation packages

1. Python runtime environment

From https://repo.anaconda.com/archive/
Specifically - https://repo.anaconda.com/archive/Anaconda2-2019.10-Windows-x86_64.exe


2. IntelliJ Community Edition

https://download.jetbrains.com/idea/ideaIC-2020.2.2.exe

3. JDK

Download
https://portapps.io/app/oracle-jdk-portable/#download

And make sure to install to

```
C:\Users\%USERNAME%\dev\jdk
```

If path doesn't exist then run

```
mkdir C:\Users\%USERNAME%\dev
mkdir C:\Users\%USERNAME%\dev\jdk
```

4. Hadoop Libraries

This is part of the git repository - no need to source externally

## Configuration setup

Setup path variables - do this on the basepath of this repo
```
setx HADOOP_HOME %CD%\hadoop-2.7.6
setx SPARK_HOME %CD%\spark-2.4.6-bin-hadoop2.7

REM This stop may not work if user does not have elevated access
REM Recommended then to install JDK within user's own userspace and then point JAVA_HOME to it

setx JAVA_HOME "C:\Program Files\Java\jre1.8.0_181"
```
