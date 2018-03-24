<div class="book with-summary">

<div class="head">

<div class="head_box">

# [](javascript:; "_('微信公众平台 小程序')")

<div class="header_ctrls">

*   [介绍](javascript:;)
    *   [小程序介绍](https://mp.weixin.qq.com/debug/wxadoc/introduction/index.html)
    *   [小游戏介绍](https://mp.weixin.qq.com/debug/wxagame/introduction/index.html)
*   [设计](https://mp.weixin.qq.com/debug/wxadoc/design/index.html)
*   [小程序开发](javascript:;)
    *   [小程序开发](https://mp.weixin.qq.com/debug/wxadoc/dev/index.html)
    *   [小游戏开发](https://mp.weixin.qq.com/debug/wxagame/dev/index.html)
*   [运营](https://mp.weixin.qq.com/debug/wxadoc/product/index.html)
*   [数据](javascript:;)
    *   [小程序数据](https://mp.weixin.qq.com/debug/wxadoc/analysis/index.html)
    *   [小游戏数据](https://mp.weixin.qq.com/debug/wxagame/analysis/index.html)

</div>

</div>

</div>

<div class="sub_nav_box">

<div class="sub_nav_inner">

<div class="book-summary-opr" id="js-book-summary-opr"><a class="book-summary-btn"></a></div>

<div class="top_sub_nav">

<div class="top_title_wap"><span class="icon_title icon_dev"></span>

微信小程序开发文档

</div>

*   [简易教程](../)
*   [框架](../framework/MINA.html)
*   [组件](../component/)
*   [API](../api/)
*   [工具](devtools.html)
*   [腾讯云支持](../qcloud/qcloud.html)

</div>

<div id="book-search-input" role="search">

<form><label for="search-input" class="search-icon" id="js-search-icon"></label><input type="text" id="search-input" name="search-input" placeholder="搜索"> </form>

</div>

</div>

</div>

<div class="book-summary">

<div class="book-summary-home" id="js-summary-home"><a><span class="icon_home_s icon_dev"></span><span class="s_title_2">开发文档首页</span></a></div>

<nav role="navigation">

*   [概览](devtools.html)
*   [界面](page.html)
    *   [启动页](page.html#启动页)
    *   [菜单栏](page.html#菜单栏)
    *   [工具栏](page.html#工具栏)
    *   [模拟器](page.html#模拟器)
    *   [设置](settings.html)
        *   [外观设置](settings.html#外观设置)
        *   [编辑设置](settings.html#编辑设置)
        *   [代理设置](settings.html#代理设置)
        *   [通知设置](settings.html#通知设置)
    *   [项目页卡](project.html)
        *   [项目设置](project.html#项目设置)
        *   [域名信息](project.html#域名信息)
        *   [腾讯云状态](project.html#腾讯云状态)
*   [快捷键](shortcut.html)
*   [代码编辑](edit.html)
    *   [文件格式](edit.html#文件格式)
    *   [文件类型](edit.html#文件支持)
    *   [自动补全](edit.html#自动补全)
    *   [项目配置文件](edit.html#项目配置文件)
    *   [Git 状态展示](edit.html#git-状态展示)
*   [小程序调试](debug.html)
    *   [模拟器](debug.html#模拟器)
    *   [自定义编译](debug.html#自定义编译)
    *   [前后台切换](debug.html#前后台切换)
    *   [调试工具](debug.html#调试工具)
        *   [Wxml Panel](debug.html#wxml-panel)
        *   [Sources Panel](debug.html#sources-panel)
        *   [AppData Panel](debug.html#appdata-panel)
        *   [Storage Panel](debug.html#storage-panel)
        *   [Network Panel](debug.html#network-panel)
        *   [Console Panel](debug.html#console-panel)
        *   [Sensor Panel](debug.html#sensor-panel)
    *   [自定义数据上报](debug.html#自定义数据上报)
    *   [特殊场景调试](different.html)
    *   [真机调试](remote-debug.html)
*   [命令行调用](cli.html)
*   [HTTP 调用](http.html)
*   [小程序开发助手](mydev.html)
*   [代码片段](minicode.html)
*   [第三方平台](ext.html)
*   [小程序插件开发](plugin.html)
*   [云测试](monkey-test.html)
*   [实现差异](details.html)
    *   [运行环境差异](details.html#运行环境差异)
    *   [ES6 支持情况](details.html#客户端es6-api-支持情况)
    *   [API 实现差异](notsupport.html)
*   [下载](download.html)
*   [历史更新日志](uplog.html)

</nav>

</div>

<div class="book-body">

<div class="body-inner">

<div class="page-wrapper" tabindex="-1" role="main">

<div class="page-inner">

<div id="book-search-results">

<div class="search-noresults">

<section class="normal markdown-section">

# 功能概述

真机远程调试功能可以实现直接利用开发者工具，通过网络连接，对手机上运行的小程序进行调试，帮助开发者更好的定位和查找在手机上出现的问题。

## 调试流程

要发起一个真机远程调试流程，需要先点击开发者工具的工具栏上 “远程调试” 按钮。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/button.jpg)

此时，工具会将本地代码进行处理打包并上传，就绪之后，使用手机客户端扫描二维码即可弹出调试窗口，开始远程调试。

## 远程调试窗口

使用手机扫描此二维码，即可开始远程调试。

要结束调试，直接关闭此调试窗口，或点击右下角 “结束调试” 按钮即可。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/window.jpg)

远程调试窗口分为两部分，分别是左侧的调试器视图、右侧的信息视图。开发者可以在调试器里直接进行代码的调试，并查看 Storage 情况；信息视图则可以查看目前与手机和服务器的连接情况，以及发生的错误信息等。

### 调试器

在远程调试的调试器里，开发者可以在 Console 面板里对代码进行调试，在 Sources 面板里查看小程序的源代码并进行断点单步调试，在 Storage 面板里查看小程序的 Storage 使用情况等。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/console.jpg)

注意，要在 Console 里对小程序进行调试，需要将调试的上下文切换到 VM Context 1，如图所示。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/context.jpg)

在 Sources 面板查看源代码时，开发者所有的文件路径都是以 `weapp://` 开头的。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/sources.jpg)

除了可以在调试器进行单步调试，开发者还能在代码中手动插入 `debugger;` 语句进行断点调试。因此，如果想要在小程序启动的尽早时刻断点，可以在进入远程调试之前，编辑代码手动在需要断点处的代码插入 `debugger;` 语句来实现。

WXML、AppData、Storage 面板的操作和开发者工具调试模拟器时的操作一致。注意，如果在右侧信息视图取消勾选了 “使用工具端的 Storage”，则所有的 Storage 数据将被存储在手机上，将不再出现 Storage 面板。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/storage.jpg)

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/appdata.jpg)

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/wxml.jpg)

### 信息视图

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/info.jpg)

右侧的信息视图展示了手机、网络连接的信息。手机信息展示手机的型号、系统、名称、微信版本等信息，以及通信延时。通信延时越小，与手机的通信越流畅。

在 “连接信息” 里，展示了工具与服务器的连接信息，包括了连接状态、服务器状态等，当连接故障、服务器阻塞影响到调试的过程和流畅度时，此处将展示这一状态。当连接状态为 “已结束” 时，表明调试已被终止。

“警告和错误” 展示了最近发生的错误和警告信息。如果网络连接断开，此处将会询问开发者是否需要重新连接。

## 手机端展示

调试过程中的手机端展示如下所示。

> 当手机无网络或者进入了断点状态时，将会出现一个浮层提示并阻止进一步的操作。

![](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools2/remote-debug/iphone.jpg)

</section>

</div>

<div class="search-results">

<div class="has-results">

# <span class="search-results-count"></span>个结果 "<span class="search-query"></span>"

</div>

<div class="no-results">

# 没有找到相关内容 "<span class="search-query"></span>"

</div>

</div>

</div>

</div>

</div>

<div class="foot" id="footer">

*   [关于腾讯](http://www.tencent.com/zh-cn/index.shtml)
*   [文档中心](https://mp.weixin.qq.com/debug/wxadoc/introduction/index.html?t=1484641676&)
*   [辟谣中心](https://mp.weixin.qq.com/cgi-bin/opshowpage?action=dispelinfo&lang=zh_CN&begin=1&count=9)
*   [客服中心](http://kf.qq.com/faq/120911VrYVrA1509086vyumm.html)
*   [联系邮箱](mailto:weixinmp@qq.com)
*   Copyright © 2012-<span id="s_copyright_year"></span> Tencent. All Rights Reserved.

</div>

</div>

[](different.html)[](cli.html)</div>

</div>