# eolinker4.0-docker

拉取dev测试分支 
```bash
#拉取代码
git clone  -b dev https://github.com/KaapoMarcus/eolinker4.0-docker.git
#给文件目录赋权限
chmod -R 777 eolinker4.0-docker
```
```bash
#在此文件上可以查看数据库连接信息，填写外网ip 端口号默认3306
www\server\Server\Web\Module\InstallModule.class.php
```
## 启动

```bash

docker-compose build

docker-compose up -d

```


## 请求

> http://localhost:24285

## 安装配置

TODO...
