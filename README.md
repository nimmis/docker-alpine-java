## Alpine microcontainer with Java

This is a micro docker container [![](https://images.microbadger.com/badges/image/nimmis/alpine-java.svg)](https://microbadger.com/images/nimmis/alpine-java "Get your own image badge on microbadger.com") based on Alpine 3.5 [nimmis/alpine-mico](https://registry.hub.docker.com/u/nimmis/alpine-micro/) (for oracle java Alpine with glibc [nimmis/alpine-glibc](https://registry.hub.docker.com/u/nimmis/alpine-glibc/) is used) with different versions of OpenJDK and Oracle java

### Examples

This images are build on nimmis/alpine-micro which are a modified version of Alpine with a working 
init process, and a working cron, logrotate  and syslog. Services are started with
runit daemon, for more information about that see [nimmis/alpine-mico](https://registry.hub.docker.com/u/nimmis/alpine-micro/)

#### starting the container with a normal shell

	docker run -ti nimmis/alpine-java:openjdk-8-jdk /bin/bash

This will start the container with a normal shell, no cron or other systems are started

#### starting the container as a daemon

	docker run -d nimmis/alpine-java:openjdk-8-jdk

This will start the container with the init process running, access the container with

	docker exec -ti <container ID> /bin/bash

### Loading different versions of java

The different version is determined with the TAG 

## Issues

If you have any problems with or questions about this image, please contact us by submitting a ticket through a [GitHub issue](https://github.com/nimmis/docker-alpine-java/issues "GitHub issue")

1. Look to see if someone already filled the bug, if not add a new one.
2. Add a good title and description with the following information.
 - if possible an copy of the output from **cat /etc/BUILDS/*** from inside the container
 - any logs relevant for the problem
 - how the container was started (flags, environment variables, mounted volumes etc)
 - any other information that can be helpful

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

## TAGs

This image contains the following versions of java, the container names are
nimmis/alpine-java:<tag> where tag is

| Tag    | OpenJDK version | size |
| ------ | -------------- | ---- |
| latest |  Oracle Java version 8 JRE  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java.svg)](https://microbadger.com/images/nimmis/alpine-java "Get your own image badge on microbadger.com") | 
| openjdk-7-jdk |  OpenJDK Java version 7 JDK  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:openjdk-7-jdk.svg)](https://microbadger.com/images/nimmis/alpine-java:openjdk-7-jdk "Get your own image badge on microbadger.com") |
| openjdk-7-jre |  OpenJDK Java version 7 JRE  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:openjdk-7-jre.svg)](https://microbadger.com/images/nimmis/alpine-java:openjdk-7-jre "Get your own image badge on microbadger.com") |
| openjdk-8-jdk |  OpenJDK Java version 8 JDK  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:openjdk-8-jdk.svg)](https://microbadger.com/images/nimmis/alpine-java:openjdk-8-jdk "Get your own image badge on microbadger.com") |
| openjdk-8-jre |  OpenJDK Java version 8 JRE  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:openjdk-8-jre.svg)](https://microbadger.com/images/nimmis/alpine-java:openjdk-8-jre "Get your own image badge on microbadger.com") |
| oracle-8-jdk |  Oracle Java version 8 JDK  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:oracle-8-jdk.svg)](https://microbadger.com/images/nimmis/alpine-java:oracle-8-jdk "Get your own image badge on microbadger.com") |
| oracle-8-jre |  Oracle Java version 8 JRE  | [![](https://images.microbadger.com/badges/image/nimmis/alpine-java:oracle-8-jre.svg)](https://microbadger.com/images/nimmis/alpine-java:oracle-8-jre "Get your own image badge on microbadger.com") |
Example to run a container with OpenJDK version 7 JDK

	docker run -d nimmis/alpine-java:openjdk-7-jdk

