# 三master模式

```
sudo bin/swan --mesos-master=127.0.0.1:5050\
              --cluster=127.0.0.1:9999,127.0.0.1:9998,127.0.0.1:9997\
              --raftid=1\
              --raft-cluster=http://127.0.0.1:2111,http://127.0.0.1:2112,http://127.0.0.1:2113\
              --data-dir=./data/
```
```
sudo bin/swan --mesos-master=127.0.0.1:5050\
              --cluster=127.0.0.1:9999,127.0.0.1:9998,127.0.0.1:9997\
              --raftid=1\
              --raft-cluster=http://127.0.0.1:2111,http://127.0.0.1:2112,http://127.0.0.1:2113\
              --data-dir=./data/
```
```
sudo bin/swan --mesos-master=127.0.0.1:5050\
              --cluster=127.0.0.1:9999,127.0.0.1:9998,127.0.0.1:9997\
              --raftid=1\
              --raft-cluster=http://127.0.0.1:2111,http://127.0.0.1:2112,http://127.0.0.1:2113\
              --data-dir=./data/
```


参数说明:
    详见[参数说明](explain.md)
