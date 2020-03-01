<template>
  <section class="banner">
    <figure></figure>
    <figure></figure>
    <figure></figure>
    <figure></figure>
    <figure></figure>
    <div class="banner__caption">
      <g-image src="~/images/logo2.gif" width="500" />
      <h1 class="banner__caption__title">QUALITY CUSTOM GLASS AND MIRROR</h1>
      <h2
        class="banner__caption__subtitle"
      >Professional Fabrication And Installation Of Commercial And Residential Glass And Mirror Products</h2>
    </div>
  </section>
</template>

<script>
export default {
  name: "Banner"
};
</script>

<style>
.banner {
  height: 100vh;
  position: relative;
}
.banner__caption {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  position: relative;
}
.banner__caption__title,
.banner__caption__subtitle {
  color: #fff;
  text-shadow: 2px 2px 1px #333;
  text-align: center;
  margin: 0 1em;
}
.banner__caption__title {
  font-size: 2.5em;
}
.banner__caption__subtitle {
  font-size: 1.5em;
}
.banner > figure {
  height: 100vh;
  animation: imageAnimation 25s linear infinite 0s;
  animation-iteration-count: infinite;
  backface-visibility: hidden;
  background-size: cover;
  background-position: center center;
  color: transparent;
  height: 100%;
  left: 0px;
  opacity: 0;
  position: absolute;
  top: 0px;
  width: 100%;
  z-index: 0;
  margin: 0;
}
.banner > figure:nth-child(1) {
  background-image: url("/images/banner/lead-bg.jpg");
}
.banner > figure:nth-child(2) {
  animation-delay: 5s;
  background-image: url("/images/banner/IMG_9776.jpg");
}
.banner > figure:nth-child(3) {
  animation-delay: 10s;
  background-image: url("/images/banner/IMG_9428.jpg");
}
.banner > figure:nth-child(4) {
  animation-delay: 15s;
  background-image: url("/images/banner/IMG_7157.jpg");
}
.banner > figure:nth-child(5) {
  animation-delay: 20s;
  background-image: url("/images/banner/IMG_8200.jpg");
}

@keyframes imageAnimation {
  0% {
    animation-timing-function: ease-in;
    opacity: 0;
  }
  8% {
    animation-timing-function: ease-out;
    opacity: 1;
  }
  17% {
    opacity: 1;
  }
  25% {
    opacity: 0;
  }
  100% {
    opacity: 0;
  }
}

@media (max-width: 500px) {
  .banner__caption__title {
    font-size: 2em;
  }
  .banner__caption__subtitle {
    margin-top: 1em;
    font-size: 1.25em;
  }
}
</style>