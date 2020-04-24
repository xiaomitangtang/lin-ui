---
title: 弧形滚动弹出层 ArcPopup（研发中）
---

# ArcPopup

> Popup弧形滚动弹出层组件。

::: tip
本组件依赖于视图组件中的 `Popup` 组件，请保证组件完整性！
:::

该组件支持<a href="/start/wx.html">wx.lin</a>用法。

## 基础使用

本组件可设置 `show` 属性展示或隐藏组件。

## 最大高度设置

本组件默认最大高度 `600` ，单位为 `rpx` ，可自行更改 `max-height` 属性重置最大高度， `scroll` 为 `true` 内容超出高度会自动纵向滚动。  
本组件滚动依赖于微信原生 `scroll-view` 组件，并提供其部分属性与方法，详细请看下文。

## 组件顶部弧度

本组件顶部默认弧度为 `12` ，单位为 `rpx` ，可自行设置 `border-radius` 属性进行更改。  
本组件当 `content-align` 为 `top` 时，属性值为 `12` ，为 `bottom` 时，属性值为 `8`。

## 遮罩层区域透明度设置

本组件默认透明度为 `0.8` ，最大值为 `1` ，可自行设置 `opacity` 属性进行更改。

## 从上/下弹出

本组件默认从下至上弹出，通过设置 `content-align` 属性的值来控制从不同的方向进入屏幕，可选值为 `top` 、`bottom`。

## 组件属性

| 参数 | 说明 | 类型 | 可选值 | 默认值 |  
|:----|:----|:----|:----|:----|
| show	| 设置组件展示隐藏	| Boolean | - | false |
| max-height	| 设置组件最大高度，单位为 `rpx`	| Number | - | 600 |
| border-radius	| 组件弧度，单位为 `rpx`	| Number | - | 12 |
| scroll	| 设置是否滚动	| Boolean | - | true |
| z-index	| 设置组件的页面层级		| Number | - | 777 |
| locked   | 弹出层是否设定为锁定态 | Boolean | - | false |
| animation | 控制弹出层有无动画 | Boolean |  -  | true  | 
| opacity	| 设置组件遮罩层区域透明度	| Number | 0-1 | 0.8 |
| content-align | 控制弹出层内容区域的位置 | String |  top/bottom  | bottom  | 

::: tip 注意事项
  `border-radius` 当 `content-align` 为 `top` 时，属性值为 `12` ，为 `bottom` 时，属性值为 `8`。  
  `z-index` `locked` `animation` 属性继承与 `Popup` 组件内属性，与 `Popup` 属性功能相同。
:::

## 组件外部样式类
| 外部样式类名 | 说明 | 备注 |
| :--------- | :----------------- | :----- |
| l-class   | 覆盖背景区域（内容部分除外）的自定义外部样式类   |  ---   | 


::: tip 注意事项
 `l-class` 样式类继承于 `Popup` ，与 `Popup` 样式类功能相同。
:::

## 组件事件

| 事件名称 | 说明 | 返回值	 | 备注 |
|:----|:----|:----|:----|:----|
| bind:linshow	| 组件展示后触发（ `show` 属性为 `true` 时）	| - | - | 
| bind:linclose	| 组件关闭后触发（ `show` 属性为 `false` 时）	| - | - | 

<RightMenu />


