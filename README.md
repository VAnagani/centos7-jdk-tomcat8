# centos7-jdk-tomcat8
Docker image with CentOS7-JDK,Tomcat8

What is CentOS?
CentOS (abbreviated from Community Enterprise Operating System) is a Linux distribution that attempts to provide a free, enterprise-class, community-supported computing platform which aims to be functionally compatible with its upstream source, Red Hat Enterprise Linux.




What is Tomcat?
Apache Tomcat is an open source web server and servlet container developed by the Apache Software Foundation (ASF). Tomcat implements the Java Servlet and the JavaServer Pages (JSP) specifications from Oracle, and provides a "pure Java" HTTP web server environment for Java code to run in. In the simplest config Tomcat runs in a single operating system process. The process runs a Java virtual machine (JVM). Every single HTTP request from a browser to Tomcat is processed in the Tomcat process in a separate thread.



How to use this image?
Pull the image using the command

docker pull vanagani/centos7-jdk-tomcat8
Run the image in container using the command

docker run -d -p 8090:8080 vanagani/centos7-jdk-tomcat8 /start.sh
Host Manager, accessible via the link

http://server_IP_address:8080/host-manager/html/
Access the homepage entering below URL in web browser:

http://server_IP_address:8080
Manager App accessible via the link

 http://server_IP_address:8080/manager/html
Login Credentials to access manager page:
Username : admin
Password : password

Tomcat Environment :

Environment=JAVA_HOME=/usr/lib/jvm/jre
Environment=CATALINA_PID=/opt/tomcat/temp/tomcat.pid
Environment=CATALINA_HOME=/opt/tomcat
Environment=CATALINA_BASE=/opt/tomcat
Environment='CATALINA_OPTS=-Xms512M -Xmx1024M -server -XX:+UseParallelGC'
Environment='JAVA_OPTS=-Djava.awt.headless=true 
-Djava.security.egd=file:/dev/./urandom'
Deploy your web service using manager page:


Supported Docker versions
This image is officially supported on Docker version 1.10.1.

Support for older versions (down to 1.6) is provided on a best-effort basis
