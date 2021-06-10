# 树莓派模型分类-串口收发


## 一.树莓派换源
树莓派换国内软件源（buster版本）
源地址 http://www.raspbian.org/RaspbianMirrors
### 1.sudo nano /etc/apt/sources.list   #修改软件更新源
把原来的源注释，输入
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ buster main contrib non-free rpi
deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ buster main contrib non-free rpi
#输入结束 crtl+o保存 crtl+x退出
### 2.sudo nano /etc/apt/sources.list.d/raspi.list
注释原来的源，输入
deb http://mirrors.ustc.edu.cn/raspberrypi/ buster main ui
deb-src http://mirrors.ustc.edu.cn/raspberrypi/ buster main ui
#输入结束 crtl+o保存 crtl+x退出
### 3.sudo apt-get update&&upgrade

## 二.配置python并安装必要库
设置python3为默认python
1.sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100
2.sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150
 

## 三.配置串口
sudo raspi-config


## 四.设置树莓派开机自启
sudo vim 


## 五.通信协议


