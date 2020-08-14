# Maven Installation On Linux
Maven is a code build tool which used to convert your code to artifact.

#### Install Maven on Jenkins
Download maven packages https://maven.apache.org/download.cgi onto Jenkins server. In this case I am using /opt/maven as my installation directory
	- Link : https://maven.apache.org/download.cgi
```sh
  # Creating maven directory under /opt
  mkdir /opt/maven
  cd /opt/maven
  # downloading maven version 3.6.0
  wget https://mirrors.estointernet.in/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
  tar -xvzf apache-maven-3.6.3-bin.tar.gz
 ```
	
Setup M2_HOME and M2 paths in .bash_profile of user and add these to path variable
```sh
  vi ~/.bash_profile
  M2_HOME=/opt/maven/apache-maven-3.6.3
  M2=$M2_HOME/bin
  PAHT=<Existing_PATH>:$M2_HOME:$M2
```
Once installtion done run below commands
```sh
logoff and login to check maven version
```
or
```sh
source ~/.bash_profile
```
Check maven version 
```sh
  mvn –version
``` 
