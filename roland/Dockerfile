FROM ubuntu
MAINTAINER roland@gilt.com

# basic stuff
RUN apt-get -y update
RUN apt-get -y install emacs23
RUN apt-get -y install git
RUN apt-get -y install wget
RUN apt-get -y install curl

# install java
RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get -y install python-software-properties
RUN add-apt-repository -y ppa:webupd8team/java
RUN apt-get -y update
RUN apt-get -y install oracle-java7-installer

# install scala
RUN wget http://www.scala-lang.org/files/archive/scala-2.10.1.tgz
RUN tar zxf scala-2.10.1.tgz
RUN mv scala-2.10.1 /usr/share/scala
 
RUN ln -s /usr/share/scala/bin/scala /usr/bin/scala
RUN ln -s /usr/share/scala/bin/scalac /usr/bin/scalac
RUN ln -s /usr/share/scala/bin/fsc /usr/bin/fsc
RUN ln -s /usr/share/scala/bin/scaladoc /usr/bin/scaladoc
RUN ln -s /usr/share/scala/bin/scalap /usr/bin/scalap

# install sbt 
RUN wget http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.12.3/sbt.deb
RUN dpkg -i sbt.deb
RUN apt-get update
RUN apt-get -y install sbt