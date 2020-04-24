---
title: 日历 Calendar（开发中）
---

# <H2Icon /> 日历 Calendar（开发中）

> 用于选择年月日，可自定义需要选择的时间范围。

## 基本用法

日历组件可以通过`show`设置是否显示，可选值为`true/false`，默认为`false`。

### 示例代码

```wxml
<l-calendar show="{{ true }}" />
```

## 自定义颜色

日历组件默认继承`Lin UI`的官方主题色，当然你也可以通过`color`属性来修改为你喜欢的主题色。

### 示例代码

```wxml
<l-calendar show="{{ true }}" color="#f60" />
```

## 是否显示节日

日历组件允许通过设置`showFestival`属性来控制是否显示节日信息，比如元旦，国庆，等等。

### 示例代码

```wxml
<l-calendar show-festival="{{ true }}"  />
```

## 设置日期格式

通过`format`可以日期输出的格式，默认是`yyyy-mm-dd`，通过`bind:linchange`来获取到

:::tip 注意事项
 * `format`可以参见文档下方的`format`列表说明。
 * `bind:linchange`事件的返回内容可以查看文档下方的事件列表。
:::

### 示例代码
```wxml
<l-calendar show="{{ true }}" format="yyyy-mm-dd" />
```

## 设置最小和最大日期间距

通过 `min` 的方式设置所选日期的最小间隔，比如选择了5月1号，这个时候在选择日期范围的时候，如果选择5月2号或者5月3号，就出弹出toast提示日期间隔不能小于3天。<br />
`max`同理，如果你设置为`3`，那么超过所选日期间隔超过3天的话，会弹出提示信息。

### 示例代码

```wxml
<l-calendar show="{{true}}"  min="3" max="7"/>
```

## 自定义起始时间

日历组件的起始时间，默认为当前终端的日期，但是我们也可以通过`date`属性来控制，例如可以传入`date="2019-6-6"`。

:::tip 注意事项
 * `date`里传入的日期格式必须和`format`的规则一样才能生效，如：`date="2019-6-6"`时，format必须是`format="yyyy-m-d"`
:::

### 示例代码

```wxml
<l-calendar date="2019-6-6"  format="yyyy-m-d" />
```

## 日历组件属性（Calendar Attributes）

| 参数   | 说明 | 类型 | 可选值 | 默认值 |  
|:----|:----|:----|:----|:----|
| show | 控制日历组件的显示和隐藏 | Boolean | true/false | false | 
| color | 主题色 | String |  | lin UI主题色 | 
| date | 初始日期 | String |  | 当前日期 | 
| format | 日期规则 | String |  | yyyy-m-d | 
| min | 设置所选日期的最小间隔 | String/Number |  | 1 | 
| max | 设置所选日期的最大间隔 | String/Number |  | - | 
| show-festival | 控制是否显示节日信息 | Boolean | true/false | true | 
| clear  | 每次点击确定后是否会重置日历组件的信息 | Boolean | true/false | true |

## 日历组件属性（Calendar Attributes）

| 格式   | 含义 | 备注 | 举例 |
|:----|:----|:----|:----|
| yyyy | 年 |  | 2019 |
| m | 月 | 不补零 | 1 | 
| mm | 月 | 补零 | 01 | 
| d | 日 | 不补零 | 5 | 
| dd | 日 | 补零 | 05 | 

## 日历组件事件 (Calendar Events）

| 事件名称        | 说明                                              | 返回值          | 备注 |
| :-------------- | :------------------------------------------------ | :-------------- | :--- |
| bind:linchange |   选中的日期触发  | 选中项发生变化时触发 `linchange` 事件，event.detail = { current: [ 选中项的日期 ]} | -    |
| bind:linconfirm | 确定按钮点击时触发  | event.detail = {current: [ 选中项的日期 ], msg: linconfirm: ok } | -    |
| bind:lincancel | 取消按钮点击时触发 | 图片预览触发 `linpreview` 事件，event.detail = { msg: lincancel: ok } | -    |

<RightMenu />
