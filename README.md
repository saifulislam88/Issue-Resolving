




[Rabbitmq](#Rabbitmq)
[Issue 1:** Unable to start rabbitmq-server on Ubuntu 22.04](#issue-1-unable-to-start-rabbitmq-server-on-ubuntu-2204)




##Rabbitmq

### **Issue 1:** Unable to start rabbitmq-server on Ubuntu 22.04

I faced this issue while installing rabbitmq-server, while I was installing Openstack.Update hostfile with exact hostname which already given for loopback address. The work around for me and the solution to this problem is given as follows.

```sh
$ hostname
$ sudo vim /etc/hosts
$ 127.0.0.1 <hostname>
$ sudo service rabbitmq-server start
```
