<template>
  <button @click="login">一键登录</button>
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
