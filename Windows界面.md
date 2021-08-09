## windows将是将改成按秒显示

![image-20210809134505395](https://raw.githubusercontent.com/alphandbelt/Note/main/img/image-20210809134505395.png)

### 管理员cmd执行

```bash
reg add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced /v "ShowSecondsInSystemClock" /t reg_dword /d 1 /f >nul 2>nul1
```

### 重启资源管理器

![image-20210809134345150](https://raw.githubusercontent.com/alphandbelt/Note/main/img/image-20210809134345150.png)

* 在任务管理器里面找到windows资源管理器，然后右键点击重启服务即可