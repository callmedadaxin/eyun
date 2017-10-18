# Tip

按钮组件, 各类样式可以持续添加

## 基本使用

``` html
Vue.tip('这是一条提示信息')
// 带类型和图标
this.$tip({
  msg: '这是一条提示信息',
  type: 'loading'
})
// 不自动关闭
Vue.tip({
  msg: '这是一条提示信息',
  autoClose: false
})
```

## options

option | value | default| 描述
---  |  ---  |   ---  | ---
msg | String | '' | 提示的内容
type | loading\success\error\fail | - | 各种图标类型
autoClose | Boolean | true | 是否自动关闭



