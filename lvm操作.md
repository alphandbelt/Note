# LVM

## 删除lv时出现被占用的情况

### 执行脚本查找与该lv相关的进程

```sh
for i in  /proc/[0-9]* ; do echo $i >> /tmp/mountinfo ;  \ grep -q "/dev/mapper/test-vg-test-storage" $i/mountinfo ; echo $? >> /tmp/mountinfo ; done
```

### 查看

```sh
grep -B 1 '^0$' /tmp/mountinfo
```

