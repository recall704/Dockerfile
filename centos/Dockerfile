FROM centos:7.4.1708

LABEL author="recall704"
LABEL email="tk657309822@gmail.com"

ENV TZ=Asia/Shanghai

RUN rm -rf /etc/yum.repo.d/*

COPY Centos-Base.repo /etc/yum.repo.d/Centos-Base.repo
COPY epel.repo /etc/yum.repo.d/epel.repo
COPY resolv.conf /etc/resolv.conf

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo '$TZ' > /etc/timezone && \
    sed -i -e '/^enabled/ s/1/0/' /etc/yum/pluginconf.d/fastestmirror.conf &&  \
    localedef -c -f UTF-8 -i zh_CN zh_CN.utf8 

ENV LANG=zh_CN.UTF-8 \
    LANGUAGE=zh_CN:zh \
    LC_ALL=zh_CN.UTF-8
