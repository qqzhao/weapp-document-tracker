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

*   [简易教程](../../../)
*   [框架](../../MINA.html)
*   [组件](../../../component/)
*   [API](../../../api/)
*   [工具](../../../devtools/devtools.html)
*   [腾讯云支持](../../../qcloud/qcloud.html)

</div>

<div id="book-search-input" role="search">

<form><label for="search-input" class="search-icon" id="js-search-icon"></label><input type="text" id="search-input" name="search-input" placeholder="搜索"> </form>

</div>

</div>

</div>

<div class="book-summary">

<div class="book-summary-home" id="js-summary-home"><a><span class="icon_home_s icon_dev"></span><span class="s_title_2">开发文档首页</span></a></div>

<nav role="navigation">

*   [目录结构](../../structure.html)
*   [配置](../../config.html)
*   [逻辑层](../../app-service/)
    *   [注册程序](../../app-service/app.html)
    *   [场景值](../../app-service/scene.html)
    *   [注册页面](../../app-service/page.html)
    *   [路由](../../app-service/route.html)
    *   [模块化](../../app-service/module.html)
    *   [API](../../app-service/api.html)
*   [视图层](../)
    *   [WXML](./)
        *   [数据绑定](data.html)
        *   [列表渲染](list.html)
        *   [条件渲染](conditional.html)
        *   [模板](template.html)
        *   [事件](event.html)
        *   [引用](import.html)
    *   [WXS](../wxs/)
        *   [模块](../wxs/01wxs-module.html)
        *   [变量](../wxs/02variate.html)
        *   [注释](../wxs/03annotation.html)
        *   [运算符](../wxs/04operator.html)
        *   [语句](../wxs/05statement.html)
        *   [数据类型](../wxs/06datatype.html)
        *   [基础类库](../wxs/07basiclibrary.html)
    *   [WXSS](../wxss.html)
    *   [组件](../component.html)
*   [自定义组件](../../custom-component/)
    *   [组件模版和样式](../../custom-component/wxml-wxss.html)
    *   [Component构造器](../../custom-component/component.html)
    *   [组件事件](../../custom-component/events.html)
    *   [behaviors](../../custom-component/behaviors.html)
    *   [组件间关系](../../custom-component/relations.html)
    *   [抽象节点](../../custom-component/generics.html)
*   [插件](../../plugin/)
    *   [开发插件](../../plugin/development.html)
    *   [使用插件](../../plugin/using.html)
    *   [插件的限制](../../plugin/api-limit.html)
*   [分包加载](../../subpackages.html)
*   [多线程](../../workers.html)
*   [基础库](../../client-lib.html)
*   [兼容](../../compatibility.html)
*   [运行机制](../../operating-mechanism.html)
*   [性能](../../performance/)
    *   [优化建议](../../performance/tips.html)
    *   [分析工具](../../performance/tools.html)

</nav>

</div>

<div class="book-body">

<div class="body-inner">

<div class="page-wrapper" tabindex="-1" role="main">

<div class="page-inner">

<div id="book-search-results">

<div class="search-noresults">

<section class="normal markdown-section">

# 数据绑定

WXML 中的动态数据均来自对应 Page 的 data。

## 简单绑定

数据绑定使用 Mustache 语法（双大括号）将变量包起来，可以作用于：

### 内容

    <view> {{ message }} </view>

    Page({
      data: {
        message: 'Hello MINA!'
      }
    })

### 组件属性(需要在双引号之内)

    <view id="item-{{id}}"> </view>

    Page({
      data: {
        id: 0
      }
    })

### 控制属性(需要在双引号之内)

    <view wx:if="{{condition}}"> </view>

    Page({
      data: {
        condition: true
      }
    })

### 关键字(需要在双引号之内)

`true`：boolean 类型的 true，代表真值。

`false`： boolean 类型的 false，代表假值。

    <checkbox checked="{{false}}"> </checkbox>

**_特别注意：不要直接写 `checked="false"`，其计算结果是一个字符串，转成 boolean 类型后代表真值。_**

## 运算

可以在 `{{}}` 内进行简单的运算，支持的有如下几种方式：

### 三元运算

    <view hidden="{{flag ? true : false}}"> Hidden </view>

### 算数运算

    <view> {{a + b}} + {{c}} + d </view>

    Page({
      data: {
        a: 1,
        b: 2,
        c: 3
      }
    })

view中的内容为 `3 + 3 + d`。

### 逻辑判断

    <view wx:if="{{length > 5}}"> </view>

### 字符串运算

    <view>{{"hello" + name}}</view>

    Page({
      data:{
        name: 'MINA'
      }
    })

### 数据路径运算

    <view>{{object.key}} {{array[0]}}</view>

    Page({
      data: {
        object: {
          key: 'Hello '
        },
        array: ['MINA']
      }
    })

## 组合

也可以在 Mustache 内直接进行组合，构成新的对象或者数组。

### 数组

    <view wx:for="{{[zero, 1, 2, 3, 4]}}"> {{item}} </view>

    Page({
      data: {
        zero: 0
      }
    })

最终组合成数组`[0, 1, 2, 3, 4]`。

### 对象

    <template is="objectCombine" data="{{for: a, bar: b}}"></template>

    Page({
      data: {
        a: 1,
        b: 2
      }
    })

最终组合成的对象是 `{for: 1, bar: 2}`

也可以用扩展运算符 `...` 来将一个对象展开

    <template is="objectCombine" data="{{...obj1, ...obj2, e: 5}}"></template>

    Page({
      data: {
        obj1: {
          a: 1,
          b: 2
        },
        obj2: {
          c: 3,
          d: 4
        }
      }
    })

最终组合成的对象是 `{a: 1, b: 2, c: 3, d: 4, e: 5}`。

如果对象的 key 和 value 相同，也可以间接地表达。

    <template is="objectCombine" data="{{foo, bar}}"></template>

    Page({
      data: {
        foo: 'my-foo',
        bar: 'my-bar'
      }
    })

最终组合成的对象是 `{foo: 'my-foo', bar:'my-bar'}`。

**注意：**上述方式可以随意组合，但是如有存在变量名相同的情况，后边的会覆盖前面，如：

    <template is="objectCombine" data="{{...obj1, ...obj2, a, c: 6}}"></template>

    Page({
      data: {
        obj1: {
          a: 1,
          b: 2
        },
        obj2: {
          b: 3,
          c: 4
        },
        a: 5
      }
    })

最终组合成的对象是 `{a: 5, b: 3, c: 6}`。

**注意：** 花括号和引号之间如果有空格，将最终被解析成为字符串

    <view wx:for="{{[1,2,3]}} ">
      {{item}}
    </view>

等同于

    <view wx:for="{{[1,2,3] + ' '}}">
      {{item}}
    </view>

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

[](./)[](list.html)</div>

</div>