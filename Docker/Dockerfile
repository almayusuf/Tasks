# Pulls centos 7 image
FROM centos:7



RUN \
#Remove Default packer from Centos
rm -rf /usr/sbin/packer* && \
#Install Telnet
yum install telnet -y    && \
#Install elinks
yum install elinks -y