<template>
  <div id="app">
    <ActionBar />
    <router-view/>
  </div>
</template>

<script>
import ActionBar from '@/components/ActionBar'

export default {
  components: {
    ActionBar
  }
}
</script>
<style lang="stylus">
#app
  box-sizing border-box
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  padding-top 35px
</style>
