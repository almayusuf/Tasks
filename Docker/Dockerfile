#Pulls centos 7 image
FROM centos:7

RUN \
#Install Telnet
yum install telnet -y    && \
#Install elinks
yum install elinks -y     && \
#Install wget and unzip
yum install wget unzip -y && \
#Remove Default Centos Packer
unlink /usr/sbin/packer     
#Install Hashicorp packer

#Keep Container running after deployment
CMD [ "/usr/bin/sleep", "infinity" ]