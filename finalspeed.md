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

### 设置服务端口

```text
mkdir -p /fs/cnf/ ; echo 端口号 > /fs/cnf/listen_port ; sh /fs/restart.sh
```

{% hint style="danger" %}
## 默认udp 150和tcp 150 ,由于finalspeed的工作原理,请不要在本机防火墙开放finalspeed所使用的tcp端口.
{% endhint %}

### 设置开机启动

```text
chmod +x /etc/rc.local
```

```text
vi /etc/rc.local
```

加入

```text
sh /fs/start.sh
```

{% hint style="warning" %}
### 还要注意，已经在运行了没有停止情况下重复启动是会报错的，所以最好先停止或者重启。
{% endhint %}

## 软件

> [https://raw.githubusercontent.com/partyinstead/speed/master/FinalSpeed/Client/FinalSpeed.zip](https://raw.githubusercontent.com/partyinstead/speed/master/FinalSpeed/Client/FinalSpeed.zip)

