<template>
  <section class="section section--cta">
    <h3 class="section__title">See some of our work on Instagram</h3>
    <a
      class="section__btn"
      href="https://www.instagram.com/showerdoorspl.us/"
      target="_blank"
      rel="noreferrer"
    >check it out!</a>
  </section>
</template>

<script>
export default {
  name: "InstagramCTA"
};
</script>

<style scoped>
.section--cta {
  background: rgba(140, 20, 252, 1);
  padding: 3em;
  margin: 4em 0 0;
  color: #fff;
  text-align: center;
}
.section__title {
  font-size: 2rem;
  text-transform: capitalize;
  margin-top: 0;
  margin-bottom: 2em;
}
.section__btn {
  font-size: 1.25rem;
  text-transform: capitalize;
  text-decoration: none;
  background: #fff;
  padding: 1em 2em;
  box-shadow: 0 4px 6px 0 rgba(46, 49, 49, 1);
}
</style>