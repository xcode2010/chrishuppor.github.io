---
layout: post
title: "MyLittleToolsInstruction"
date: 2019-04-29 8:8:8
categories: MyLittleTools
tags: Instruction
---
All My Little Tools

所有小工具的源码获取地址： [https://github.com/chrishuppor/src/tree/master/MyLittleTools](https://github.com/chrishuppor/src/tree/master/MyLittleTools)

所有小工具的可执行程序获取地址：[https://github.com/chrishuppor/src/tree/master/MyLittleTools/bin](https://github.com/chrishuppor/src/tree/master/MyLittleTools/bin)

以下带*的工具仅为本人机器开发，即src下的“专用小工具”

# FormatErrCode

* 功能：系统错误码描述工具
  * 输入err code回车，程序显示对应英文描述
* 操作
  * 输入GetLastErr()获得的&lt;err code>，回车
  * 输入任意字母结束程序


# DllInjectTool

* 功能：dll注入卸载工具
  * dll注入，支持特定进程注入和全部进程注入
  * 支持dll卸载
* 操作
  * cmd启动，输入相应的启动参数
* 启动参数说明
  * 参数1-可以是pid，可以是进程名。如果使用“*”则尝试注入所有进程
  * 参数2-dll绝对路径（未测试中文路径）
  * 参数3-模式“-i”表示注入，“-d”表示卸载，不区分大小写

# Base64

* 功能：base64编解码
  * 解码base64和字符串base64编码
* 操作
  * 输入要处理的字符串，然后输入0或1。（0表示编码，1表示解码）
* 注意：
  * 这个程序有输入字符的限制
  * 没有对输入数据进行判断，默认输入的都是合法数据

ps:所以说这个程序烂的很，比errcode那个还要充数

# FastDirOpen

* 功能及操作：快速目录启动工具
  * 添加、删除目录——支持多路径拖拽添加，不可以重复添加；右键、Del删除指定路径（仅支持单路径删除）
  * 弹出对应文件夹界面——双击目录、单击+回车、上下键选择+回车
  * 修改备注——两次单击或右键菜单修改备注
  * 排序——单击列标题可按列值从小到大排列
  * 支持无效路径”清理“——将不存在的路径删除
  * 支持全部路径“清空”——删除全部路径
  * 最小化时最小化到系统托盘
  * 启动时保留原来的配置（配置文件为同目录下mydeardirs）
* 无关功能
  * 列表区域可以跟随界面缩放，不影响美观

PS>点解会有呢个程序嚟？还不是因为windows的快速访问太烂，而我又不想每回都要去一堆文件夹中找目标文件

对这个程序还是比较满意，但仍有两处地方需要处理：

1. 360总是提示该程序在利用文件资源管理器，添加了信任程序还是不行
2. 图标：这图标是模拟人生中我家的一张照片，丑爆了
3. 删除：支持多路径删除

# MD5Calc

* 功能：计算文件或字符串的md5值
* 操作：
  * 输入
    * 字符串：在str文本框输入字符串
    * 文本路径：在file文本框输入文件路径，也可以使用文件浏览，也支持文件拖拽（PS:感觉我像是文件的亲妈字符串的后娘）
  * 计算：点击Calc按键，如果是文件则支持回车进行计算

# bilibili弹幕删减脚本*

* 操作：
  1. 输入本地弹幕路径
  2. 根据提示选择保留该弹幕还是删除该条弹幕，如果没有保留上一条弹幕但现在后悔了，则可以输入2表明自己很2，然后就重新保留上一条弹幕了

* 结果：将删减后的结果保存在<name>.xml文件同目录的<name_reduced>.xml文件中

# IsTheSameFile

* 功能：比较两个文件是否完全一致
* 操作：输入要比较的两个文件绝对路径
* 结果：一致则输出“Same.”，不一致输出“Diff.”

ps:不值一提的工具，纯粹为了个人方便，不用在需要时去网上搜那些挑花了眼运行又慢的工具

# CompletePost*

* 目的：按照jeklly搭建的博客的post文件格式编写文件不符合正常的文件编写习惯，所以用这个py来将“正常”编写的draft完善成post
* 操作：python3将_drafts文件夹拖到本py上
* 结果：将已经编好名字和内容的md文件完善成jeklly搭建的博客post文件的格式，并添加到_posts文件夹中

# UpdatePostTime*

- 目的：博文写完了之后不是一成不变的，总会修修补补。修补完了之后肯定希望文件中与时间相关的信息能够更新，但手动修改又会破坏写博文的流畅体验，所以用这个py来自动将文件中时间相关信息修改为文档的更新时间。
- 操作：python3下直接运行
- 结果：将更新过的post中的文件时间相关字符串替换为最新的时间。
