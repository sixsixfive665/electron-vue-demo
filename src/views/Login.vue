<template>
  <a-button type="primary" @click="login">一键登录</a-button>
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

</style>
