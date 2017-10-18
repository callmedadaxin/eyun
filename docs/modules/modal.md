# Modal
模态框

## 基本使用

``` html
<x-button type="primary" @click.native="showModal = true">点我展示弹窗</x-button>
<x-modal v-model="showModal">
  <h3 slot="header">这是标题</h3>
  <div slot="content">这是内容，可以填充各种内容</div>
</x-modal>
```

![](./img/modal.png)

### 定制底部按钮
```
<x-modal v-model="showModal">
  <h3 slot="header">这是标题</h3>
  <div slot="content">这是内容，可以填充各种内容</div>
  <div slot="footer" class="modal-button-panel">
    <x-button type="primary" class="modal-button">定制按钮</x-button>
  </div>
</x-modal>
```

![](./img/modal-footer.png)

## props

prop | value | default| 描述
---  |  ---  |   ---  | ---
showFooter | Boolean | true | 是否展示footer
single | Boolean | true | 是否为单例模式，单例模式下，只同时展示一个模态框
reset | Boolean | true | 隐藏时是否移除dom
onClose | Function | noop | 关闭时的回调
onOK | Function | noop | 点击确定时的回调
onCancel | Function | noop | 点击取消时的回调
beforeClose | Function | noop | 关闭前的回调，会传入个done的函数，假设不调用就不会关闭


