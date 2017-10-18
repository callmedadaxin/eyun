# Message
模态框

## 基本使用
绑定在Vue全局，也可以用this.$method使用
### alert

``` html
// 直接alert
Vue.alert('这是一个提示消息')

// 设置title
Vue.alert({
  msg: '这是一个提示消息',
  title: '提示'
})

// 设置关闭回调
Vue.alert({
  msg: '这是一个提示消息',
}, done => {
  console.log('这是关闭前的回调')
  done()
}).then(r => {
  console.log('这是关闭后的回调')
})

// 自定义按钮
Vue.alert({
  msg: '这是一个提示消息',
  buttons: [{
    type: 'primary',
    content: '按钮内容',
    handler () {
      这是自定义按钮回调
    }
  }]
})
```

### confirm
与alert基本一样，多了个catch用于取消的回调

### showModal
直接将一个modal组件进行展示

```
this.$showModal(ModalComponents, props)
```

## options
alert,confirm的配置

option | value | default| 描述
---  |  ---  |   ---  | ---
msg | String | '' | 显示内容
title | String | '提示' | 模态框标题
buttons | Array | - | 自定义按钮


