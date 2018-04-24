Basic JMS example
=====================================
Example taken from [Practical Java EE 7 Development using WildFly application server](http://www.itbuzzpress.com/ebooks/java-ee-7-development-on-wildfly.html)

This example demonstrates the basic usage of a remote JMS 2.0 client

###### Pre-requisites:
You need the following Queue Definition in a full/full-ha profile:

```xml
 <jms-queue name="ExampleQueue" entries="queue/exampleQueue java:/jboss/exported/jms/queue/exampleQueue"/>
```

###### Build Deploy and Test
```shell
mvn clean install test  
```
**Important Notice** If the javaee7-jms-basic example is running on your server, the receiver will fail to grab the message, that will be consumed by the MDB contained in javaee7-jms-basic. So undeploy at first the **javaee7-jms-basic** application using:
```shell
mvn clean install wildfly:undeploy  
```



