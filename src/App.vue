<template>
  <div id="app">
    <span>Vue3 + Vite + Elemen-Plus</span>
    <el-button>我是 Element-Plus 的按钮</el-button>
    <el-card>
      {{ message }}
    </el-card>
    <div class="footer"></div>
  </div>
</template>

<script setup lang="ts">
const message = ref<number | string>(1);
console.log(message.value);
</script>

<style lang="scss">
#app {
  .footer {
    width: 100%;
    height: 200px;
    background-color: pink;
  }
}
</style>
