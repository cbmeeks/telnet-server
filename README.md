Simple Telnet Server
=====================


This is a simple Telnet server written in Java. It supports basic Unix commands such as: ls, mkdir, pwd, cd, rm. It is intended for novice Java developers to learn how to write server/client communication. It doesn't use any external libraries, so it's pure Core Java to factilitate the learning. Enjoy!


How to run the server
=======================

> Maven: mvn exec:java (The sever will be run on port 12667 by default. This can be overriden in pom.xml. If you run the server from the exectuable jar, it will use whatever defined in server.properties file)


> IDE: run ServerLauncher.java as Java application.


Running example
================

* Run the server as above explanation. 
* open a bash or cmd terminal and run: telnet localhost 12667. It should display an welcome message with all the possible commands. By default working directoy is set to 'user.home', i.e (wherever you unzipped the file)

* Limitations of some of the commands:
  
> ls: It only list the files within the working directory, so path as argument isn't supported.

> cd: It supports navigating into sub-directories of the 'user.home' directory. Full path is also supported such as '/usr/local' or 'C:\Documents'.

How to build the jar
=====================
> mvn clean install (will run the tests too)

> Maven build jar

  * mvn clean install to build the jar
  * cd target/ then run: java -jar telnet-server.jar



How to run tests
=====================

> mvn clean test
