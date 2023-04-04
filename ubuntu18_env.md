# ubuntu 18.04 初装软件配置

## 1.设置root密码,进行密码设置

```shell
sudo passwd
```

验证root是否设置成功

```shell
su root
```

输入密码后确认是否可以切换到root账户，用exit退出root账户

## 2.更换软件源列表

备份初始软件源列表

```shell
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
```

编辑软件源列表

```shell
sudo gedit /etc/apt/sources.list
```

删除sources.list里面所有东西，放入以下内容:清华源

```Text
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse
deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
```

终端输入

```shell
sudo apt update
```

更新，这一命令会更新内核，最好只在刚装上系统时运行一次

```shell
sudo apt upgrade
```

## 3.安装必备软件

### 3.1 输入法

<https://blog.csdn.net/weiguang102/article/details/122522271>

### 3.2 音视频播放器 VLC

- 通过ubuntu软件商店直接安装

### 3.3 格式转换/解码器 ffmpeg

```shell
sudo apt-get install ffmpeg
```

### 3.4 浏览器 Firefox

- 通过ubuntu软件商店直接安装

### 3.5 vscode

- 通过ubuntu软件商店直接安装

### 3.6 vim

```shell
sudo apt install vim
```

### 3.7 文件传输

微信传输助手网页版

### 3.8 wps

- 通过ubuntu软件商店直接安装

### 3.9 代码比对工具 meld

```shell
sudo apt-get install meld
```

### 3.10 邮箱 thunderbird

- 通过ubuntu软件商店直接安装

### 3.11 串口工具 minicom

```shell
sudo apt-get install minicom
```

### 3.12 ssh

- 系统自带

### 3.13 ifconfig

```shell
sudo apt install net-tools
```

### 3.14 git gitk

```shell
sudo apt install git
sudo apt install gitk
```

### 3.15 gcc4.9 g++4.9

<https://blog.csdn.net/weixin_43876206/article/details/100923785>

使用命令修改源

```shell
sudo gedit /etc/apt/sources.list
```

在打开的文件中的最后两行加上如下代码

```Text
deb http://dk.archive.ubuntu.com/ubuntu/ xenial main
deb http://dk.archive.ubuntu.com/ubuntu/ xenial universe
```

使用命令更新源

```shell
sudo apt-get update
```

使用命令安装gcc和g++

```shell
sudo apt install g++-4.9
sudo apt install gcc-4.9
```

添加版本到update-alternatives

```shell
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.9 1
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.9 1
```

配置 gcc 默认指向 gcc-4.9
配置 g++ 默认指向 g++-4.9

```shell
sudo update-alternatives --config gcc
sudo update-alternatives --config g++
```

### 3.16 python

- 系统自带

python -> python2.7

python3 -> python3.6

### 3.17 ftp

- 系统自带

### 3.18 make

```shell

sudo apt-get install make
```

### 3.19 cmake

```shell
sudo apt install cmake
```

### 3.20 百度网盘

到百度网盘下载deb安装包:

<https://pan.baidu.com/download#linux>

安装deb包

```shell
sudo dpkg -i ~/Downloads/baidunetdisk_4.17.7_amd64.deb
```

### 3.21 截图工具

- 系统自带:ScreenShot

### 3.22 包管理工具 新立得(Synaptic)

```shell
sudo apt-get install synaptic

sudo synaptic
```

### 3.23 doxygen

```shell
sudo apt-get install doxygen
```

### 3.24 indicator-sysmonitor

```shell
sudo add-apt-repository ppa:fossfreedom/indicator-sysmonitor
sudo apt-get update
sudo apt-get install indicator-sysmonitor
indicator-sysmonitor &
```

<https://www.cnblogs.com/hjw1/p/7901048.html>

### 3.25 drawio

```shell
sudo snap install drawio
```

### 3.26 valgrind

```shell
sudo apt-get install valgrind
```

### 3.27 adb

```shell
sudo apt install adb
```

### 3.28 Typora

链接: <https://pan.baidu.com/s/1__W-a-LnZMLl4FLRFBchRg>
提取码: 3euu
下载双击deb安装即可

### 3.29 录屏软件 Kazam

- 通过ubuntu软件商店直接安装

### 3.30 tree

```shell
sudo apt install tree
```

### 其他

- 向日葵

- nvidia显卡驱动

- 抓包工具：wireshark

- ImageJ

- mysql

## 4.配置

### 4.1 配置自启应用

<https://blog.csdn.net/qq_39902475/article/details/108238901>

### 4.2 配置git

参考配置部分内容:

<https://blog.csdn.net/qq_34160841/article/details/104838269>

```shell
git config --global user.name liaochengliang
git config --global user.email 2789094390@qq.com
git config --list
```

### 4.3 配置ssh

```shell
ssh-keygen -t rsa -C "2789094390@qq.com"
```

提示的地方直接按Enter

### 4.4 gcc，g++，python版本管理

- update-alternatives

<https://blog.csdn.net/qq_42608626/article/details/106249986>

### 4.5 vscode插件管理

- C/C++

- Remote-SSH

- Python

- markdownlint

- Markdown Preview Enhanced

- CMake

### 4.6 vscode配置

#### 4.6.1 Vs Code使用 - 保存时自动删除多余空格

<https://blog.csdn.net/jackailson/article/details/100056064>

### 4.7 Java环境

```shell
sudo apt-get install default-jre
sudo apt-get install default-jdk
```

- 配置Java环境变量
<https://blog.csdn.net/DovSnier/article/details/108512664>
