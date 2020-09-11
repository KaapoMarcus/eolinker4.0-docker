# eolinker4.0-docker

拉取prod测试分支 
```bash
#拉取代码
git clone https://github.com/KaapoMarcus/eolinker4.0-docker.git
#给文件目录赋权限
chmod -R 777 eolinker4.0-docker
```
```bash
#在此文件上可以查看数据库连接信息，填写外网ip 端口号默认3306  代码中有  >> 两处3306端口
www\server\Server\Web\Module\InstallModule.class.php
```

## 启动

```bash

docker-compose build

docker-compose up -d

```
```bash
#启动成功之后进入mysql容器设置允许远程登录root
docker exec -it eolinker40-docker_mysql_1 bash
#容器内执行以下命令
mysql -u root -p
#输入初始密码
h9tGyYgsTFP7
#设置root或者其他用户远程登录的密码
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'h9tGyYgstTFP7' WITH GRANT OPTION;
#刷新设置
flush privileges;
```
```bash
#重启docker服务
 systemctl restart docker
```
## 请求

> http://localhost:24285

数据库连接地址填写要访问应用的远程 ip

一步步执行成功后  注册添加的第一个用户是管理员权限

## 安装配置

TODO...
