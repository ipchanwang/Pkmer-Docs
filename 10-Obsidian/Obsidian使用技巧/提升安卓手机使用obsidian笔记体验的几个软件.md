---
uid: 20231127171110
title: 提升安卓手机使用 obsidian 笔记体验的几个软件
tags: [移动端, 手机]
description: 
author: calmwaves
type: other
draft: false
editable: false
modified: 20231209100538
---

# 提升安卓手机使用 obsidian 笔记体验的几个软件

## 需求分析

在日常生活中，我们常常不能时刻携带电脑，但我们的灵感却总是在随时降临。当这种情况发生时，我们想要记录灵感，能随身携带的手机就有得天独厚的便利。于是，我们产生了一种需求：在手机上可以随时查阅 Obsidian 中的笔记，并能方便地记录和简单编辑。 这个需求的核心是希望通过手机实现对知识的获取和记录，使之更加便捷和高效。

但我们不能要求手机上的体验和电脑能完全一样，所以我根据实际使用场景，确定了以下几个刚需：

1. 笔记库的安卓和电脑之间要进行双向同步，以确保数据的一致性。
2. 查阅功能是必需的
	1. 首先要能够搜索整个笔记库，因为我们有时候也不确定内容会记在哪篇笔记中。
	2. 查阅对于打开速度要求不高，不奢求一秒打开，当然打开速度也不能过慢，超过半分钟就不可接受了，更不能像某些在线笔记软件那样偶尔因为不可抗因素连打开查阅都不能
3. 简单的记录编辑功能也是必要的
	1. 手机只是用于快速记一点零碎信息，因此不能要求复杂的编辑功能
	2. 但是编辑打开的速度一定要快，很多时候，我们会突然有一个想法需要记录下来，如果打开软件都需要十秒钟，可能我们已经忘记了要记什么。
	3. 编辑记录的数据能很方便的进入到 obsidian 库中

Obsidian 的数据是以 Markdown 明文形式存储的，这给了我们可操作性的空间，我们可以借助其他软件来满足上述的三个需求。这也是本文的主要目的，接下来就三个需求一一说明我的解决方案。

## 同步

我的设备是 win10 和 Android

（实际上我还有一台 ipad，但我本身很少使用，由于 ipad 封闭的文件政策，我几乎放弃了在 ipad 上使用 obsidian，只将库文件同步到 ipad 借助 mweb 偶尔查看编辑）

同步采用的软件是微力同步，下载：[官网链接](http://www.verysync.com/download.html)

不建议将电脑上的插件配置全同步过来，因为手机性能确实不好，开得插件越多，启动加载就越慢

> [!NOTE] 那么会有一个新的问题：如何让电脑和手机的笔记数据同步但是配置不一样？
> 有两种解决方案：
> 一是使用微力同步的『ignore 忽略列表』功能
> 二是改配置文件夹名称，让电脑和手机使用不同的配置文件夹（设置→关于→切换配置文件夹）

## 查阅

实际上，Obsidian 本身的查阅搜索功能已经很强大，如果只是进行简单的查阅，直接使用 Obsidian 本体即可，详细可查看 obsidian 搜索功能的教程。

虽然查阅对于打开速度要求不高，不奢求一秒打开，当然打开速度也不能过慢。

因此我在安卓上只留了三个插件，dataview，calendar，Copy-Image-and-URL-context-menu

留下的原因就不细讲了，与我个人的笔记习惯和应用场景相关，想了解这几个插件的话点进链接看社区文章即可

关于安卓上的主题，我使用的是默认主题，配了三个 css，在之前的文章中我已经写过：[[Obsidian样式-通过css修改安卓上的搜索框宽度]]（提升查阅体验），[[通过css在移动端右下角添加源码和阅读转换按钮]]（提升编辑体验），[[obsidian安卓上利用css修改界面字体]]

## 简单编辑

即使我在安卓上仅保留了 3 个插件，但是安卓的 obsidian 打开速度仍然称不上快，因此我强烈推荐这个软件 **zettel notes** ，[下载地址](https://znotes.thedoc.eu.org/download/)，请注意，除了是该软件的用户之外，我与开发人员没有任何关系。

这个软件可以与 obsidian 无缝集成，主要有以下几个优点：

1. 直接读取 obsidian 库里的 md 文件
2. 打开速度超快（obsidian 在安卓上的打开速度真的让人心急）
3. 和 ob 的很多语法都兼容，`[[]]` 双链，`#` 标签，yaml 属性等
4. 可以插入图片，附件等
5. 有快速记录的 shortcut，可以在桌面建立一个快捷方式，点击马上就进入笔记界面开始记录

上述已经满足了我在第一节中的需求，而且和 ob 耦合起来十分好，在此基础上，zettel notes 还有很多让我惊喜的功能，以下我列举几个我已知的功能，我不常用这些功能，可自行探索

1. 有桌面小部件可以把某一篇笔记展示在桌面，单击即可进入编辑器（速度也超快）
2. 支持外链 uri：`znotes://repository/note.md`
3. log 功能，在笔记中记录时间戳
4. 日历功能
5. git 同步，以及 webdav，google drive，Dropbox，SFTP 同步
6. 备份功能
7. 音频笔记、绘画笔记等等功能
8. 网页剪藏功能
9. 导出单篇笔记为 html 或者 pdf 格式
10. 文字转语音朗读功能
11. ……仍有许多功能我未列举，开发者仍在不断更新，而且响应非常快，会添加更多的功能，如果对此感兴趣，可以加入 tg 群组反馈和交流。

> 我在另一篇文章 [[文字转语音朗读你的笔记]] 中提到借助 edge 的大声朗读功能来文字转语音，在安卓上，即可借助 zettel notes 导出 html 文件，再在 edge 中打开，从而实现朗读功能
> 而 zettel notes 也自带文字转语音朗读功能，可以直接使用，这调用的是系统语音引擎，可以安装诸如 MultiTTS 或者讯飞等等自行修改语音引擎，获得更自然逼真的效果。

==软件本体不收费，作者开发了几个插件，可以在 Google play 里付费购买支持作者，如果你暂时没有能力支持，可以在 F-Droid 上免费下载插件==

对我来说使用上稍有不爽的点：

一是不能打开进入 app 自动打开今天的日记

二是图片链接采用基于库的绝对链接，但是和 ob 的绝对链接不兼容（这是 obsidian 对于链接处理的问题，无法解决）

（关于 ob 里的几种链接，后续有时间会写一下好好讲明白）

> [!note] 推荐另一个软件：mixplorer
> 这是一个文件管理器，可以在 google play 里下载
> obsidian 的文件都是明文以 md 存储的，可以直接在文件管理器里查看到源文件，这个文件管理器自带文本编辑器，也能用来简单地查看和编辑 md 文件，以及其他纯文本文件，比如我第三节提到的三个 css 文件，就是在 mixplorer 里完成的编写。
>
> 多说一点，在 ob 还没有问世的时候，我就已经在用这个文件管理器了，也就是说，mixplorer 不仅能辅助 ob 的使用，对于日常的文件管理也适合。
> - （以后有时间也会分享一下关于 mixplorer 的使用经验，感兴趣的话可以先自行探索）

## 其他软件推荐

上述已经够用了，全是我自己安装在手机上正在用的，下面是还列出一些可以和 obsidian 联用的软件，但我不需要了所以没有安装。

markor：安卓上老牌的 md 编辑器，开源，功能很全

epsilon notes：安卓上很好的 Markdown 编辑器，需要付费购买

[Android-Markdown-Widge](https://github.com/Tiim/Android-Markdown-Widget)：用于在主屏幕上显示 Markdown 文件的小部件应用程序，专门为 obsidian 做了适配，但是目前点击小部件在 ob 中打开的功能已经失效了

### 易码

先说缺点吧，3 年没更新了，作者已然弃坑，但是仍旧很好用，软件评论区曾经有一句为了这个软件留在安卓系统没有转去 ios。相比于 ob，这个软件的功能太少了（自定义选项太少，不能和我的日记格式和 yaml 兼容，毕竟 3 年没更新了），但刚刚好能满足我第一节分析的需求，在发现 zettel notes 之前，我一直留着这个软件。

优点：直接编辑 obsidian 的库文件，webdav 同步的功能很强，实时渲染也做的很好

总结：日常使用坚果云同步且安卓上需求不高的话，可以考虑这个软件

下载：酷安（但由于长时间不更新已经被下架），可以在酷安搜索动态自行寻找安装包

### fv 悬浮球

可借助 fv 悬浮球的自定义任务，添加文字到 md 文件中，从而实现闪念笔记的效果。

但是这个需要花点时间配置，而且只有一个输入框，不能换行，缺点比较多

这是我之前的配置，若有需要可参考

![image.png](https://cdn.pkmer.cn/images/20231127171526.png!pkmer)

## 安卓使用的其他注意事项

不让 obsidian 库里的图片出现在相册：[[安卓和鸿蒙设备照片中乱入Obsidian图片解决方案]]

## 最后一个预告

PKMer 出品的 [Thino 2.1 (原 Obsidian Memos)](https://pkmer.cn/products/productDetails/) 正在火热内测中，计划支持手机上的快速记录和云端同步。

通过向社区投稿知识、方法论等稿件（协作者指南），或者社区为爱 [发电捐助](https://pkmer.cn/products/price/) 都可以获得内测资格，thino 插件介绍可 [点击网址]( https://pkmer.cn/show/20231109234455 ) 查看。
