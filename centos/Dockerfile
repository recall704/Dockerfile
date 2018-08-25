FROM centos:7.4.1708

LABEL author="recall704"
LABEL email="tk657309822@gmail.com"

ENV TZ=Asia/Shanghai
ENV LC_ALL=zh_CN.utf8

RUN set -ex \ 
    rm -f /etc/yum.repos.d/*.repo && \
    curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo && \
    curl -o /etc/yum.repos.d/epel.repo http://mirrors.aliyun.com/repo/epel-7.repo && \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo '$TZ' > /etc/timezone && \
    localedef -c -f UTF-8 -i zh_CN zh_CN.utf8
