<template>
  <div>
    <div class="wrape">
      <brand msg="message">
        brand logo
      </brand>
      <burger>burger icon</burger>
      <glovaMenul>glovaMenul</glovaMenul>
      <login>login</login>
    </div>

    <!-- <brand v-slot:brandLogo>
      <span>h-works</span>
    </brand>-->
    <!-- <navbar v-slot:burger>
      <span>burger</span>
    </navbar>
    <navbar v-slot:menu>
      <span>menu</span>
    </navbar>
    <navbar v-slot:login>
      <span>login</span>
    </navbar>-->
    <!-- <navbar v-slot:brand>
      <span>h-works</span>
    </navbar>
    <navbar v-slot:burger>
      <span>burger</span>
    </navbar>
    <navbar v-slot:menu>
      <span>menu</span>
    </navbar>
    <navbar v-slot:login>
      <span>login</span>
    </navbar>-->
    <nuxt />
  </div>
</template>
<script>
import brand from '~/components/header/brand.vue'
import burger from '~/components/header/burger.vue'
import login from '~/components/header/login.vue'
import glovaMenul from '~/components/header/glovaMenul.vue'
// import navbar from '~/components/header/navbar.vue'
export default {
  components: {
    brand,
    burger,
    glovaMenul,
    login
  }
}
</script>
<style scoped lang="scss">
// .brand {
//   color: coral;
// }
</style>
<script>
export default {
  data() {
    return {
      brandLogo: '~assets/img/logo/h-logo.svg'
      //   items: [
      //     {
      //       title: 'Home',
      //       icon: 'home',
      //       to: { name: 'index' }
      //     },
      //     {
      //       title: 'Inspire',
      //       icon: 'lightbulb',
      //       to: { name: 'inspire' }
      //     },
      //     {
      //       title: 'Documentation',
      //       icon: 'file-document-box',
      //       to: { name: 'documentation' }
      //     }
      //   ]
    }
  }
}
</script>
<style scoped lang="scss">
.wrape {
  height: 4rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
}
</style>
