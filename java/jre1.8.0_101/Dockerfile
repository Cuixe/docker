FROM ubuntu
RUN apt-get update && apt-get install -y iputils-ping
RUN apt-get install -y openssh-server && apt-get install -y openssh-client && service ssh start
RUN apt-get install -y net-tools
RUN wget --no-cookies --no-check-certificate --header "Cookie: oraclelicense=accept-securebackup-cookie" \
	"http://download.oracle.com/otn-pub/java/jdk/8u101-b13/jre-8u101-linux-x64.tar.gz" -O jre-8u101-linux-x64.tar.gz
RUN mkdir -p /usr/local/java/
RUN tar -zxf jre-8u101-linux-x64.tar.gz  && mv jre1.8.0_101 /usr/local/java/
ENV JAVA_HOME=/usr/local/java/jre1.8.0_101 \
    PATH=${PATH}:/usr/local/java/jre1.8.0_101/jre1.8.0_101/bin
RUN ln -s /usr/local/java/jre1.8.0_101/bin/java /usr/local/bin/java
