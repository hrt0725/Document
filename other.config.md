# Internet 快捷方式

[https://www.58pic.com/](https://www.58pic.com/)

[百度地图api](https://lbsyun.baidu.com/index.php?title=jspopularGL)

[虚幻引擎5文档](https://docs.unrealengine.com/5.0/zh-CN/)

[Microsoft 文档](https://docs.microsoft.com/zh-cn/)

[Yolov5 详解](https://free.aliyun.com/product/product/ecs/freetrial?utm_content=se_1011426966)

[yolov5 code](https://blog.csdn.net/weixin_43334693/article/details/129460666?spm=1001.2014.3001.5501)

[mixamo](http://www.mixamo.com/)

[byrut.org](https://byrut.org/)

[beigei](http://www.byget.xyz/)

[AKEBI-GC](https://github.com/lwd-temp/Akebi-GC)

# CL

**path**

G:\Program Files\vs_community\Community\VC\Tools\MSVC\14.33.31629\bin\Hostx86\x86

**INCLUDE**

G:\Program Files\vs_community\Community\VC\Tools\MSVC\14.33.31629\include
G:\Windows Kits\10\Include\10.0.19041.0\cppwinrt
G:\Windows Kits\10\Include\10.0.19041.0\shared
G:\Windows Kits\10\Include\10.0.19041.0\ucrt
G:\Windows Kits\10\Include\10.0.19041.0\um
G:\Windows Kits\10\Include\10.0.19041.0\winrt

**LIB**

G:\Program Files\vs_community\Community\VC\Tools\MSVC\14.33.31629\lib\x86
G:\Windows Kits\10\Lib\10.0.19041.0\um\x86
G:\Windows Kits\10\Lib\10.0.19041.0\ucrt\x86
G:\Windows Kits\10\Lib\10.0.19041.0\ucrt_enclave\x64

---

# Wallpapers

计算机\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Wallpapers
C:\Users\LAN\AppData\Local\Packages\Microsoft.Windows.ContentDeliveryManager_cw5n1h2txyewy\LocalState\Assets

---

# CMD

shutdown -s -t 20
shutdown -a
secpol.msc    本地安全策略

---

# VS CODE

**删除插件：**
Users\用户\.vscode         |   %userprofile%

**删除用户信息和缓存信息：**
Users\用户\Appdata\Roaming\code
Users\用户\Appdata\Roaming\Visual Studio Code

---

# VM Ware

**第142行(vm防检测**

monitor_control.disable_directexec = "TRUE"
monitor_control.disable_chksimd = "TRUE"
monitor_control.disable_ntreloc = "TRUE"
monitor_control.disable_selfmod = "TRUE"
monitor_control.disable_reloc = "TRUE"
monitor_control.disable_btinout = "TRUE"
monitor_control.disable_btmemspace = "TRUE"
monitor_control.disable_btpriv = "TRUE"
monitor_control.disable_btseg = "TRUE"
usb_xhci:4.present = "TRUE"
usb_xhci:4.deviceType = "hid"
usb_xhci:4.port = "4"
usb_xhci:4.parent = "-1"

---

# Python

## pip换源

Python pip配置国内清华大学镜像
pypi 镜像使用帮助
pypi 镜像每 5 分钟同步一次。

### 临时使用

pip install -i https://pypi.tuna.tsinghua.edu.cn/simple
中国科学技术大学 : https://pypi.mirrors.ustc.edu.cn/simple
豆瓣：http://pypi.douban.com/simple/
阿里云：http://mirrors.aliyun.com/pypi/simple/
注意，simple 不能少, 是 https 而不是 http

### 永久生效 [命令行配置]

升级 pip 到最新的版本 (>=10.0.0) 后进行配置：
pip install pip -U
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple

### 永久生效 [文件配置]

Linux下，修改 ~/.pip/pip.conf (没有就创建一个文件夹及文件。文件夹要加“.”，表示是隐藏文件夹)
内容如下：
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host=mirrors.aliyun.com

---
