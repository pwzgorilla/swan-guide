# macvlan配置

创建macvlan网络
```
# docker network create -d macvlan --subnet=192.168.1.0/24 --gateway=192.168.1.1 -o parent=en0.10 -o macvlan_mode=bridge swan
```
如上命令创建了一个IP地址在`192.168.1.1-192.168.1.255`之间的子网，子网名称是`swan`.
`192.168.1.1`一般用于网关地址，`192.168.1.255`一般用于子网广播地址.


