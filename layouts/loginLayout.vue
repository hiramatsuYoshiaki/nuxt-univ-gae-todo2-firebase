<template>
  <div>
    <nav v-if="isOpenMobileMenu" class="mobileMenu">
      <div @click="closeMobileMenu()">
        <i class="material-icons">close</i>
      </div>
      <slot name="mobileMenu" />
    </nav>
    <header>
      <slot name="headerBar" />
    </header>
    <main>
      <div class="main-contents">
        <slot />
      </div>
      <!-- <aside>aside</aside>
      <div class="side-main-contents">
        <slot />
      </div>-->
    </main>
    <footer>
      <slot name="footerBar" />
    </footer>
  </div>
</template>
<script>
// import { mapState } from 'vuex'
import { mapState, mapMutations } from 'vuex'
// import loginLayout from '~/layouts/loginLayout.vue'
export default {
  //   components: {
  //     loginLayout
  //   },
  computed: {
    ...mapState('headerBar', ['isOpenMobileMenu'])
  },
  methods: {
    ...mapMutations({ close: 'headerBar/setOpenMobileMenu' }),
    closeMobileMenu() {
      this.close()
    }
  }
}
</script>
<style scoped lang="scss">
header {
  width: 100%;
  height: 4rem;
  color: white;
  background-color: #212121;
}
main {
  width: 100%;
  height: 100%;
  color: black;
  background-color: white;
  overflow: hidden;
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-direction: row;
}
.main-contents {
  margin-top: 10rem;
  width: 100%;
  height: 100%;
  color: black;
  background-color: white;
  overflow: hidden;
}
nav.mobileMenu {
  position: fixed;
  z-index: 1000;
  width: 100vw;
  height: 100vh;
  //   background-color: #212121;
  background-color: green;
  color: #fff;
  overflow: hidden;
}
// aside {
//   width: 20%;
//   height: 100%;
//   color: black;
//   background-color: whitesmoke;
//   overflow: hidden;
// }
// .side-main-contents {
//   width: 80%;
//   height: 100%;
//   color: black;
//   background-color: white;
//   overflow: hidden;
// }

footer {
  width: 100%;
  height: 100%;
  color: white;
  background-color: #212121;
}
</style>
