<template>
  <div class="wrape">
    <div v-if="isLogin" @click="clickLogin()">
      Log out
    </div>
    <div v-else @click="clickLogin()">
      Log in
    </div>
  </div>
</template>
<style scoped lang="scss">
.wrape {
  width: 100%;
  height: 100%;
}
</style>
<script>
export default {
  data() {
    return {
      isLogin: false
    }
  },
  methods: {
    clickLogin() {
      alert(' login button click')
      this.isLogin = !this.isLogin
    }
  }
}
</script>
<style scoped lang="scss">
.wrape div {
  cursor: pointer;
}
</style>
