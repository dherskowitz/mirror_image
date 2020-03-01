<template>
  <section class="section section--cta">
    <span id="contact" class="anchor"></span>
    <h2 class="section__title">Get a Quote</h2>
    <h3 class="section__subtitle">Call or email now to arrange for a quote.</h3>
    <div class="section__content">
      <span class="section__btn">
        <span>Email</span>
        <a href="mailto:showerdoorsplus@gmail.com">showerdoorsplus@gmail.com</a>
      </span>
      <span class="section__btn">
        <span>Call</span>
        <a href="tel:+1-215-672-8800">215-672-8800</a>
      </span>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactCTA"
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
  text-transform: capitalize;
  font-size: 3em;
  margin: 0;
}
.section__subtitle {
  text-transform: capitalize;
  font-size: 2em;
  margin: 0 0 1em 0;
}
.section__content {
  display: flex;
  justify-content: center;
}
.section__btn {
  margin: 0 2em;
  display: flex;
  flex-direction: column;
  color: #fff;
  font-size: 1.25rem;
}
.section__btn > a {
  color: #fff;
}
@media (max-width: 768px) {
  .section--cta {
    padding: 0.5em;
    margin: 0;
  }
  .section__content {
    flex-direction: column;
  }
  .section__btn {
    margin: 1em;
  }
}
</style>