# 单master模式

```
sudo ./bin/swan --zk-path=zk://127.0.0.1:2181/mesos\
                --raftid=1 \
                --raft-cluster=http://127.0.0.1:2111
```
参数说明:
    详见[参数说明](explain.md)
