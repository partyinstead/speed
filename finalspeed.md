---
description: >-
  FinalSpeed是高速双边加速软件,可加速所有基于tcp协议的网络服务,在高丢包和高延迟环境下,仍可达到90%的物理带宽利用率,即使高峰时段也能轻松跑满带宽.
---

# FinalSpeed

## 搭建服务端

```text
rm -f install_fs.sh
```

```text
wget https://raw.githubusercontent.com/partyinstead/speed/master/FinalSpeed/server/install_fs.sh
```

```text
chmod +x install_fs.sh
```

```text
./install_fs.sh 2&gt;&amp;1 | tee install.log
```

### 相关命令：

### 安装完成后可通过查看日志看是否运行

```text
tail -f /fs/server.log
```

### 卸载

```text
sh /fs/stop.sh ; rm -rf /fs
```

### 停止

```text
sh /fs/stop.sh
```

### 重新启动

```text
sh /fs/restart.sh; tail -f /fs/server.log
```

