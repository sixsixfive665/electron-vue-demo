<template>
  <div class="container">
    <a-button type="primary" @click="login">一键登录</a-button>
  </div>
</template>

<script>
export default {
  methods: {
    login () {
      this.$router.push("/home")
    }
  }
}
</script>

<style scoped lang="stylus">
.container
 padding-top 50px
</style>
