# 已激活和已停用的事件

当组件被激活时，会发出`activated()`事件。 当组件被停用时，会发出`deactivated()`事件。


```html
<template>
  <div class="view-box">
    <div id="toolbar">点击激活组件activated和取消激活deactivated</div>
    <div class="container">
      <vue-drag-resize-rotate :w="200" :h="200" @activated="onActivated" @deactivated="onDeactivated">
        <p v-if="active">这个组件正处于激活状态</p>
      </vue-drag-resize-rotate>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: false
    };
  },
  methods: {
    onActivated() {
      this.active = true;
    },
    onDeactivated() {
      this.active = false;
    }
  }
};
</script>
```
