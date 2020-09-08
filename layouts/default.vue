<template>
  <div>
    <header-bihua/>
    <nuxt />
    <footer-bihua/>
  </div>
</template>

<script>
import HeaderBihua from '~/components/HeaderBihua.vue'
import FooterBihua from '~/components/FooterBihua.vue'

export default {
  components: {
    HeaderBihua,
    FooterBihua
  },
  head () {
    return {
      title: 'Prismic Nuxt.js Multi Page Website',
    }
  },
  // Called before rendering the layout (even for error page)
  async middleware({ store, $prismic }) {
    await store.dispatch('fetchMenu', $prismic)
  }
}
</script>
