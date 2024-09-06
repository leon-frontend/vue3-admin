# 01. 切换路由组件时，实现过渡动效

- 文件位置：**`src/layout/Main/index.vue`**

- 参考：https://router.vuejs.org/zh/guide/advanced/transitions.html

```html
<template>
  <!-- 路由组件的出口位置 -->
  <router-view v-slot="{ Component }">
    <!-- 在切换路由组件时, 实现过渡动效 -->
    <transition name="fade">
      <component :is="Component" />
    </transition>
  </router-view>
</template>
<style lang="scss" scoped>
.fade-enter-from { opacity: 0; }
.fade-enter-active { transition: all 0.7s; }
.fade-enter-to { opacity: 1; }
</style>
```



