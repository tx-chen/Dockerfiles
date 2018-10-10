# based on Debian 9 with Python 2.7
# Sources: mirrors.cloud.tencent.com
# TimeZone: HongKong

FROM python:2.7-stretch
LABEL maintainer="https://github.com/tx-chen/Dockerfiles.git"

ARG TZ=Asia/Hong_Kong

RUN set -ex \
    && sed 's;http.*//.*debian.org;https://mirrors.cloud.tencent.com;g' -i /etc/apt/sources.list \
    && echo '[global]\nindex-url=https://mirrors.cloud.tencent.com/pypi/simple/\ntrusted-host=mirrors.cloud.tencent.com' > /etc/pip.conf \
    && ln -sf /usr/share/zoneinfo/$TZ /etc/localtime \
    && rm -rf /var/cache/apt/* /root/.cache/pip/*
