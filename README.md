# Getting started with Pyspark and Twitter Data Analysis

## Installation

Prerequisites for this notebook are :
- Python3
- pip3
- java 8
- Scala ( I have used 2.11 for this example )


Next we have to install spark following the next steps :
- Go to [apache.spark.org](https://spark.apache.org/)
- Download Spark built for Hadoop 2.7 and unzip it into the `/home/` using a command as follows :
```
sudo tar -zxvf spark-x.x.x-bin-hadoopy.y.tgz
```

Of course, you need to replace x.x.x and y.y by the respective versions of Spark and Hadoop
- Set environment variables to link Python with Spark and Pyspark with Jupyter notebooks :
```
export SPARK_HOME=’/home/spark-x.x.x-bin-hadoopy.y/’
export PATH=$SPARK_HOME:$PATH
export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH
export PYSPARK_DRIVER_PYTHON=“jupyter”
export PYSPARK_DRIVER_PYTHON=OPTS=“notebook”
export PYSPARK_PYTHON=python3
```
- To prevent any permissions issues in the future, we run the following commands :
```
sudo chmod 777 home/spark-x.x.x-bin-hadoopy.y
```
We can verify whether this was successful or not by running `python3` from the `home/spark-x.x.x-bin-hadoopy.y` and then try `import pyspark`.
Then :
```
sudo chmod 777 home/spark-x.x.x-bin-hadoopy.y/python
sudo chmod 777 home/spark-x.x.x-bin-hadoopy.y/python/pypspark
```

**Caution** : To avoid frequent errors due to version conflicts, make sure Spark and Pyspark are of the same version. You can run the `pip freeze` command to check the version of Pyspark. My version is pyspark 2.4.4 therefore I have downloaded spark-2.4.4-bin-hadoop2.7.

## Start the tweet reader :
 
 Install the tweepy package required to connect with Twitter :
 ```
 pip3 install tweepy
 ```
 Then run the [tweetReader.py]() from the terminal

## Run the notebook to process the tweets

Check [TwitterApplication.ipynb]() for more details