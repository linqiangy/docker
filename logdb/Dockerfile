FROM ubuntu

RUN sed -i s@/archive.ubuntu.com/@/mirrors.aliyun.com/@g /etc/apt/sources.list \
    && apt-get clean \
    && apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y libmysqlclient-dev python cron psmisc make gcc wget zip tzdata \
    && wget -P /root https://github.com/linqiangy/logdb/archive/master.zip \
    && unzip /root/master.zip -d /root \
    && mv /root/logdb-master /root/logdb \
    && cd /root/logdb/src && make && make install \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure -f noninteractive tzdata