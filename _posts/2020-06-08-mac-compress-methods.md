---
layout: post 
title: Mac 文件压缩工具总结
date: 2020-06-08
author: Sesame
tags: [tools, Mac]
comments: true 
---

使用mac的时候需要对文件进行压缩，mac进行文件压缩使用自带的软件功能少，支持的格式也少。使用app store或者其他的
三方压缩软件一般都需要付费。本文对于mac使用cli（命令行工具）进行文件压缩方法的总结。
<!-- more -->

## rar
rar 是一个比较主流的压缩算法（格式），其版权为具体公司所有，其他三方工具如果需要进行rar压缩需要付费，所以很多软件
并不支持rar压缩格式。（尤其是mac，撰写本文缘由也是寻找合适的rar压缩、解压工具）

### rar cli 压缩工具下载
下载地址 [https://www.rarlab.com/download.htm](https://www.rarlab.com/download.htm)
选择合适的「RAR」文件版本下载。（本文撰写时间，需要下载的文件名称为：`RAR 5.91 beta 1 for macOS (64 bit)`）

### 安装(所谓安装，就是将下载下来的文件放在某一个·合适·的位置)
使用「聚焦搜索」（默认的快捷唤出按键为`Command+空格`）输入`Terminal`或者`iterm`
以下命令在Terminal软件中输入
```sh
# # 符号之后为注释，起解释作用不是命令

# 工作目录至刚才下载的「RAR」文件存储的地方，以下命令提供参考
cd ~/Downloads #如有问题，可尝试 cd ~/下载

# 解压缩「RAR」文件
tar -xzvf rarosx-5.9.1b1.tar.gz # tar -xzvf <文件名>

# 工作目录至解压文件内部（如有问题，自行解决）
cd rar # 没有报错就没问题，UNIX哲学

# 将命令放在指定（PATH）路径，以下提供一个一般来说一定有的路径
sudo cp rar /usr/bin # 需要输入系统用户密码，根据需要 /usr/bin 可以换成 /usr/loacl/bin
```

### 使用 rar
```sh
# 使用 rar 进行压缩

# 举例，将 file1，file2, file3 压缩为「压缩包名称.rar」文件
rar a 压缩包名称.rar file1 file2 file3

# 举例，解压「压缩包.rar」文件
rar x 压缩包.rar


# tips（好像有人找不到压缩后的文件，问题本质是不理解路径问题，可以百度「Linux文件路径」进行理解
# 「open . 」命令可以在Terminal软件中直接打开「访达」且访达的目录为当前工作路径
# 「rar」命令输入后可以直接显示 rar 软件的用法，其他rar的使用方式参考该用法
```

## 7z #TODO

### install 
```sh
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brew search 7z  # result p7zip

$ brew install p7zip
```

### usage
```sh
$ 7z --help
```

## gzip, bzip2 #TODO

## zip #TODO
