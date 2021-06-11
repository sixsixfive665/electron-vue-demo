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
    // document.getElementById('yourPage').innerHTML= "<object type='text/html' data='https://192.168.100.20:8080/river/admin/BeamShow/index' width='100%' height='100%'></object>"
    document.getElementById('yourPage').innerHTML= "<object type='text/html' data='https://bbs.csdn.net/topics/390113679' width='100%' height='100%'></object>"
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
