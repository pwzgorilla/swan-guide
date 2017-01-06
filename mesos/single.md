# 单master安装(单机版)

## Centos 7.x

添加repo
```
# yum install http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm
```
安装组件
```
# yum install docker mesosphere-zookeeper mesos -y
```

设置mesos
```
# echo 'docker,mesos' > /etc/mesos-slave/containerizers
# echo '5mins' > /etc/mesos-slave/executor_registration_timeout
# echo '$IPADDR' > /etc/mesos-master/hostname
# echo '$IPADDR' > /etc/mesos-slave/hostname
```
其中`IPADDR`为本机可外部访问的地址.

设置防火墙
```
firewall-cmd --permanent --zone=public --add-port=5050/tcp # mesos-master
firewall-cmd --permanent --zone=public --add-port=5051/tcp # mesos-slave
firewall-cmd --reload
```

启动服务
```
for SERVICES in docker zookeeper mesos-master mesos-slave; do
    systemctl enable $SERVICES
    systemctl restart $SERVICES
done
```




