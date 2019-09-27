<template>
  <div>
    <useLoginLayout>
      <!-- header contents -->
      <template v-slot:burger>
        <burger />
      </template>
      <template v-slot:brand>
        <brand />
      </template>
      <template v-slot:glovalMenu>
        <glovalMenu />
      </template>
      <template v-slot:loginMenu>
        <loginMenu />
      </template>
      <template v-slot:mobileMenu>
        <mobileMenu />
      </template>

      <!-- main contents default-->
      <p>discription</p>
      <h3>baseLayout - settinglayout - useLoginLayout - loginLayout</h3>
      <h1>w-works</h1>
      <h2>w-works</h2>
      <h3>w-works</h3>
      <h4>w-works</h4>
      <h5>w-works</h5>
      <h6>w-works</h6>
      <p>h-works</p>
      <!-- <nuxt /> -->
      <!-- footer contents -->
      <template v-slot:copylight>
        <copylight />
      </template>
      <template v-slot:sns>
        <sns />
      </template>

      <!-- aside contents -->
    </useLoginLayout>
  </div>
</template>
<script>
import useLoginLayout from '~/layouts/useLoginLayout.vue'
import brand from '~/components/header/brand.vue'
import burger from '~/components/header/burger.vue'
import glovalMenu from '~/components/header/glovalMenu.vue'
import loginMenu from '~/components/header/loginMenu.vue'
import mobileMenu from '~/components/header/mobileMenu.vue'
import copylight from '~/components/footer/copylight.vue'
import sns from '~/components/footer/sns.vue'
export default {
  components: {
    useLoginLayout,
    brand,
    burger,
    glovalMenu,
    loginMenu,
    mobileMenu,
    copylight,
    sns
  }
}
</script>
