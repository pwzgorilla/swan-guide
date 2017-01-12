# Proxy设计和实现原理
源码地址: [https://github.com/Dataman-Cloud/swan-janitor](https://github.com/Dataman-Cloud/swan-janitor)

# Proxy验证方法
将dns服务地址加在dns配置文件中.
linux的配置文件在/etc/resolv.conf中。
mac可以通过"系统偏好设置"->"网络"->"选择网络"->"高级"->"DNS"， 在DNS服务器中添加dns服务地址，在搜索域中添加域名范域名的支持。如(*.DOMAIN)
```
nameserver $DNS_ADDR
```
然后可以通过curl请求服务:
```
curl 0.app1.user1.cluster1.DOMAIN
```

