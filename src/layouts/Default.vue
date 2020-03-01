<template>
  <div class="layout">
    <NavBar/>
    <slot/>
    <Footer/>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    NavBar,
    Footer
  }
}
</script>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.anchor {
    display: block;
    position: relative;
    top: -75px;
    visibility: hidden;
}

.section {
  padding: 1em;
}

.title {
  font-size: 3em;
  text-transform: capitalize;
}

img {
  max-width: 100%;
}

.container {
  max-width: 1500px;
  margin: 0 auto;
}

</style>
