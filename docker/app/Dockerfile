FROM centos:7

ENV PHP_VERSION 5.3.3

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