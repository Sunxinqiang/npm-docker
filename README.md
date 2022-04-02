# npm 私有库
balabala

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

## 私有库使用
#### 配置
- nrm add inner-npm http://sunxq.top:3005
- nrm use inner-npm

#### 添加用户
需要更改config/config.yaml下的
```shell
# 可注册
auth
    htpasswd
        max_users: 1000
# 不可注册
auth
    htpasswd
        max_users: -1
```
- npm adduser

#### 安装普通包
- npm i xxx

#### 安装内部包/发布包
- npm login
- npm i xxx
- npm publish



## 权限
- @inner/xx  登录后才可以访问
- 其他 不登录也可以访问
- 所有包，登录后才可以发布