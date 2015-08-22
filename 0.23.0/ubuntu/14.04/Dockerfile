FROM ubuntu:14.04

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && \
echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && \
apt-get update && \
apt-get -y install mesos=0.23.0-1.0.ubuntu1404

CMD ["/usr/sbin/mesos-master"]

ENV MESOS_WORK_DIR /tmp/mesos

VOLUME /tmp/mesos
