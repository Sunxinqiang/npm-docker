# npm 私有库
balabalba

## 启动
```shell
# 给数据目录可写权限
sudo chown -R 10001:65533 ./
# 启动
docker-compose up -d --build
```

## 查看日志
```shell
docker logs -f  verdaccio
```