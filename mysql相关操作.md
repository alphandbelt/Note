# MySQL操作记录

## 安装mariadb到Windows

### 下载地址

```html
https://mariadb.com/downloads/
```

### 文档

```
https://mariadb.com/kb/en/installing-mariadb-msi-packages-on-windows/
```

***

## 卸载mariadb安装MySQL（centos）

### 下载rpm包

```html
下载rpm包 https://dev.mysql.com/downloads/repo/yum/ 
```

### 执行命令卸载mariadb

```sh
rpm -qa | grep Maria*
```

```sh
yum -y remove Maria*
```

```sh
rm -rf /var/lib/mysql
```

### 安装

#### 参考链接

```sh
https://dev.mysql.com/doc/refman/5.7/en/linux-installation-yum-repo.html
```

#### rpm包下载地址

```sh
 https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm
```

#### 本地安装

```sh
sudo yum localinstall mysql80-community-release-el7-3.noarch.rpm
```

#### 关闭默认的Mysql的模块

```sh
sudo yum module disable mysql
```

#### 安装mysql

```sh
sudo yum install mysql-community-server
```

#### 启动服务

```sh
sudo service mysqld start
```

#### 查看默认密码

```sh
sudo grep 'temporary password' /var/log/mysqld.log
```

#### 登录并且修改密码

```sh
mysql -ub root -p
ALTER USER 'root'@'localhost' IDENTIFIED BY 'NEWPASSWD';
```

<br/>

***

## 修改mysql的数据目录

```bash
https://blog.csdn.net/ruanhao1203/article/details/52242438
```

