# mesos-master

[![Join the chat at https://gitter.im/mesoscloud/mesos-master](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mesoscloud/mesos-master?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Apache Mesos is a cluster manager that provides efficient resource isolation and sharing across distributed applications, or frameworks.

## centos

[![](https://badge.imagelayers.io/mesoscloud/mesos-master:0.22.1-centos-7.svg)](https://imagelayers.io/?images=mesoscloud/mesos-master:0.22.1-centos-7)

Usage example:

```
docker run -d \
-e MESOS_ZK=zk://master-1:2181,master-2:2181,master-3:2181/mesos \
-e MESOS_QUORUM=2 \
-e MESOS_IP=10.0.0.123 \
-e MESOS_HOSTNAME=10.0.0.123 \
--name mesos-master --net host --restart always mesoscloud/mesos-master:0.22.1-centos-7
```

*What's going on here?*

- We are specifying a quorum of ZooKeeper nodes
- `MESOS_IP` is optional, use it if you have a private interface and you want Mesos to only listen on it
- `MESOS_HOSTNAME` is optional, use it if you don't have name resolution setup, this is most noticeable when the Mesos UI does an external redirect to the current leader
- We're using `host` networking.  One advantage of this is that `localhost` is the same for all `--net host` containers.  We are not concerned about port conflicts for non app containers.
- `--restart always` will ensure that your container starts on boot and restarts on failure

## ubuntu

[![](https://badge.imagelayers.io/mesoscloud/mesos-master:0.22.1-ubuntu-14.04.svg)](https://imagelayers.io/?images=mesoscloud/mesos-master:0.22.1-ubuntu-14.04)
