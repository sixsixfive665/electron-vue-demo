<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" @click="backLogin">
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
    },
    backLogin () {
      this.$router.push('/login')
    }
  }
}
</script>
