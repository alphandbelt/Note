## ubuntu修改交换分区后启动慢解决
### 适用于修改后的磁盘uuid不一致的情况
* 使用lsblk -f 查看磁盘对应的交换分区

  ![圖片](https://user-images.githubusercontent.com/28209685/135009999-ca9774cd-160c-4e2e-a6b2-e84d8323c4e2.png)
* 编辑/etc/fstab将交换分区对应的uuid改为上一步查询出来的

  ![圖片](https://user-images.githubusercontent.com/28209685/135010203-85dde139-aeab-4890-a3e3-68f7c0ab0ce9.png)
  
### 如何排查出这个问题
* 首先查看启动时的job,找到waiting的那一项,看看具体是哪个,然后再进行具体的排查
  ```bash 
  systemctl list-jobs
