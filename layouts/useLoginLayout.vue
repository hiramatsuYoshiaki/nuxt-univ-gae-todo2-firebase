<template>
  <div>
    <loginLayout>
      <template v-slot:mobileMenu>
        <div class="mobileMenu-wrape">
          <div class="burger">
            <slot name="burger" />
          </div>
          <div class="brand">
            <div>
              <slot name="brand" />
            </div>
          </div>
          <div class="glovalMenu">
            <slot name="glovalMenu" />
          </div>
          <div class="loginMenu">
            <slot name="loginMenu" />
          </div>
        </div>
      </template>

      <template v-slot:headerBar>
        <!-- <div v-if="isOpenMobileMenu" class="mobileMenu">
          <slot name="mobileMenu" />
          <h1>Mobile Menu2</h1>
          <div @click="closeMobileMenu()">
            <i class="material-icons">close</i>
          </div>
        </div>-->
        <div class="header-wrape">
          <div class="burger">
            <slot name="burger" />
          </div>
          <div class="brand">
            <div>
              <slot name="brand" />
            </div>
          </div>
          <div class="glovalMenu">
            <slot name="glovalMenu" />
          </div>
          <div class="loginMenu">
            <slot name="loginMenu" />
          </div>
        </div>
      </template>

      <div class="main-content">
        <slot />
      </div>
      <template v-slot:footerBar>
        <div class="footer-wrape">
          <div class="burger">
            <slot name="burger" />
          </div>
          <div class="brand">
            <div>
              <slot name="brand" />
            </div>
          </div>
          <div class="glovalMenu">
            <slot name="glovalMenu" />
          </div>
          <div class="loginMenu">
            <slot name="loginMenu" />
          </div>
        </div>
      </template>
    </loginLayout>
  </div>
</template>
<script>
import { mapState } from 'vuex'
// import { mapState, mapMutations } from 'vuex'
import loginLayout from '~/layouts/loginLayout.vue'
export default {
  components: {
    loginLayout
  },
  computed: {
    ...mapState('headerBar', ['isOpenMobileMenu'])
  }
  //   methods: {
  //     ...mapMutations({ close: 'headerBar/setOpenMobileMenu' }),
  //     closeMobileMenu() {
  //       this.close()
  //     }
  //   }
}
</script>
<style scoped lang="scss">
.header-wrape {
  position: relative;
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: row;
}
.mobileMenu-wrape {
  position: relative;
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
}
// .mobileMenu {
//   position: fixed;
//   z-index: 1000;
//   width: 100vw;
//   height: 100vh;
//   background-color: #212121;
//   color: #fff;
//   overflow: hidden;
// }
.footer-wrape {
  width: 100%;
  height: 100%;
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
}

// .header {
//   width: 100%;
//   height: 5rem;
//   color: darkgoldenrod;
//   background-color: rgb(122, 122, 122);
// }
// .main-content {
//   width: 100%;
//   height: 10rem;
//   color: darkgoldenrod;
//   background-color: whitesmoke;
// }
// .footer {
//   width: 100%;
//   height: 5rem;
//   color: darkgoldenrod;
//   background-color: rgb(248, 91, 91);
// }
</style>
