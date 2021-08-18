# Redis 安装

## [压缩包下载地址](https://download.redis.io/releases/)

## 单节点安装

### 安装 Redis(将 * 换为你的 redis 版本)

#### 安装

```shell
tar -xzvf *.tar.gz
ln -s * redis
cd redis
make
make install
```

#### 验证安装

```shell
redis-cli -v
```

### 启动 redis

1. 可以自己配置 redis.conf ,如

    ```shell
    cat > redis.conf <<EOF
    port 6379 #redis 监听端口
    logfile /var/log/redis/redis.log #redis 日志文件
    dir /var/lib/redis # redis 指定本地数据库存放目录(即存放持久化文件和日志文件)
    daemonize yes # 是否以守护进程的方式启动
    EOF

    redis-server redis.conf
    ```
2. 检查是否启动成功

    ```shell
    cat /var/run/redis.pid
    ```

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