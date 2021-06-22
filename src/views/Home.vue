<template>
  <div class="home">
    <div id="yourPage"></div>
  </div>
</template>

<script>
const { ipcRenderer } = require('electron')
export default {
  name: 'Home',
  mounted () {
    this.changeWindowSize()
    // document.getElementById('yourPage').innerHTML= "<object type='text/html' data='https://192.168.100.156:8443/river/admin/BeamShow/exist_main' width='100%' height='100%'></object>"
    document.getElementById('yourPage').innerHTML= "<object type='text/html' data='https://www.jianshu.com/p/a651251b5ad5' width='100%' height='100%'></object>"
  },
  methods: {
    changeWindowSize () {
      ipcRenderer.send('maximize')
    }
  }
}
</script>

<style lang="stylus" scoped>
.home
 height 100%

#yourPage
 height 100%
</style>
