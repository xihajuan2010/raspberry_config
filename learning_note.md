### RaspberryPi树莓派软件源的国内镜像[速度超快]
终于入手树莓派了，这几天开始折腾，免不了要安装好多软件，可是RaspberryPI的默认的官方软件安装源在国外，对于国内的用户来说速度非常慢，本来树莓派CPU就慢，再加上网速慢，实在让人无法忍受，所以决心找个国内的软件源！
功夫不负啊，终于找到一个速度不错的软件源，具体操作方法如下：
编辑软件源配置文件：   sudo vi  /etc/apt/sources.list
直接先把官方源去掉或者前面加#号注释掉，添入以下源：
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/   wheezy main contrib non-free rpi
这个源实际就是中科大的镜像，中科大是国内的Debian官方认可的源镜像，所以稳定性和速度都有保障！
保存退出即可！接下来试试更新体验下速度!
sudo apt-get upgrade
## tsinghua mirrors
```
deb http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ jessie main non-free contrib
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ jessie main non-free contrib
```

### mmodule 
```
lsusb
lsmod
iwconfig
```
### Change passwd
use sudo passwd to active and set password for root account 
```
sudo passwd root
```
### modify default user home directory
```
usermod –d /home/zhouwuxiang
uderadd zhouwuxiang –d /home/zhouwuxiang
```
### linux .bashrc文件修改和生效
每次修改.bashrc后，使用source ~/.bashrc（或者 . ~/.bashrc）

#### /etc/network/interfaces
network interface configuration for ifup and ifdown

### To start/stop/restart  Linux network service:
```
/etc/init.d/networking restart
for systemd based 
systemctl start/stop/restart networking
```