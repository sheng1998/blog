<template>
  <div class="header-bar">
    <div class="logo-container">
      <img class="logo" src="@/assets/img/logo.png" alt="logo" data-explain="图片来源：https://www.qt86.com/">
    </div>
    <ul class="navbar-header-right flex-vertical-center">
      <li>
        <el-popover :width="300">
          <template #reference>
            关于我
          </template>
          <template #default>
            <ul class="about-me">
              <ol>
                <span class="label">email: </span>
                <strong>zeguwx@163.com</strong>
              </ol>
              <ol>
                <span class="label">QQ-email: </span>
                <strong>2642336565@qq.com</strong>
              </ol>
              <ol>
                <span class="label">QQ: </span>
                <strong>2642336565</strong>
              </ol>
              <ol>
                <div>
                  <span class="label">wechat: </span>
                  <strong>sheng_1998z</strong>
                </div>
                <img class="wechat-QR" src="@/assets/img/wechat-QR-code.jpg" alt="微信二维码">
              </ol>
            </ul>
          </template>
        </el-popover>
      </li>
    </ul>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  height: {
    type: Number,
    default: 62,
  },
});
</script>

<style lang="scss" scoped>
.header-bar {
  width: 100%;
  height: calc(v-bind(height) * 1px);
  padding: 0 30px;
  background-color: pink;
  .logo-container {
    display: inline-block;
    height: 100%;
    padding: 10px 20px;
    .logo {
      height: 100%;
      object-fit: cover;
    }
  }
  .navbar-header-right {
    height: 100%;
    padding: 10px 20px;
    float: right;
    & > li {
      float: left;
      cursor: pointer;
      & + li {
        margin-left: 16px;
      }
    }
  }
}
.about-me {
  font-size: 16px;
  ol {
    line-height: 30px;
  }
  .wechat-QR {
    width: 200px;
    margin-top: 5px;
    height: auto;
    border-radius: 10px;
  }
}
</style>
