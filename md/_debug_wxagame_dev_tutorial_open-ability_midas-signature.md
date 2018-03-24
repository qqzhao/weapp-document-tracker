<div class="book with-summary">

<div class="head">

<div class="head_box">

# [](javascript:; "_('微信公众平台 小程序')")

<div class="header_ctrls">

*   [介绍](javascript:;)
    *   [小程序介绍](https://mp.weixin.qq.com/debug/wxadoc/introduction/index.html)
    *   [小游戏介绍](https://mp.weixin.qq.com/debug/wxagame/introduction/index.html)
*   [设计](https://mp.weixin.qq.com/debug/wxadoc/design/index.html)
*   [小游戏开发](javascript:;)
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

微信小游戏开发文档

</div>

*   [教程](../../index.html)
*   [API](../../document/render/canvas/wx.createCanvas.html)
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

*   [基础](../../index.html)
    *   [快速上手](../../index.html)
    *   [Adapter](../base/adapter.html)
    *   [对引擎的支持](../base/engine.html)
    *   [模块化](../base/module.html)
*   [能力](../ability/audio.html)
    *   [音频播放](../ability/audio.html)
    *   [文件系统](../ability/file-system.html)
*   [可用性](../usability/debug.html)
    *   [调试](../usability/debug.html)
    *   [性能](../usability/performance.html)
    *   [小游戏更新](../usability/update.html)
    *   [多线程 Worker](../usability/worker.html)
*   [开放能力](authorize.html)
    *   [用户授权](authorize.html)
    *   [用户登录态签名](http-signature.html)
    *   [米大师支付签名](midas-signature.html)
    *   [关系链数据使用指南](open-data.html)
    *   [虚拟支付](payment.html)
    *   [获取二维码](qrcode.html)
    *   [转发](share.html)
    *   [用户数据的签名验证和加解密](signature.html)

</nav>

</div>

<div class="book-body">

<div class="body-inner">

<div class="page-wrapper" tabindex="-1" role="main">

<div class="page-inner">

<div id="book-search-results">

<div class="search-noresults">

<section class="normal markdown-section">

## 米大师支付签名

以查询余额的接口为例，原始请求信息：

1.  米大师密钥：zNLgAGgqsEWJOg1nFVaO5r7fAlIQxr1u
2.  HTTP请求方式: POST
3.  请求的URI：/cgi-bin/midas/getbalance

### sig签名

#### 参与米大师签名请求参数

    "openid":"odkx20ENSNa2w5y3g_qOkOvBNM1g",
    "appid":"wx1234567",
    "offer_id":"12345678",
    "ts":1507530737,
    "zone_id":"1",
    "pf":"iap"

对参与米大师签名的参数按照key=value的格式，并按照参数名ASCII字典序升序排序如下：

    stringA="appid=wx1234567&offer_id=12345678&openid=odkx20ENSNa2w5y3g_qOkOvBNM1g&pf=iap&ts=1507530737&zone_id=1"

拼接uri、method和米大师密钥：

    stringSignTemp=stringA+"&org_loc=/cgi-bin/midas/getbalance&method=POST&secret=zNLgAGgqsEWJOg1nFVaO5r7fAlIQxr1u"

把米大师密钥作为key，使用HMAC-SHA256得到签名。

    sig=hmac_sha256(key,stringSignTemp)
       ="d1f0a41272f9b85618361323e1b19cd8cb0213f21b935aeaa39c160892031e97"

### mp_sig签名

#### 1 参与开平签名请求参数

    "access_token":"ACCESSTOKEN",
    "openid":"odkx20ENSNa2w5y3g_qOkOvBNM1g",
    "appid":"wx1234567",
    "offer_id":"12345678",
    "ts":1507530737,
    "zone_id":"1",
    "pf":"iap",
    "sig":"d1f0a41272f9b85618361323e1b19cd8cb0213f21b935aeaa39c160892031e97"

#### 2 对参与开平签名的参数按照key=value的格式，并按照参数名ASCII字典序升序排序如下：

    stringA="access_token=ACCESSTOKEN&appid=wx1234567&offer_id=12345678&openid=odkx20ENSNa2w5y3g_qOkOvBNM1g&pf=iap&sig=d1f0a41272f9b85618361323e1b19cd8cb0213f21b935aeaa39c160892031e97&ts=1507530737&zone_id=1"

#### 3 拼接uri、method和session_key：

    stringSignTemp=stringA+"&org_loc=/cgi-bin/midas/getbalance&method=POST&session_key=V7Q38/i2KXaqrQyl2Yx9Hg=="

#### 4 把session_key作为key，使用HMAC-SHA256得到签名。

    mp_sig=hmac_sha256(key,stringSignTemp)
          ="f7fc0198b1bf795892bed804d145206105eb5835d6ac53fd745834b4a1236c78"

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
*   [辟谣中心](https://mp.weixin.qq.com/cgi-bin/opshowpage?action=dispelinfo&lang=zh_CN&begin=1&count=9&)
*   [客服中心](http://kf.qq.com/faq/120911VrYVrA1509086vyumm.html)
*   [联系邮箱](mailto:weixinmp@qq.com)
*   Copyright © 2012-<span id="s_copyright_year"></span> Tencent. All Rights Reserved.

</div>

</div>

[](http-signature.html)[](open-data.html)</div>

</div>