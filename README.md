# raspberrypi-
单片机发送指令，树莓派识别并串口发送给单片机


# 配置树莓派
一.树莓派换国内软件源（buster版本）
1.sudo nano /etc/apt/sources.list
把原来的源注释,输入
deb (源地址)/raspbian/raspbian/ buster main contrib non-free rpi
deb-src （源地址)/raspbian/raspbian/ buster main contrib non-free rpi
crtl+o保存 crtl+x退出
2.sudo nano /etc/apt/sources.list.d/raspi.list
注释原来的环境，输入
deb (源地址)/raspberrypi/ buster main ui
deb-src (源地址)/raspberrypi/ buster main ui

3.sudo apt-get update&&upgrade


二.设置python3为默认python
1.sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100
2.sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150
 

三.配置串口
sudo raspi-config


