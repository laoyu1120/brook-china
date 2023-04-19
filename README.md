# brook-china
## 国内服务器可用脚本
# 转载自 https://maobuni.com/2022/01/17/brook-iptables-ddns/


iptables是一款非常强大的防火墙管理工具，同样支持端口转发，同时也支持端口段转发<BBR对于iptables不起作用的>

brook脚本流量转发，可转发TCP/UDP流量，支持动态域名转发，不支持端口段转发，可以自行配置brook.conf（/usr/local/brook-pf/brook.conf）运行。

推荐使用brook或者haproxy(不支持UDP流量)。

其他端口转发工具：nginx，gost，ehco，socat，realm（https://github.com/seal0207/EasyRealM）

## Iptables端口转发/流量转发脚本

**国内可用：**

```perl
wget --no-check-certificate -qO natcfg.sh http://www.arloor.com/sh/iptablesUtils/natcfg.sh && bash natcfg.sh
```
**国外可用：**
```perl
wget --no-check-certificate -qO natcfg.sh https://raw.githubusercontent.com/arloor/iptablesUtils/master/natcfg.sh && bash natcfg.sh
```
#卸载
```perl
wget --no-check-certificate -qO uninstall.sh https://raw.githubusercontent.com/arloor/iptablesUtils/master/dnat-uninstall.sh && bash uninstall.sh
```

**使用：**

![Brook/iptables端口转发一键管理脚本/国内可用/支持DDNS](https://maobuni.com/wp-content/uploads/2022/01/image-13-1024x389.png)

来源：https://github.com/arloor/iptablesUtils

## Brook端口转发/流量转发脚本

**For RHEL / CentOS:**

```lua
yum install bind-utils -y && yum install wget -y && wget https://raw.githubusercontent.com/ECIAP/brook/master/brook-pf-mod.sh && chmod +x brook-pf-mod.sh && bash brook-pf-mod.sh
```

**For Debian / Ubuntu:**

```csharp
apt-get install dnsutils -y && sudo apt-get install wget -y && wget https://raw.githubusercontent.com/ECIAP/brook/master/brook-pf-mod.sh && chmod +x brook-pf-mod.sh && bash brook-pf-mod.sh
```

**对于v20200801以及之前版本可以使用：**

```csharp
wget https://raw.githubusercontent.com/NewCheung/brook/master/brook-pf-mod.sh && bash brook-pf-mod.sh
 #管理界面之后手动输入版本号，如：
v20200801
```

来源：https://github.com/ECIAP/brook

## **Brook国内服务器可用脚本:**
#直接安装v20200801版本
本站提供，解决国内机器与github链接不佳

centos提前安装：
```csharp
yum install bind-utils -y
```
debian提前安装：
```csharp
apt-get install dnsutils -y
```

```csharp
wget http://download.maobuni.com/brook/brook-pf-mod.sh
bash brook-pf-mod.sh
```
