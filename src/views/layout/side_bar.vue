<template>
  <el-menu
    default-active="2"
    class="el-menu-vertical-demo"
    :collapse="isCollapse"
    @open="handleOpen"
    @close="handleClose"
  >
    <el-sub-menu index="1">
      <template #title>
        <el-icon>
          <location />
        </el-icon>
        <span>111111111111111111111111111</span>
      </template>
      <el-menu-item-group>
        <template #title>
          <span>2222222</span>
        </template>
        <el-menu-item index="1-1">
          333333333
        </el-menu-item>
        <el-menu-item index="1-2">
          item two
        </el-menu-item>
      </el-menu-item-group>
      <el-menu-item-group title="Group Two">
        <el-menu-item index="1-3">
          item three
        </el-menu-item>
      </el-menu-item-group>
      <el-sub-menu index="1-4">
        <template #title>
          <span>item four</span>
        </template>
        <el-menu-item index="1-4-1">
          item one
        </el-menu-item>
      </el-sub-menu>
    </el-sub-menu>
    <el-menu-item index="2">
      <el-icon>
        <icon-menu />
      </el-icon>
      <template #title>
        Navigator Two
      </template>
    </el-menu-item>
    <el-menu-item index="3" disabled>
      <el-icon>
        <document />
      </el-icon>
      <template #title>
        Navigator Three
      </template>
    </el-menu-item>
    <el-menu-item index="4">
      <el-icon>
        <setting />
      </el-icon>
      <template #title>
        测试测试
      </template>
    </el-menu-item>
  </el-menu>
</template>

<script setup lang="ts">
/* eslint-disable no-unused-vars, import/no-extraneous-dependencies */
import {
  Document,
  Menu as IconMenu,
  Location,
  Setting,
} from '@element-plus/icons-vue';
/* eslint-enable */

const isCollapse = ref(false);
const handleOpen = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
const handleClose = (key: string, keyPath: string[]) => {
  console.log(key, keyPath);
};
</script>
