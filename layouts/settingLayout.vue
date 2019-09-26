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

      <!-- main contents default-->
      <p>discription</p>
      <h3>baseLayout - settinglayout - useLoginLayout - loginLayout</h3>
      <!-- <nuxt /> -->
      <!-- footer contents -->
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
export default {
  components: {
    useLoginLayout,
    brand,
    burger,
    glovalMenu,
    loginMenu
  }
}
</script>
