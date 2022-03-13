FROM centos:6.9

ENV PHP_VERSION 5.3.3

RUN sed -i -e "s/^mirrorlist=http:\/\/mirrorlist.centos.org/#mirrorlist=http:\/\/mirrorlist.centos.org/g" /etc/yum.repos.d/CentOS-Base.repo
RUN sed -i -e "s/^#baseurl=http:\/\/mirror.centos.org/baseurl=http:\/\/vault.centos.org/g" /etc/yum.repos.d/CentOS-Base.repo

RUN yum install -y \
    php \
    php-mbstring \
    php-pgsql \
    php-mysql \
    php-gd \
    zip \
    unzip \
    git \
    httpd && \
    yum clean all

RUN mkdir /work_space
WORKDIR /work_space

EXPOSE 80

CMD ["/usr/sbin/apachectl","-DFOREGROUND"]