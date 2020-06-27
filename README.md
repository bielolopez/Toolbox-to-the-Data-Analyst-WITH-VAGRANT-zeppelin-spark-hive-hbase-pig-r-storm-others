# vagrant-spark-hive-hbase-pig-r-pyspark-zeppelin-and-others
##Educational virtual machine to practice scala, spark.r, pyspark, pig, hbase, flume, and others big data technology


In the repository you will find a file version.sh in the folder called scripts where the versions of each technology are found to find the most convenient combination for your work. 
They can also download the technologies in the resources folder and also changing the version, it will not be necessary that when lifting the virtual machine each of tar.gz or .tgz must be downloaded.
If any repository changes places, an error will appear but it will say that the installation is complete, so they will have to find the appropriate and current repository to introduce the change in the common.sh file located also in the scripts folder.

 After having made the vagrant up and connected to the virtual machine by terminal with vagrant ssh,
 I highly recommend doing it as an administrator, if necessary, proceed to install R.

The procedure for installing R is as follows:

sudo apt-get update

sudo apt-get install libxml2-dev

sudo apt-get install libcurl4-openssl-dev libssl-dev

sudo apt-get install r-base



Validate the installation of R with:

Introduce R in the terminal.

Install additional libraries:

install.packages("devtools")

install.packages("ggplot2")

install.packages("glmnet")

install.packages("caret")

install.packages("pROC")

install.packages("data.table")

install.packages("lme4")

install.packages("sqldf")

install.packages("wordcloud")

install.packages("tidyverse")

and others packages.


Before you run Zeppelin with cd /opt/zeppelin  and ./bin/zeppelin-deamon.sh start, change the permission of all folder in zeppelin folder.





Install Apache MAHOUT if you need.

Second, How to install directly from tar file.
Download .tar.gz file.
sudo tar -zxvf mahout-distribution-#.#.tar.gz.
sudo mv mahout-distribution-#.# /usr/lib/mahout
sudo nano ~/.bashrc
introduce in .bashrc =>   export MAHOUT_HOME=/usr/local/mahout
Run this command for update bashrc  =>       source ~/.bashrc
Is installed successfully.




To install SCALA 2.11

sudo apt-get update
sudo apt-get install scala



If you need MAVEN

wget http://apache.mirrors.pair.com/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
sudo tar -xvzf apache-maven-3.6.3-bin.tar.gz
sudo mv apache-maven-3.6.3 /opt/maven
sudo nano /etc/profile.d/mavenenv.sh


Add this lines to mavenenv.sh
export M2_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}

Save the changes with escape and :wq

Change the permission of mavenenv.sh file.
sudo chmod +x /etc/profile.d/mavenenv.sh

And update this file for the systems.
source /etc/profile.d/mavenenv.sh

Verify
mvn --version

Thanks to Alex Holmes for the great work at github path>>> https://github.com/alexholmes/vagrant-hadoop-spark-hive
