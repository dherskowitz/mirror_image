<template>
  <section class="section">
    <span id="about" class="anchor"></span>
    <div class="container">
      <span class="section__about">
        <h2 class="title section__title">About Us</h2>
        <p
          class="section__content"
        >Mirror image is a 3rd generation father and son business. Since our founding in 1956, we have been been proudly serving the Pennsylvania, New York, and New Jersey areas for any commercial and residential glass and mirror needs.</p>
        <g-image class="section__image" src="~/images/aboutus.jpg" />
      </span>
    </div>
  </section>
</template>

<script>
export default {
  name: "AboutSection"
};
</script>

<style scoped>
.section__title {
  font-size: 3em;
  grid-column: span 2;
  margin: 0;
}
.section__about {
  display: grid;
  align-items: center;
  justify-content: center;
  grid-template-columns: repeat(4, 1fr);
}
.section__content {
  grid-column: 1/4;
  grid-row: 2/4;
  z-index: 2;
  background: rgba(42, 187, 155, 1);
  padding: 0.5em;
  font-size: 1.3em;
}
.section__image {
  grid-column: span 2 / -1;
  grid-row: 1/4;
  width: 100%;
}
.section__about span {
  grid-column: 3 /-1;
  grid-row: 1/4;
}
@media (max-width: 991px) {
  .section__about {
    align-items: flex-end;
  }
  .section__title {
    grid-column: span 4 / -1;
    grid-row: 3 / -1;
    z-index: 2;
    padding: 1em 0;
    text-shadow: 1px 1px 1px #c3c3c3;
  }
  .section__image {
    grid-column: span 3 / -1;
  }
}
@media (max-width: 768px) {
  .section__title {
    grid-row: 2 / -1;
    padding: 0;
  }
}
@media (max-width: 700px) {
  .section__title {
    grid-row: 4 / -1;
  }
  .section__content {
    grid-column: span 4/4;
    grid-row: 3/6;
  }
  .section__about {
    align-items: center;
  }
}
@media (max-width: 480px) {
  .section__image {
    grid-column: span 4 / -1;
    grid-row: 2 / 4;
  }
  .section__content {
    grid-column: span 4/5;
  }
  .section__title {
    grid-row: 2 / -1;
  }
}
</style>
