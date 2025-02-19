# 安装

### 安装 mysql8

```
安装mysql
sudo apt install mysql-server
#启动msyql
sudo systemctl start mysql
#开机自启
sudo systemctl enable mysql

#查看用户名密码
sudo cat /etc/mysql/debian.cnf


sudo systemctl status mysql
sudo systemctl start mysql
sudo systemctl stop mysql
sudo systemctl restart mysql

```

#### 修改本地连接密码

```
# 更改密码
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密码';
# 刷新权限
FLUSH PRIVILEGES;
```

#### mysql 8.0以后默认没有"root@%"远程连接账户，修改远程连接密码需要这样做：

```
// MySQL里查看用户信息
use mysql;
select host, user, authentication_string from user;

// 创建用户
create user 'root'@'%' identified by '新密码';

// 授权
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' WITH GRANT OPTION;

// 刷新权限
FLUSH PRIVILEGES;

// 然后还要修改配置文件，先关闭服务再修改
sudo systemctl stop mysql
sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
把bind-address  = 127.0.0.1注释掉，保存文件，重启mysql
```



### 安装redis

```
sudo apt update
sudo apt install redis-server

#启动reids
sudo systemctl status redis-server

#需要远程访问则修改配置文件(修改为以下内容)
cd /etc/redis/redis.conf
修改：bind 127.0.0.1 ::1
改为： bind 0.0.0.0 ::1

修改peotected-mode yes
改为：protected-mode no

#重启
sudo systemctl restart redis-server
```

