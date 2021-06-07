<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
  </div>
</template>

<script>
const { ipcRenderer } = require('electron')
export default {
  name: 'Home',
  mounted () {
    this.changeWindowSize()
  },
  methods: {
    changeWindowSize () {
      ipcRenderer.send('changWindowSize')
    }
  }
}
</script>
