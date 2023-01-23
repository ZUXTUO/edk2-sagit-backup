# 只是备份！！！

# 骁龙835(MSM8998)的EDK2 UEFI固件

**在编译该项目前，请确定你有一定的Linux常识，以下步骤已经是最简单的方法，如果你看不懂，那么请使用Releases中的编译成品**

## 资源

[Telegram英语交流群](https://t.me/joinchat/MNjTmBqHIokjweeN0SpoyA)

[Discord英语交流群](https://discord.gg/XXBWfag)

QQ中文交流群: 

主群：697666196 (已满，人数小于1900后开放)  
二群：996450026        
摸鱼专用群：737223105（需具有一定知识储备并正确回答入群问题）     
情感交流群：991796138（仅限邀请）       
核心管理群：766060878（暂不开放）     

[Windows 驱动](https://github.com/edk2-porting/WOA-Drivers)

[项目官网](https://renegade-project.org/)

[项目论坛](https://forum.renegade-project.org/)


## 警告

**请勿尝试移植到任何索尼和谷歌设备上**

**你的UFS会被清空!!!**

## 已支持的设备

1. 小米手机6 (sagit)

## 依赖

Windows/MacOS/其它Linux发行版:

手动安装Docker或者使用Ubuntu虚拟机

Ubuntu 20.04:

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential uuid-dev iasl git nasm gcc-aarch64-linux-gnu abootimg python3-distutils python3-pil python3-git gettext
```

## 构建

**不建议使用Ubuntu 18.04版本，请使用Ubuntu 20.04或以上版本**

1.克隆此项目

```bash
git clone https://github.com/ZUXTUO/edk2-sagit-backup.git
cd edk2-sagit-backup
```

2.编译此项目

```bash
bash build.sh --device sagit
```

3.启动镜像

```bash
fastboot boot boot_sagit.img
```
或者
```bash
fastboot flash boot boot_sagit.img
```

另外，你可以将UEFI刷写至recovery分区以实现双重启动。

```bash
fastboot flash recovery boot_sagit.img
```

# 支持：
USB
UFS
显示
触摸
蓝牙

# 不支持：
UEFI按键
WiFi
电池
充电
虚拟化
GPU
LTE
音频
定位
传感器
摄像头
NFC

## 感谢

https://github.com/edk2-porting/edk2-msm8998

https://github.com/lumingyu0423/edk2-MSM8998
