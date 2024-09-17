




[Rabbitmq](#Rabbitmq)
- [Issue-"1":Unable to start rabbitmq-server on Ubuntu 22.04](#issue-1-unable-to-start-rabbitmq-server-on-ubuntu-2204)


Every SRE/DevOps or Infra engineer should have knowledge of Networking troubleshoot likes below core parts.

1.**Network latency issues**/
2.**Routing problems**/
3.**DNS resolution issues**/
4.**Proxy issues etc**/
5.**Firewall and Security Group Issues**/

## Rabbitmq

### **Issue 1:** Unable to start rabbitmq-server on Ubuntu 22.04

I faced this issue while installing rabbitmq-server, while I was installing Openstack.Update hostfile with exact hostname which already given for loopback address. The work around for me and the solution to this problem is given as follows.

```sh
$ hostname
$ sudo vim /etc/hosts
$ 127.0.0.1 <hostname>
$ sudo service rabbitmq-server start
```
