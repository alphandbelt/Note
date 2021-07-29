# Nats

## 使用nats-streaming-server

### 创建表

#### 从链接下载数据库文件

```sh
https://github.com/nats-io/nats-streaming-server/blob/master/scripts/mysql.db.sql
```

#### 执行命令安装

```powershell
mysql -u nss -p -D nss_db -e "$(cat ./scripts/mysql.db.sql)"
```

### 创建nss_db数据库

```sh
mysql -u root -e "CREATE USER 'nss'@'localhost' IDENTIFIED BY 'password'; \
GRANT ALL PRIVILEGES ON *.* TO 'nss'@'localhost'; CREATE DATABASE nss_db;"
```

#### Note

- 如果数据库中已经存在nss_db数据库，先删除并刷新权限。

### 执行

```sh
nats-streaming-server -store sql -sql_driver mysql -sql_source "nss:password@/nss_db?readTimeout=5s&writeTimeout=5s" 
```

