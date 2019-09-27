<template>
  <div class="wrape">
    <ul>
      <!-- <nuxt-link to="/">
          Home
        </nuxt-link>
        <nuxt-link to="/">
          work
        </nuxt-link>
        <nuxt-link to="/">
          about
        </nuxt-link>
        <nuxt-link to="/">
          contact
      </nuxt-link>-->
      <li v-for="(item, key) of items" :key="key">
        <a :href="item.link">
          <!-- {{ item.title }} -->
          <i :class="item.icon" />
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Twitter',
          link: 'https://twitter.com/',
          icon: 'fab fa-twitter'
        },
        {
          title: 'instagram',
          link: 'https://www.instagram.com/',
          icon: 'fab fa-instagram'
        },
        {
          title: 'facebook',
          link: 'https://www.facebook.com/',
          icon: 'fab fa-facebook-square'
        },
        {
          title: 'github',
          link: 'https://github.com/',
          icon: 'fab fa-github-square'
        },
        {
          title: 'youtube',
          link: 'https://www.youtube.com/',
          icon: 'fab fa-youtube'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.wrape {
  width: 100%;
  height: 100%;
}
li {
  display: inline;
  padding: 0 2rem;
}
</style>
