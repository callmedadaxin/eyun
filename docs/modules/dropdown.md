# Dropdown

按钮组件, 各类样式可以持续添加

## 基本使用
默认slot为触发区域，名为list的slot为展示的内容区域
``` html
<x-dropdown trigger="click">
  <x-button type="gray">点击触发</x-button>
  <div slot="list" class="dropdown-list">
    这里是dropdown的内容
  </div>
</x-dropdown>
```

## 预览
![](./img/dropdown.png)

## props

prop | value | default| 描述
---  |  ---  |   ---  | ---
trigger | hover\click | hover | 触发展示的方式
delay | Number | 0 | 延时展示时间

