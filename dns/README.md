# DNS设计和实现原理

# DNS验证方法

+ 范域名支持
```
#dig @DNS_ADDR 0.app1.user1.cluster1.DOMAIN
```
DNS_ADDR为dns服务的ip地址, 例如localhost, 127.0.0.1。

dns的范域名支持与代理服务器proxy配合使用,通过识别DOMAIN，dns可以解析到proxy的地址。
当请求到达proxy时，proxy通过请求的host地址将请求反向代理到实际的服务地址。

+ 服务支持
```
#dig @DNS_ADDR 0.app1.user1.cluster1.DOMAIN srv
```
dns会解析出0.app1.user1.cluster1.DOMAIN服务实际的ip,port.

如果dig之后很久没有结果，请查看53端口是否被占用,命令为:
```
#lsof -i -P|grep 53
```
杀掉占用53端口的服务，然后再使用此dns服务。
