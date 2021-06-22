<template>
  <div class="action_bar">
      <span class="action_bar_no_drag left_area"></span>
      <div class="action_bar_title">
          <div class="action_bar_no_drag top_area"></div>
          星天海洋
      </div>
      <span class="min_btn" @click="minimize">一</span>
      <span class="min_btn" @click="close">X</span>
  </div>
</template>

<script>
const { ipcRenderer } = require('electron')

export default {
  methods: {
    // 点击最小化按钮调用的方法
    minimize () {
      ipcRenderer.send('minimize')
    },
    // 点击关闭按钮调用的方法
    close () {
      ipcRenderer.send('close')
    }
  }
}
</script>

<style scoped lang="stylus">
.action_bar
 position fixed
 display flex
 width 100%
 top 0
 left 0
 height 35px
 background #665665

.action_bar_no_drag
 -webkit-app-region: no-drag

.left_area
 width 2px
 height 35px

.top_area
 height 2px

.action_bar_title
 -webkit-app-region: drag
 line-height 33px
 flex 1

.min_btn
 width 35px
 height 35px
 line-height 35px
 cursor default
 &:hover
  background #556556

</style>
