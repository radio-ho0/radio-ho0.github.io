---
layout: post
title: Linux Tour 
categories: [general, GNU/Linux ]
tags: [ daily ]
fullview: true
---

         以前我认为 使用 LFS 是终极 Linux 高手， 高级水平， 
         用 gentoo， `arch` 是高手，中级水平， 其他(ubuntu , fedora) 初学者。

## ubuntu:

    练习 vim & C 的地方
 我练习C就是用 `ubuntu` and `gcc`， 跟很多人的不同哈哈

现在看来是对， 我装了不知多少次`arch`， 从一开始用cd 装， 而且下了 core 库， 和一部分 extra 库， 一个200多M， 一个 3G多（还没下完啊， 真暴力， 不会看wiki， 愚蠢）， 第一次安装很费劲

先是 vi， 这个混蛋包名很怪(`vi:????????`) 在windows 分区无法识别冒号`:`， 而我是保存在fat分区上， 通过slitaz 的 isomaster制作iso， 最后通过挂载并修改 /etc/pacman.conf, 安装。

- slitaz:
  一个我高三学习 `Linux` 的主要发行版， 另一个是`Tiny core Linux`, 他们都是用 `busybox` ， 嘻嘻( `Debian` 开发出来 太棒了， 另一个对我之后很有用的 `Debian` 开发工具 `minicom` )后来又发现 `picocom` 比 `minicom` 易用)

接着难题就是图形界面， 由于不能联网， 通过我上网下载的 extra 组里的pkg 只有一部分，是不完整(用firefox下载工具， 因为功力经验不够 没想到有 wget这招， 后来亦因为用 `firefox` 下载东西，又是文件损坏……)， 多得舍友给力，在宿舍通过他们的电脑不断下载损坏的pkg， 终于可以一睹 `Arch` 图形界面！这一装用了一年， 后来越来越会安装

安装越来越容易，次数更多了，下次装有图形界面是家里的PC（之前练习是用 ``core.iso ``也就是没 `xorg`)， 家里的PC 本想装 `KDE` 给 john 的， 不知道为何失败， 现在想来可以用 `pacman -S kde` 搞定.

- **给力舍友**:
            明哥 and 副

之后 接着在自己的机子上又搞了一个复习-练习版， 后来许多次重装都是靠它（大功臣！）， 居然当时没装 wpa_supplicant! 我的机子的`arch` 不知重生了多少次。

后来在 ``arch-wiki`` 上看到有其他很多安装方法有 ``chroot`` , 镜像挂载…… 千边万化！

今年上数学建模因为也想有所作为， 根据很久之前在 [solidot](http://www.solidot.org) 上看到有开源的 数学建模软件( ``octave`` )， 决定重装 `arch` 通过 wifi 校园网 4M 新的 `Arch` 重生！

通过那次安装再次感受到联网真爽， 不久又在家里安装一次， 因签名问题始终安装不了， 以为是时间问题（之前因时间的试过证书认证失败后来改过时间又成功，如网页 好像没了 css）， 这次不行。

在倒数第二次去图书外语阅览室时重装一个到u 盘以解决 `arm` 开发难题(后可能版本问题失败),这次 把所有的pkg 保留以作下次签名问题，应对方案(不久前又是证书搞到安装失败)。

七月份在家里装了一个64位到硬盘上， 主要为了娱乐。这次在wiki上看到有 groups 很多安装包都有在一个组里(例如 gcc 在 base-devel……)， 这次xorg 因显卡问题问题搞到，图形界面有问题， 一个 `pacman -S xorg` 神马图形问题搞定！

安装`arch` 大收获之一发现终极的 shell : zsh， 我在`archlivecd` 看到字体 红色跟绿色的man手册深深吸引了我， 一直恋恋不忘， 查了很久原来它是用了[grml-zsh-config](https://grml.org/zsh/)( pacman -S grml-zsh-config) 的配置， 其间我用过 [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh) ，最终还是喜欢grml的， 从此我可以用色彩斑斓的 shell.

* fun:
在用 ``oh-my-zsh`` 是弄出了一个笑话， 我发现 [oh-my-zsh](http://ohmyz.sh/) 有个 `scritp`叫 `upgrade.sh` 之类它是用 `git` 更新， 我用一句 `echo hello ele1000` 替换了， 从此认为 `git` 是个混蛋程序哈哈，大二 学 嵌入式C语言（吭）时， 学习了 `git` 和 `gnugpg`， 那是才真正认识 `git` 。

 haha

## tinycore and slitaz
高三时，语文老师， 笔记本因为一个按键失灵， 带到学校叫我们去破解密码，途中试 `syslinux grub` 不知为何失败， 隔日用蓝牙键盘输入正确密码…… (真郁闷，还费不少心机研究)， 之后突发奇想，用用 linux， 发现都要安装，查了有种叫livecd 的东西， 不用安装的，很多都很大要CD， 这里没光盘更没刻录机！经过长期探寻找到一个叫 Tiny core 的，很小20来M， 先后用 ``syslinux``  写入``(unetbootin``) 去手机 和 内存卡， 千辛万苦可以一赌 ``linux`` 的容貌。很简陋难怪那么小。 感觉回到 win95了。当时打的第一条LINUX 命令 ``ls -> df -> date -> du -> cal ……`` (大二考 linux 我问老师学的linux命令是什么 她的 是 ls ， 我也告诉她我的是 startx.)

平时上课完下课在宿舍在那里间中查linux 命令， 又发现``slitaz (wm: fluxbox)比 tiny core(wm: fvwm)`` 美观 多倍， 也是基于 ``busybox``。功能多了不少 `mplayer sqlite ....`， 从此告别 `tiny core` , 直到大学第一次运行的系统也是 `Slitaz` ， 当时人们看到我打命令 还以为我在编程 哈！ 那是命令， 到大二 很多人学了linux 还这么认为！

## slax
这系统是我用得最久的livecd linux ， 在高二在隆芯实习， 无意上网发现一个可定制的linux(slax 6), 不错， 很帅， 图标美丽极了(到写这篇文章是还上slax 6 论坛 得到 不少技巧包括更改root密码， 新建账号).

时间跳到大一， 用了`ubuntu livecd` 在图书馆 作恶多端的我讨厌`ubuntu`慢, 于是寻找，找到了 `slax7` 发现不错， 试下 `gcc， make`  等工具，一开始配置失败， 找不到， 试下 `slax 6` , 它居然有 `make`  赶紧试下 `gcc` 也有！ 进入图形界面不错， 好像见过， 时隔很久终于想起高二时见过它， 网上那些人有 `toram`  那招， 我回头弄了弄` slax 7(6 太不稳定）toram` 成功， 一直用`toram` 模式， 比 `win7` 快！！

## wm

    gnome fvwm fluxbox xfce kde blackbox awesome i3 ratposion

` gnome` 2005  **John** 的 *Redhat9* 上见过， `startx` 源于此。大学`ubuntu` 12.04 在NGS 电子阅览室用 `Thunder` 在 [163](http://mirrors.163.com) 镜像， 以3.xM/s 下载。(在20#319装过， 也试过x`ubuntu`因屏幕不适应舍弃了)，很慢， 老牛拖车那样， 不过那是学习 C 和vim 的起点。 Thanks for `ubuntu`

fvwm 2011 tinycore 当时看来 挺酷， 曾经大二寒假学过一番， 很难配置，可塑性极高， 最后偷懒上网找了一个大牛的， 修改后使用， 也给slax 装过。 到了很久之后上网查 tinycore 才发现它用 fvwm！

fluxbox 2011 slitaz 比tiny core 的fvwm 帅

xfce 2012 在NGS 的图书馆把 LFS-6.3 刻录在光盘使用发现了这只可爱的老鼠, gvim-7.2, 觉得xfce 短小精悍， 不像 gnome 臃肿恶心。当时还不知可以硬盘引导 LFS (在20#319 上用过一阵子， 因不稳定舍弃， 收获一些经验)。之后的`arch` 就必须装xfce

kde 2013 slax-6

blackbox 2014 slax-7

awesome 2014 `arch`

i3 2014 `arch` 现在就用它

ratposion 2014 `arch` 主要给slax 用， ratposion容易编译多， 依赖少。


## bsd

挺吸引人的， 出名的三兄弟 Netbsd, Openbsd, Freebsd. 而Openbsd 每次发行都有一首歌曲和海报！ 我还会唱过3.7那首 I love to hate my pc!

Freebsd比较高调， Netbsd 听说嵌入式方面超牛， 支持N 多种U。

我曾经把 Netbsd-6.3 x64 刻录到光盘去， 还以为是 x86的！ 怪自己没看清。没linux 那样方便易用， 驱动更少。
