---
layout: post
title: 复杂寻线小车的原理及实现
date: 2017-09-06
tag: 博客
---

<h6><img src="https://robotkang-1257995526.cos.ap-chengdu.myqcloud.com/icon/copyright.png" alt="copyright" style="display:inline;margin-bottom: -5px;" width="20" height="20"> 版权声明：本文为博主原创文章，未经博主允许不得转载。
<a target="_blank" href="http://robotkang.cc/2017/09/the-car-of-follow-line/">原文地址：http://robotkang.cc/2017/09/the-car-of-follow-line/ </a>
</h6>
学校的那台[nao机器人]系统版本比较低了，官方慢慢的不支持了，所以我就给它来了一次升级，好在刷机比较成功。不过刷机后机器人开机的时间比较长了，估计是硬件有点跟不上了吧...  现在把升级过程方法记录在这里，大家也可以参考一下~            

1. 机器人刷机的办法一般有两种，第一种是通过choregraph来，先去[官网](https://www.ald.softbankrobotics.com/en)community-source-documentions-NAOQI OS下载你需要的系统镜像文件版本，然后再去chore（连接-高级-更新机器人系统），这种是比较正常的办法~但是有时候机器人系统完全崩溃，想要整个机器人恢复到出厂设置，变成一台全新的机器人，那么就需要用到下面的方法了。
2. 在给机器人刷机恢复至出厂设置前，你需要准备以下几样：<br>
a) NAOQI os<br>
b) Flasher（官网下，下载位置与OS下载位置相同）<br>
c) 大于4G的U盘<br>
3. 下面我们就开始刷机。<br>
第一步，先打开flasher，注意要用管理员权限打开，然后插上U盘，选中你的U盘。<br>
![world](https://robotkang-1257995526.cos.ap-chengdu.myqcloud.com/nao%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%88%B7%E6%9C%BA%E6%96%87%E7%AB%A0/2.png)
第二步，选中U盘之后，勾选 Factory reset，这一步一定要勾选，因为只有这样才能把原本的系统完全抹去。<br>
第三步，点击`write`，开始刻写镜像文件OS至U盘。<br>
`在这一步骤，很可能出现错误，显示在记得U盘里已经有了什么driver什么的，出现这一错误的原因是因为U盘已经被windows系统装上了驱动，需要清除，所以我们给它清除一下即可。
点击电脑左下角“开始”，输入“diskpart”，这个是Windows自带的。`
![world](https://robotkang-1257995526.cos.ap-chengdu.myqcloud.com/nao%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%88%B7%E6%9C%BA%E6%96%87%E7%AB%A0/1.png)
`然后，我们就按照下图的指示，一步步的来clean你的U盘。注意最好把盘里重要的资料备份，因为这步操作会把盘里的东西全抹掉。`
![world](https://robotkang-1257995526.cos.ap-chengdu.myqcloud.com/nao%E6%9C%BA%E5%99%A8%E4%BA%BA%E5%88%B7%E6%9C%BA%E6%96%87%E7%AB%A0/3.png)
接下来我们就可以去write了。<br>
第四步，write完成后，就要开始正式刷机了。<br>
首先，关闭机器人，刷机要在机器人关闭情况下进行，但是切记要确保机器人有电，否则刷机过程中没电了就得重刷了。<br>
接下来把U盘插入机器人后脑部的USB，然后按住breast button要等到等变蓝再松手，机器人会启动，button会持续开始闪烁蓝灯，这就意味着开始刷机了，然后耐心等待即可，大概需要十分钟左右。

刷机成功，机器人会说话，大概意思就是让你触摸它的头部或者手部脚部它就会wake up，然后就算是刷机彻底成功啦~就可以愉快的继续使用NAO了。<br>


<p style="color: #FF2D2D">
<strong>话说，中午的时候外甥女给我发来几张图片，点开一看，原来今天是我们成为QQ好友整七年的日子，感觉腾讯这个小功能做的还是蛮贴心的，也觉得时间过得还真是快啊...所以下班后去超市买了十块钱的瓜子庆祝了一下...</strong>
</p>




----------
> 总有一天，我会克服请假、签证、资金等种种羁绊，远渡重洋，跋涉万里，直到北欧大陆的尽头，在北极光的照耀下，拿出冻得快要没电的手机，打开网易云音乐，点开这首victory ，我要看看是怎样的陆地，怎样的天空，怎样的海洋，怎样的国家，怎样的人民，怎样的环境，怎样的生活，能孕育出这样的歌曲。




