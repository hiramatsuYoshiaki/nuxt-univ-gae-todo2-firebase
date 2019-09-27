<template>
  <div class="wrape">
    <div v-if="isLogin" class="hw--btn" @click="clickLogin()">
      Log out
    </div>
    <div v-else class="hw--btn" @click="clickLogin()">
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
      this.isLogin = !this.isLogin
    }
  }
}
</script>
