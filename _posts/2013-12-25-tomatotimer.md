---
layout: post
title: 番茄时间计数器
categories: [ham]
tags: [51mcu, ele]
fullview: false
---

2013 年尾声，制作的一个玩意因为在网上看到 [番茄时间工作法](http://zh.wikipedia.org/wiki/%E7%95%AA%E8%8C%84%E5%B7%A5%E4%BD%9C%E6%B3%95"番茄时间工作法") ，
[英文页面](http://en.wikipedia.org/wiki/Pomodoro_Technique "Pomodoro Technique") 

以下转自[维基百科页面](http://zh.wikipedia.org/wiki/%E7%95%AA%E8%8C%84%E5%B7%A5%E4%BD%9C%E6%B3%95"番茄时间工作法") ，

##步骤

番茄工作法有五个基本步骤:
1. 决定待完成的任务
2. 设定番茄工作法定时器至 n 分钟（通常为25分钟）。
3. 持续工作直至定时器提示,记下一个x。
4. 短暂休息3-5分钟。
5. 每四个x，休息15-30分钟。

##原理

番茄工作法的关键是规划，追踪，记录，处理，以及可视化。在规划阶段，任务被根据优先级排入 **"To Do Today" list**。 这允许用户预计每个任务的工作量。当每个番茄时结束后，成果会被记录下来以提高参与者的成就感并为未来的自我观察和改进提供原始数据。

番茄时意指每个工作时段的时长。当任务完成后，所有番茄计时器剩下的时间会被记入超量学习。短休息时间可以辅助达到心理学上的同化作用，``3-5`` 分钟的短休息间隔开每个番茄工作时段。四个番茄工作时组成一组。一个``15-50``分钟的长休息间隔开每组作业。
这一时间管理技术的本质目的是减小内生和外在的干扰对意识流的影响。一个单位的番茄工作时不可再细分。当在番茄工作时中被打断的情况下，只可能有两种情况：干扰的活动被推迟`（知悉 - 协商 - 计划 - 收回）`，或者当前的番茄工作时废弃，必须重新开始。

##设计原理

利用定时器中断不断计数， 首先一开始开始倒计`25`分钟， 然后休息`3`分钟，这样循环工作和休息4次就来个大休息10分钟了。每次的休息和工作之间的切换都有蜂鸣器叫一声提醒。顺便还在 ``P2`` 口加入``PWM`` 呼吸灯的效果哈哈^_^。

[地址](https://github.com/radio-ho0/new_tomato/)

此电路板是大二第二学期单片机课程明哥送给我的，太happy了
