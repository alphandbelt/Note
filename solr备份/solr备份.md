# solr备份

## solr安装

### 下载目录

```sh
https://archive.apache.org/dist/lucene/solr/8.9.0/
```

### 解压

```sh
tar -xvzf solr-8.9.0.tar.gz
```

## solr启动

### 简单启动

```sh
/bin/solr start 
```

默认的端口是8983, 启动后在浏览器访问可以看到相关配置

![截图](b7712f50f84488e5cbd198e5c8d3050c.png)

<br/>

## 添加core

```sh
bin/solr create -c core_test1
```

添加完成后在界面上选择创建的core就可以看到相应的信息

![截图](512439e5d78e25edc2f79be65605bfc3.png)

## 删除core

```sh
bin/solr delete -c core_test1 
```

![截图](efddc53926da7d4d9fd4ec7c55f7e25a.png)

<br/>

### solr 查询参数

![截图](013e258eebf1b11502d7982a02c94539.png)