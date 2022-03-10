#Pulls centos 7 image
FROM centos:7

RUN \
#Install Telnet
yum install telnet -y    && \
#Install elinks
yum install elinks -y     && \
#Install wget
yum install wget -y && \
#Install unzip
yum install  unzip -y && \
#Remove Default Centos Packer
unlink /usr/sbin/packer    && \ 
#Install Hashicorp packer
wget https://releases.hashicorp.com/packer/1.8.0/packer_1.8.0_linux_amd64.zip && \
unzip packer_1.8.0_linux_amd64.zip -d /usr/sbin/ && \ 
rm packer*  && \
#Install Hashicorp terraform 1.0 
wget https://releases.hashicorp.com/terraform/1.0.0/terraform_1.0.0_linux_amd64.zip && \
unzip terraform_1.0.0_linux_amd64.zip -d /usr/sbin/ && \
rm terraform*

# Set Labels 
LABEL \
name = "sharedtools" \
centos = "terraform" \
packer_1.8.0 \
terraform_1.0.0 \
 created_by="almayusuf"


#Keep Container running after deployment
CMD [ "/usr/bin/sleep", "infinity" ]