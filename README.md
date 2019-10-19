# Spark-In-Windows
Setup Apache Spark in Windows and In Jupyter Notebook Using Anaconda

Installing Apache Spark in Linux is easy but in Windows it is bit complex. Let's wrap up everything and solve this as piece of cake.

1. You need to install Anaconda Software.
Download it from here with your pc specs
https://www.anaconda.com/distribution/#download-section

2. Download Apache Spark
https://www.apache.org/dyn/closer.lua/spark/spark-2.4.4/spark-2.4.4-bin-hadoop2.7.tgz

3. Create a folder in your location like C:
 e.g spark
 
Now using 7zip extractor extract your Spark you have downloaded in your folder.
(Note: It may just decompress .tar u need to again extract it and move all file to spark folder destination)

4. Create one more folder in your location
e.g hadoop
one subfolder name it 'bin'
so ur directory now
  C:\hadoop\bin

Go to this link : https://github.com/khutal/winutils.git
download and extract and copy winutils.exe to hadoop/bin/

5. Now Adding path just like we do in Linux in bashrc
 step: Search 'edit environment variables for your account' in your search bar of windows
 or right click on 'This Pc'-> Properties -> Advanced System setting -> Environment Variables
 
 Under User Variable box, 
 click New -> Variable Name : HADOOP_HOME -> Variable value : location(C:\hadoop) or browse your directory and select
 Same like that add path for Spark. Good Now next.
 
 Under System Variables
 Click on path -> edit -> New -> add path with bin e.g C:\hadoop\bin also add C:\spark\bin -> OK -> OK.  Thats it we're done here. Few more step
 
 6. Now Anaconda Part
 Search Anaconda Prompt, Cmd will open -> write this command
 
 python -m pip install findspark
 
 wait for install (sometime it will not it is installed, then press any key.. it will show successfully installed)
 
 Now open Jupyter notebook. Search and it will automatically open in your browser.
 On right side of jupyter home page you find (New) dropdown -> select python 3 -> your py book will open
 
 Let's check pyspark is working or not
 
 import findspark
 findspark.init()
 
 This will execute perfectly. Seems, You got no error. You're Good to Go

### On Windows cmd or you need Spark Web UI
Simply run 'spark-shell' in your command line, spark shell will be up and you will get WEB UI ip like  http://172.22.42.67:4041
open it you will able to see Spark context Web UI.

<3
