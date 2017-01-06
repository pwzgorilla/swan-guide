# GO环境配置

#### 安装golang

##### Linux
Ubuntu
```
# apt install golang -y
```

Centos
```
# yum install golang -y 
```

##### MacOs
```
# brew install golang
```

#### 检测是否安装成功
```
# go version 
```
如果出现以下内容，则说明安装成功.
```
go version go1.7.4 darwin/amd64
```

#### 设置GOPATH

```
echo "GOPATH=/usr/local/go" >> ~/.bash_profile
source ~/.bash_profile
```

#### 检测是否设置成功
```
echo $GOPATH
```
如果输出为`/usr/local/go`, 则说明GOPATH配置成功.
