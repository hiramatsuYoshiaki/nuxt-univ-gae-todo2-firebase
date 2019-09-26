<template>
  <div>
    <baseLayout>
      <template v-slot:headerBar>
        header
      </template>
      <div class="main-content">
        <nuxt />
      </div>
      <template v-slot:footerBar>
        footer
      </template>
    </baseLayout>
  </div>
</template>
<script>
import baseLayout from '~/layouts/baseLayout.vue'
export default {
  components: {
    baseLayout
  }
}
</script>
<style scoped lang="scss">
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
