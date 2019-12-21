FROM ubuntu

RUN buildDeps='vim net-tools procps netcat iputils-ping' \
    && sed -i s@/archive.ubuntu.com/@/mirrors.aliyun.com/@g /etc/apt/sources.list \
    && apt-get clean \
    && apt-get update \
    && apt-get install -y $buildDeps \
