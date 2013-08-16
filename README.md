SpringXmlConfigExample-Update
=============================
###(with Servlet 2.5 and JSTL 1.2)

A Simple Spring MVC application with XML configuration for servlet 2.5 and a complete test suite

For me this is more of a memory aide as well as a learning tool.  I wanted to have a fully tested, template web application to jump start any future projects for work as well as being able to easily reference things that I have learned or just want to remember.  This will be the first template program in a series I am working on in my free time, I hope to soon have four of these examples.

* Spring MVC with XML Config
* Spring MVC with Java Config
* Spring MVC with Groovy on Grails    
* Spring MVC with Scala

Spring MVC with XML Config
=======================
For the xml based config I have the servlet configured as 2.4 as servlet 2.4 is the highest version that will still run on a Tomcat 5.5 container as well as JSTL 1.1.2 (I will be updating these in another example). At the time of writing this, cobertura shows by test coverage to be around 94% of all lines of code.

Setup
==============
To run this example you will need to setup a MySql database called test. Then you will need to change the username and password located in either the jetty.xml or context.xml.  After that you will need to run the Example-Create.sql file which is located under src/main/resources/sql-setup in order to setup the correct tables.

Running the Example
==============
To actually execute the example use any of the following commands. 

Run with Jetty 8
```
mvn jetty:run
```
Run with Tomcat 7
```
mvn tomcat7:run
```
Run with Tomcat 6
```
mvn tomcat6:run
```

If you want to build the example as a war and run all the tests then run the following.
```
mvn clean package
```

Testing
==============
I have done my best to completely write tests around my template to ensure that it will work out of the box and that I (or you) no longer have to be frustrated with examples that don't work when trying to get going on a new project. I have used the JUnit 4 framework and have both unit and integration tests around most of the code. At the moment I do not have integration tests around the controllers as I have not had time to figure out how to bypass spring security to allow these to run.  All mocking is performed with Mockito.  I hope to continue using this as a learning tool and will try to teach myself TestNG in the near future, when I get to that point I will add those tests as well.

####Tested Java Versions:

* Java 1.6.0_45
* Java 1.7.0_21

No issues with either of the versions I tried at least none that I noticed

####Tested Containers:

* Tomcat 5.5.28 
* Tomcat 6.0.36  
* Tomcat 7.0.37   
* Jetty  8.1.12.v20130726                                                                                               

The later three are all runable from the maven plugin and have been configured with a JNDI datasource.
####Tested Compilers:

* Maven 3.0.5    
* Maven 3.1.0

Builds and runs tests with either version without issue.

