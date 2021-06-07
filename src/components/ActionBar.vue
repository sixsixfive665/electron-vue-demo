<template>
  <div class="action_bar">
      <div class="action_bar_title">萨达昂贵的风格123qe12阿萨德1</div>
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
 background pink

.action_bar_title
 -webkit-app-region: drag
 flex 1

.min_btn
 width 35px
 height 35px
 line-height 35px
 cursor default
 &:hover
  background blue

</style>
