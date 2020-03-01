<template>
  <footer>
    <div class="social">
      <a
        class="social__icon"
        href="https://www.facebook.com/showerdoorsplus/"
        target="_blank"
        rel="noreferrer"
      >
        <g-image src="~/images/facebook.svg" />
      </a>
      <a
        class="social__icon"
        href="https://www.instagram.com/showerdoorspl.us/"
        target="_blank"
        rel="noreferrer"
      >
        <g-image src="~/images/instagram.svg" />
      </a>
      <a
        class="social__icon"
        href="https://www.yelp.com/biz/mirror-image-philadelphia-4"
        target="_blank"
        rel="noreferrer"
      >
        <g-image src="~/images/yelp.svg" />
      </a>
    </div>
    <div class="contact">
      <g-image src="~/images/contact.jpg" width="500" />
      <div class="contact__links">
        <a href="mailto:showerdoorsplus@gmail.com">showerdoorsplus@gmail.com</a>
        <a href="tel:+1-215-672-8800">215-672-8800</a>
      </div>
    </div>
    <p class="copyright">&copy; Copyright {{currentYear}} MirrorImage / ShowerDoorsPlus.com</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>

<style scoped>
footer {
  margin-top: 3em;
  background: rgba(46, 49, 49, 1);
  color: #fff;
  text-align: center;
  padding: 3em 0 1em;
}
.social {
  margin-bottom: 3em;
}
.social__icon > img {
  width: 5em;
  margin: 0 2em;
}
.contact__links > a {
  color: #fff;
  font-size: 1.5rem;
  display: flex;
  flex-direction: row;
  margin: 1em;
  justify-content: center;
}
.copyright {
  margin: 1em 0 0;
}
@media (max-width: 460px) {
  .social__icon > img {
    width: 4em;
    margin: 0 1em;
  }
  .contact__links > a {
    font-size: 1.25rem;
  }
}
</style>