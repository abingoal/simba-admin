<template>
  <div id="app">
    <transition name="component-fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
@import '../element-variables.css';
#app {
  position: absolute;
  top: 0;
  bottom: 0;
  width: 100%;
}

body {
  margin: 0;
  padding: 0;
  font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
  font-size: 14px;
  -webkit-font-smoothing: antialiased;
}

.toolbar {
  padding: 10px 0;
  .el-form-item{
    margin-bottom: 10px;
  }
}

.component-fade-enter-active,
.component-fade-leave-active {
  transition: opacity .3s ease;
}

.component-fade-enter,
.component-fade-leave-to {
  opacity: 0;
}
</style>
