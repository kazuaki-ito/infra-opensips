#https://hub.docker.com/_/centos/
FROM centos:7

RUN yum -y install epel-release && \
    yum -y update               && \
    yum -y clean all
RUN yum -y install wget make gcc gcc-c++ bison which flex lynx libxslt ncurses-devel

WORKDIR /tmp

RUN wget http://opensips.org/pub/opensips/2.3.x/opensips-2.3.1.tar.gz
RUN tar zxvf opensips-2.3.1.tar.gz

WORKDIR /tmp/opensips-2.3.1
RUN make all && make install

CMD /sbin/init