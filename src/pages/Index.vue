<template>
  <Layout>
    <span id="top"></span>
    <Banner/>
    <AboutSection/>
    <ContactCTA/>
    <ServicesSection/>
    <InstagramCTA/>
  </Layout>
</template>

<script>
import Banner from '~/components/Banner.vue'
import AboutSection from '~/components/AboutSection.vue'
import ServicesSection from '~/components/ServicesSection.vue'
import ContactCTA from '~/components/ContactCTA.vue'
import InstagramCTA from '~/components/InstagramCTA.vue'

export default {
  metaInfo: {
    title: 'Shower Doors Plus'
  },
  components: {
    Banner,
    AboutSection,
    ServicesSection,
    ContactCTA,
    InstagramCTA
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
