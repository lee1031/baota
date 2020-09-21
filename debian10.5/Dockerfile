FROM debian:10.5

LABEL maintainer="lee1031 <ligangmingx@gmail.com>"

RUN sed -i 's#http://deb.debian.org#http://mirrors.163.com#g' /etc/apt/sources.list \
    && apt-get update \
    && apt-get install -y apt-utils \
    && apt-get install -y curl \
    && apt-get install wget -y \
    && apt-get install procps -y \
    && apt-get install ufw -y \
    && apt-get install dialog -y \
    && apt-get install sshd -y \
    && wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh \
    && echo y|bash install.sh

EXPOSE 8888