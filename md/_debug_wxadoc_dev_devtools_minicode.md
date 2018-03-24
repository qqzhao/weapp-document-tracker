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

代码片段是一种可分享的小项目，可用于分享小程序和小游戏的开发经验、展示组件和 API 的使用、复现开发问题等等。分享代码片段会得到一个链接，所有拥有此分享链接的人可以在工具中导入此代码片段。如果网页可点击的链接指向的是分享链接，那么点击链接也会自动打开工具进入代码片段导入页。使用最新版的开发者工具可以[点此体验导入代码片段](wechatide://minicode/a07de76a27e3e7836c4ea39d72f75eda)。

### 创建代码片段

在工具选择项目的界面中，右侧可以选择代码片段页卡，查看所有本地代码片段，在右下角可以点击创建代码片段。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/select-project.jpg)

创建代码片段需要填入代码片段名称、本地存放目录。AppID 不是必填项，如果需要演示依赖 AppID 的操作则需填写。如果存放目录是空目录，则可在下方选择小程序、小游戏等的快速启动模板。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/create-minicode.jpg)

信息填写正确后，点击创建即可完成创建并打开代码片段。

### 代码片段主界面

代码片段的主界面与普通项目主要有以下几点区别：

1.  没有上传、腾讯云和申请测试报告等功能
2.  详情页中会展示上次分享的链接，并可以一键复制
3.  代码片段的快速启动模板与普通项目的快速启动模板不同，体积更小，功能更精简

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/project.jpg)

### 分享代码片段

在工具栏上点击分享按钮即可开启分享代码片段的流程，在分享信息中需要填写以下内容：

*   项目描述：简要介绍此代码片段的功能和目的
*   是否需要 AppID：如果是，开发者导入代码片段时会建议其填入 AppID 以完整运行代码片段
*   最低库版本：开发者打开导入的代码片段时详情页的调试基础库不会低于指定的版本

分享的小程序代码片段最大大小为 100KB，小游戏代码片段最大为 200KB。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/share.png)

分享成功后会展示分享链接，可复制分享给其他开发者，其他开发者在工具中选择导入代码片段并粘贴链接即可导入。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/share-success.png)

分享的链接除了可以粘贴到导入页导入外，还可以设置为可点击的链接。如果 `html` `<a>` 标签的 `href` 属性设置为分享的链接，如 `<a href="wechatide://minicode/76b799966b6ead1837edac517cc02e02">代码片段示例</a>`，则用户点击此链接时会自动打开工具进入代码片段导入页，最后点击导入即可完成导入。在开发者社区发帖时，如果想要提供 demo 示例，如果想要提供 demo 示例，可以插入一个链接为代码片段分享链接的超链接。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/share-bbs.png)

### 导入代码片段

在选择代码片段的页面的右下角可以点击导入进入导入页，或者点击菜单栏上的项目选项卡下的导入代码片段来打开导入页。导入时需要填写分享链接或代码片段 ID。链接的最后一部分即是代码片段的 ID，如 `wechatide://minicode/76b799966b6ead1837edac517cc02e02` 的 ID 为 `76b799966b6ead1837edac517cc02e02`。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/import-minicode.jpg)

导入时可选择存放目录和 AppID。存放目录默认是在临时文件夹。

![minicode](https://mp.weixin.qq.com/debug/wxadoc/dev/image/devtools/minicode/import-minicode-info.jpg)

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

[](mydev.html)[](ext.html)</div>

</div>