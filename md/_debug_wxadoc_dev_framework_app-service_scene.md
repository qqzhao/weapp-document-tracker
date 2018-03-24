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

*   [简易教程](../../)
*   [框架](../MINA.html)
*   [组件](../../component/)
*   [API](../../api/)
*   [工具](../../devtools/devtools.html)
*   [腾讯云支持](../../qcloud/qcloud.html)

</div>

<div id="book-search-input" role="search">

<form><label for="search-input" class="search-icon" id="js-search-icon"></label><input type="text" id="search-input" name="search-input" placeholder="搜索"> </form>

</div>

</div>

</div>

<div class="book-summary">

<div class="book-summary-home" id="js-summary-home"><a><span class="icon_home_s icon_dev"></span><span class="s_title_2">开发文档首页</span></a></div>

<nav role="navigation">

*   [目录结构](../structure.html)
*   [配置](../config.html)
*   [逻辑层](./)
    *   [注册程序](app.html)
    *   [场景值](scene.html)
    *   [注册页面](page.html)
    *   [路由](route.html)
    *   [模块化](module.html)
    *   [API](api.html)
*   [视图层](../view/)
    *   [WXML](../view/wxml/)
        *   [数据绑定](../view/wxml/data.html)
        *   [列表渲染](../view/wxml/list.html)
        *   [条件渲染](../view/wxml/conditional.html)
        *   [模板](../view/wxml/template.html)
        *   [事件](../view/wxml/event.html)
        *   [引用](../view/wxml/import.html)
    *   [WXS](../view/wxs/)
        *   [模块](../view/wxs/01wxs-module.html)
        *   [变量](../view/wxs/02variate.html)
        *   [注释](../view/wxs/03annotation.html)
        *   [运算符](../view/wxs/04operator.html)
        *   [语句](../view/wxs/05statement.html)
        *   [数据类型](../view/wxs/06datatype.html)
        *   [基础类库](../view/wxs/07basiclibrary.html)
    *   [WXSS](../view/wxss.html)
    *   [组件](../view/component.html)
*   [自定义组件](../custom-component/)
    *   [组件模版和样式](../custom-component/wxml-wxss.html)
    *   [Component构造器](../custom-component/component.html)
    *   [组件事件](../custom-component/events.html)
    *   [behaviors](../custom-component/behaviors.html)
    *   [组件间关系](../custom-component/relations.html)
    *   [抽象节点](../custom-component/generics.html)
*   [插件](../plugin/)
    *   [开发插件](../plugin/development.html)
    *   [使用插件](../plugin/using.html)
    *   [插件的限制](../plugin/api-limit.html)
*   [分包加载](../subpackages.html)
*   [多线程](../workers.html)
*   [基础库](../client-lib.html)
*   [兼容](../compatibility.html)
*   [运行机制](../operating-mechanism.html)
*   [性能](../performance/)
    *   [优化建议](../performance/tips.html)
    *   [分析工具](../performance/tools.html)

</nav>

</div>

<div class="book-body">

<div class="body-inner">

<div class="page-wrapper" tabindex="-1" role="main">

<div class="page-inner">

<div id="book-search-results">

<div class="search-noresults">

<section class="normal markdown-section">

# 场景值

> 基础库 1.1.0 开始支持，低版本需做[兼容处理](../compatibility.html)

当前支持的场景值有：

<table>

<thead>

<tr>

<th>场景值ID</th>

<th>说明</th>

</tr>

</thead>

<tbody>

<tr>

<td>1001</td>

<td>发现栏小程序主入口</td>

</tr>

<tr>

<td>1005</td>

<td>顶部搜索框的搜索结果页</td>

</tr>

<tr>

<td>1006</td>

<td>发现栏小程序主入口搜索框的搜索结果页</td>

</tr>

<tr>

<td>1007</td>

<td>单人聊天会话中的小程序消息卡片</td>

</tr>

<tr>

<td>1008</td>

<td>群聊会话中的小程序消息卡片</td>

</tr>

<tr>

<td>1011</td>

<td>扫描二维码</td>

</tr>

<tr>

<td>1012</td>

<td>长按图片识别二维码</td>

</tr>

<tr>

<td>1013</td>

<td>手机相册选取二维码</td>

</tr>

<tr>

<td>1014</td>

<td>小程序模版消息</td>

</tr>

<tr>

<td>1017</td>

<td>前往体验版的入口页</td>

</tr>

<tr>

<td>1019</td>

<td>微信钱包</td>

</tr>

<tr>

<td>1020</td>

<td>公众号 profile 页相关小程序列表</td>

</tr>

<tr>

<td>1022</td>

<td>聊天顶部置顶小程序入口</td>

</tr>

<tr>

<td>1023</td>

<td>安卓系统桌面图标</td>

</tr>

<tr>

<td>1024</td>

<td>小程序 profile 页</td>

</tr>

<tr>

<td>1025</td>

<td>扫描一维码</td>

</tr>

<tr>

<td>1026</td>

<td>附近小程序列表</td>

</tr>

<tr>

<td>1027</td>

<td>顶部搜索框搜索结果页“使用过的小程序”列表</td>

</tr>

<tr>

<td>1028</td>

<td>我的卡包</td>

</tr>

<tr>

<td>1029</td>

<td>卡券详情页</td>

</tr>

<tr>

<td>1030</td>

<td>自动化测试下打开小程序</td>

</tr>

<tr>

<td>1031</td>

<td>长按图片识别一维码</td>

</tr>

<tr>

<td>1032</td>

<td>手机相册选取一维码</td>

</tr>

<tr>

<td>1034</td>

<td>微信支付完成页</td>

</tr>

<tr>

<td>1035</td>

<td>公众号自定义菜单</td>

</tr>

<tr>

<td>1036</td>

<td>App 分享消息卡片</td>

</tr>

<tr>

<td>1037</td>

<td>小程序打开小程序</td>

</tr>

<tr>

<td>1038</td>

<td>从另一个小程序返回</td>

</tr>

<tr>

<td>1039</td>

<td>摇电视</td>

</tr>

<tr>

<td>1042</td>

<td>添加好友搜索框的搜索结果页</td>

</tr>

<tr>

<td>1043</td>

<td>公众号模板消息</td>

</tr>

<tr>

<td>1044</td>

<td>带 shareTicket 的小程序消息卡片（[详情](../../api/share.html#获取更多转发信息))</td>

</tr>

<tr>

<td>1047</td>

<td>扫描小程序码</td>

</tr>

<tr>

<td>1048</td>

<td>长按图片识别小程序码</td>

</tr>

<tr>

<td>1049</td>

<td>手机相册选取小程序码</td>

</tr>

<tr>

<td>1052</td>

<td>卡券的适用门店列表</td>

</tr>

<tr>

<td>1053</td>

<td>搜一搜的结果页</td>

</tr>

<tr>

<td>1054</td>

<td>顶部搜索框小程序快捷入口</td>

</tr>

<tr>

<td>1056</td>

<td>音乐播放器菜单</td>

</tr>

<tr>

<td>1057</td>

<td>钱包中的银行卡详情页</td>

</tr>

<tr>

<td>1058</td>

<td>公众号文章</td>

</tr>

<tr>

<td>1059</td>

<td>体验版小程序绑定邀请页</td>

</tr>

<tr>

<td>1064</td>

<td>微信连Wi-Fi状态栏</td>

</tr>

<tr>

<td>1067</td>

<td>公众号文章广告</td>

</tr>

<tr>

<td>1068</td>

<td>附近小程序列表广告</td>

</tr>

<tr>

<td>1071</td>

<td>钱包中的银行卡列表页</td>

</tr>

<tr>

<td>1072</td>

<td>二维码收款页面</td>

</tr>

<tr>

<td>1073</td>

<td>客服消息列表下发的小程序消息卡片</td>

</tr>

<tr>

<td>1074</td>

<td>公众号会话下发的小程序消息卡片</td>

</tr>

<tr>

<td>1078</td>

<td>连Wi-Fi成功页</td>

</tr>

<tr>

<td>1089</td>

<td>微信聊天主界面下拉</td>

</tr>

<tr>

<td>1090</td>

<td>长按小程序右上角菜单唤出最近使用历史</td>

</tr>

<tr>

<td>1092</td>

<td>城市服务入口</td>

</tr>

</tbody>

</table>

可以在 App 的 onlaunch 和 onshow 中获取上述场景值，部分场景值下还可以获取来源应用、公众号或小程序的appId。[详见](app.html)

**Tip:** 由于Android系统限制，目前还无法获取到按 Home 键退出到桌面，然后从桌面再次进小程序的场景值，对于这种情况，会保留上一次的场景值。

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

[](app.html)[](page.html)</div>

</div>