FROM centos
RUN yum update -y && yum clean all
RUN yum install -y java-1.7.0-openjdk
RUN yum install -y nginx

RUN systemctl start nginx
RUN systemctl enable nginx
EXPOSE 80

