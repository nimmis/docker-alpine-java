## Alpine microcontainer with Java

This is docker images of Alpine 3.3 with different versions of java

### Examples

This images are build on nimmis/alpine-micro which are a modified version of Alpine with a working 
init process, and a working cron, logrotate  and syslog. Services are started with
runit daemon, for more information about that see [nimmis/alpine-mico](https://registry.hub.docker.com/u/nimmis/alpine-micro/)

#### starting the container with a normal shell

	docker run -ti nimmis/alpine-java:openjdk-7-jdk /bin/bash

This will start the container with a normal shell, no cron or other systems are started

#### starting the container as a daemon

	docker run -d nimmis/alpine-java:openjdk-7-jdk

This will start the container with the init process running, access the container with

	docker exec -ti <container ID> /bin/bash

### Loading different versions of java

The different version is determined with the TAG 

The available version are 

* latest 		 - OpenJDK Java version 8 JRE
* openjdk-7-jdk          - OpenJDK Java version 7 JDK
* openjdk-7-jre          - OpenJDK Java version 7 JRE
* openjdk-8-jdk          - OpenJDK Java version 8 JDK
* openjdk-8-jre          - OpenJDK Java version 8 JRE

Example to run a container with OpenJDK version 7 JDK

	docker run -d nimmis/alpine-java:openjdk-7-jdk

