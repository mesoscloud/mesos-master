# mesos-master

[![Join the chat at https://gitter.im/mesoscloud/mesoscloud](https://badges.gitter.im/mesoscloud/mesoscloud.svg)](https://gitter.im/mesoscloud/mesoscloud?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Mesos

http://mesos.apache.org/

## CentOS

[![](https://badge.imagelayers.io/mesoscloud/mesos-master:0.28.1-centos-7.svg)](https://imagelayers.io/?images=mesoscloud/mesos-master:0.28.1-centos-7)

e.g.

```
docker run -d \
-e MESOS_HOSTNAME=ip.address \
-e MESOS_IP=ip.address \
-e MESOS_QUORUM=2 \
-e MESOS_ZK=zk://node-1:2181,node-2:2181,node-3:2181/mesos \
--name mesos-master --net host --restart always mesoscloud/mesos-master:0.28.1-centos-7
```

Set environment variable `SECRET` to enable framework and slave authentication.

## Ubuntu

[![](https://badge.imagelayers.io/mesoscloud/mesos-master:0.28.1-ubuntu-14.04.svg)](https://imagelayers.io/?images=mesoscloud/mesos-master:0.28.1-ubuntu-14.04)

e.g.

```
docker run -d \
-e MESOS_HOSTNAME=ip.address \
-e MESOS_IP=ip.address \
-e MESOS_QUORUM=2 \
-e MESOS_ZK=zk://node-1:2181,node-2:2181,node-3:2181/mesos \
--name mesos-master --net host --restart always mesoscloud/mesos-master:0.28.1-ubuntu-14.04
```

Set environment variable `SECRET` to enable framework and slave authentication.
