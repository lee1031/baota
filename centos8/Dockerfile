FROM centos:8

LABEL maintainer="lee1031 <ligangmingx@gmail.com>"

RUN yum -y update \
    && yum -y install wget \
    && wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-8.repo \
    && sed -i -e '/mirrors.cloud.aliyuncs.com/d' -e '/mirrors.aliyuncs.com/d' /etc/yum.repos.d/CentOS-Base.repo \
    && yum clean all \
    && yum makecache \
    && yum -y update \
    && yum -y install dbus \
    && yum -y install openssh-server \
    && yum -y install oniguruma \
    && yum -y install epel-release \
    && yum -y install libsodium \
    && wget -O install.sh http://download.bt.cn/install/install_6.0.sh \
    && echo y|sh install.sh

STOPSIGNAL SIGQUIT

EXPOSE 8888