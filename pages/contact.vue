<template>
  <section>
    <p>This is the home page</p>
  </section>
</template>

<script>
export default {
  name: 'Home',
  head () {
    return {
      title: 'Studio Bihua | Contact',
    }
  }/* ,
  async asyncData({ $prismic, error }) {
    try{
      // Query to get the home page content
      const homepage = (await $prismic.api.getSingle('homepage')).data

      return {
        // Page content
        banner: homepage.homepage_banner[0],
        // Set slices as variable
        slices: homepage.page_content
      }
    } catch (e) {
      error({ statusCode: 404, message: 'Page not found' })
    }
  }, */
}
</script>
