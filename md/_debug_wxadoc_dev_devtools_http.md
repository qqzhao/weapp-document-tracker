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

开发者工具提供了命令行与 HTTP 服务两种接口供外部调用，开发者可以通过命令行或 HTTP 请求指示工具进行登录、预览、上传等操作。

## HTTP

http 服务在工具启动后自动开启，HTTP 服务端口号在用户目录下记录，可通过检查用户目录、检查用户目录下是否有端口文件及尝试连接来判断工具是否安装/启动。

端口号文件位置：

macOS : `~/Library/Application Support/微信web开发者工具/Default/.ide`

Windows : `~/AppData/Local/微信web开发者工具/User Data/Default/.ide`

### 1\. 打开工具或指定项目

接口定义：

URL： /open

HTTP 方法: GET

<table>

<thead>

<tr>

<th style="text-align:center">URL 参数</th>

<th>必填</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:center">projectpath</td>

<td>否</td>

<td>打开指定路径中的项目。如项目已打开，自动刷新项目。如项目未创建，自动创建并打开项目</td>

</tr>

</tbody>

</table>

示例：

    # 打开工具
    http://127.0.0.1:端口号/open
    # 打开/刷新项目
    http://127.0.0.1:端口号/open?projectpath=项目全路径

注意：

*   项目路径中必须含正确格式的 project.config.json 且其中有 appid 和 projectname 字段。
*   项目路径需经 URL encode

### 2\. 登录

接口定义：

URL：/login

HTTP 方法：GET

<table>

<thead>

<tr>

<th style="text-align:center">URL 参数</th>

<th>必填</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:center">format</td>

<td>否</td>

<td>指定登录二维码返回格式，可选值有 image、base64、terminal，默认 image。图片格式为 png</td>

</tr>

<tr>

<td style="text-align:center">qroutput</td>

<td>否</td>

<td>指定文件路径，在文件写入二维码数据。如指定，二维码将被写入指定路径的文件内，如未指定，二维码将作为请求相应体返回</td>

</tr>

</tbody>

</table>

示例：

    # 登录，返回图片格式的二维码
    http://127.0.0.1:端口号/login
    # 登录，取 base64 格式二维码
    http://127.0.0.1:端口号/login?format=base64
    # 登录，取 base64 格式二维码，并写入 /Users/username/logincode.txt
    http://127.0.0.1:端口号/login?format=base64&qroutput=%2FUsers%2Fusername%2Flogincode.txt

### 3\. 预览

接口定义：

URL：/preview

HTTP 方法：GET

<table>

<thead>

<tr>

<th style="text-align:center">URL 参数</th>

<th>必填</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:center">projectpath</td>

<td>是</td>

<td>预览指定路径中的项目。如项目已打开，自动刷新项目。如项目未创建，自动创建并预览项目</td>

</tr>

<tr>

<td style="text-align:center">format</td>

<td>否</td>

<td>指定登录二维码返回格式，可选值有 image、base64、terminal，默认 image。图片格式为 png</td>

</tr>

<tr>

<td style="text-align:center">qroutput</td>

<td>否</td>

<td>指定文件路径，在文件中写入二维码数据。如指定，二维码将被写入指定路径的文件内，如未指定，二维码将作为请求相应体返回</td>

</tr>

</tbody>

</table>

示例：

    # 预览路径为 /Users/username/demo 的项目，返回图片格式的二维码
    http://127.0.0.1:端口号/preview?projectpath=%2FUsers%2Fusername%2Fdemo
    # 预览路径为 /Users/username/demo 的项目，返回 base64 格式的二维码
    http://127.0.0.1:端口号/preview?projectpath=%2FUsers%2Fusername%2Fdemo&format=base64
    # 预览路径为 /Users/username/demo 的项目，返回 base64 格式的二维码，并写入 /Users/username/logincode.txt
    http://127.0.0.1:端口号/preview?projectpath=%2FUsers%2Fusername%2Fdemo&format=base64&qroutput=%2FUsers%2Fusername%2Flogincode.txt

### 4\. 上传

接口定义：

URL：/upload

HTTP 方法：GET

<table>

<thead>

<tr>

<th style="text-align:center">URL 参数</th>

<th>必填</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:center">projectpath</td>

<td>是</td>

<td>上传指定路径中的项目</td>

</tr>

<tr>

<td style="text-align:center">version</td>

<td>是</td>

<td>版本号</td>

</tr>

<tr>

<td style="text-align:center">desc</td>

<td>否</td>

<td>本次上传的版本备注</td>

</tr>

</tbody>

</table>

示例：

    # 上传路径为 /Users/username/demo 的项目，指定版本号为 v1.0.0
    http://127.0.0.1:端口号/upload?projectpath=%2FUsers%2Fusername%2Fdemo&version=v1.0.0
    # 上传路径为 /Users/username/demo 的项目，指定版本号为 v1.0.0，并带上备注
    http://127.0.0.1:端口号/upload?projectpath=%2FUsers%2Fusername%2Fdemo&version=v1.0.0&desc=test

### 5\. 自动化测试

接口定义：

URL：/test

HTTP 方法：GET

<table>

<thead>

<tr>

<th style="text-align:center">URL 参数</th>

<th>必填</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:center">projectpath</td>

<td>是</td>

<td>测试指定路径中的项目</td>

</tr>

</tbody>

</table>

示例：

    # 提交路径为 /Users/username/demo 的项目进行测试
    http://127.0.0.1:端口号/test?projectpath=%2FUsers%2Fusername%2Fdemo

### 请求响应

正常情况下 HTTP 相应状态码为 200，错误时 400，返回如下格式的 JSON 字符串：

    {
      "code": 40000,
      "error": "原因"
    }

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

[](cli.html)[](mydev.html)</div>

</div>