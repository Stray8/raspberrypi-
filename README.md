# 树莓派模型分类-串口收发


## 一.树莓派换国内软件源（buster版本）
镜像源地址: http://www.raspbian.org/RaspbianMirrors
```
sudo nano /etc/apt/sources.list   #编辑系统源文件
```

把原来的源注释，输入
```
deb http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ buster main contrib non-free rpi
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ buster main contrib non-free rpi
#输入结束 crtl+O保存 crtl+X退出
```

```
sudo nano /etc/apt/sources.list.d/raspi.list  #修改系统源
```

注释原来的源，输入
```
deb http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui
deb-src http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui
#输入结束 crtl+o保存 crtl+x退出
```

```
sudo apt-get update&&upgrade         #完成源的更新软件包索引
```

```
                                     #修改pip源
```

## 二.配置python并安装必要库
设置python3为默认python
```
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150
 ```

## 三.配置串口
```
sudo raspi-config
```

## 四.设置树莓派开机自启
```
sudo vim /etc/rc.local
```

## 五.通信协议
包头    |  校验和   |  包尾 ｜ 数据
:-----  |-------: |:-----:
0x5a    | 内容2    |  0xa5 ｜ 0x00

