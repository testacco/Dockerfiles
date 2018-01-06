FROM centos
RUN yum update -y && yum clean all
RUN yum install -y java-1.7.0-openjdk

RUN yum -y install tomcat
sudo vi /usr/share/tomcat/conf/tomcat.conf
JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom -Djava.awt.headless=true -Xmx512m -XX:MaxPermSize=256m -XX:+UseConcMarkSweepGC"

RUN yum -y install tomcat-webapps tomcat-admin-webapps 
RUN vi /usr/share/tomcat/conf/tomcat-users.xml

<tomcat-users>
    <user username="admin" password="password" roles="manager-gui,admin-gui"/>
</tomcat-users>

RUN systemctl start tomcat
RUN systemctl restart tomcat
RUN systemctl enable tomcat


EXPOSE 80

