Bootstrap: docker
From: ubuntu:18.04

%environment
PATH=/usr/local/src/bowtie2-2.3.5.1-linux-x86_64:$PATH
export LC_ALL=C.UTF-8
export LANG=C.UTF-8

%post
sed -i "s/archive.ubuntu/de.archive.ubuntu/" /etc/apt/sources.list && \
sed -i "s/security.ubuntu/de.security.ubuntu/" /etc/apt/sources.list && \
apt-get update
apt-get dist-upgrade -y 
apt-get install wget python python3 build-essential unzip git -y 
rm -rf /var/lib/apt/lists/*
mkdir -p /usr/local/src
cd /usr/local/src && \
wget -c https://netix.dl.sourceforge.net/project/bowtie-bio/bowtie2/2.3.5.1/bowtie2-2.3.5.1-linux-x86_64.zip && \
unzip bowtie2-2.3.5.1-linux-x86_64.zip && \
rm bowtie2-2.3.5.1-linux-x86_64.zip

%labels
MAINTAINER BioBox
Version v1.0
