<template>
  <div class="home">
    <iframe src="http://www.baidu.com" name="ifrm" id="ifrm" width="100%" height="100%"></iframe>
    <a-button @click="sendNotification">发送系统通知</a-button>
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
    },
    sendNotification () {
      const myNotification = new Notification('标题', {
        body: '通知正文内容'
      })
      myNotification.onclick = () => {
        console.log('通知被点击')
      }
    }
  }
}
</script>
