FROM centos:latest

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
RUN yum install policycoreutils -y
RUN yum install -y passwd
RUN adduser apache; echo "1234" | passwd apache --stdin; usermod -aG wheel apache
RUN yum install sudo -y


# Docker Scan relies upon access to Snyk, a third party provider, do you consent to proceed using Snyk? (y/N)