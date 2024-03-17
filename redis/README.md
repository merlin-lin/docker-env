## docker-compose安装redis

> config中redis.conf为redis运行配置，根据个人情况修改


## 常用配置项及含义
```
# 这行要注释掉，解除本地连接限制
bind 0.0.0.0

# 默认 yes，如果设置为 yes，则只允许在本机的回环连接，其他机器无法连接。
protected-mode no

# 默认 no 为不守护进程模式，docker 部署不需要改为 yes，docker run -d 本身就是后台启动，不然会冲突
daemonize no

# 设置密码
requirepass 123456

# 持久化 (另外还有一个配置是aof文件的文件名，有需要的话也要更改)
appendonly yes
```

## 启动容器
```shell
docker-compose up -d
```
