<template>
  <header
    class="header"
    v-on:scroll="handleScroll"
    v-bind:class="{ 'header--scrolled' : scrolled }"
  >
    <!-- <strong> -->
    <!-- <g-link to="/">{{ $static.metadata.siteName }}</g-link> -->
    <!-- </strong> -->
    <span class="mobile">
      <span class="mobile__logo">Mirror Image</span>
      <div class="mobile__menuicon" @click="openMenu">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
      </div>
    </span>
    <nav class="nav">
      <!-- <g-link class="nav__link" to="/">Home</g-link> -->
      <a class="nav__link" @click="closeMenu" href="#top">Home</a>
      <a class="nav__link" @click="closeMenu" href="#contact">Get a Quote</a>
      <a class="nav__link" @click="closeMenu" href="#about">Who We Are</a>
      <a class="nav__link" @click="closeMenu" href="#services">What We Do</a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      scrolled: false
    };
  },
  methods: {
    handleScroll: function() {
      let vm = this;
      if (window.scrollY > 50) {
        document.body.classList.add("scrolled");
        vm.scrolled = true;
      } else {
        document.body.classList.remove("scrolled");
        vm.scrolled = false;
      }
    },
    openMenu: function() {
      document.querySelector(".header").classList.toggle("header--open");
      document
        .querySelector(".mobile__menuicon")
        .classList.toggle("mobile__menuicon--open");
    },
    closeMenu: function() {
      if (
        document.querySelector(".header").classList.contains("header--open")
      ) {
        document.querySelector(".header").classList.remove("header--open");
        document
          .querySelector(".mobile__menuicon")
          .classList.remove("mobile__menuicon--open");
      }
    }
  },
  created() {
    if (process.isClient) {
      Window.addEventListener("scroll", this.handleScroll);
    }
  },
  destroyed() {
    if (process.isClient) {
      Window.removeEventListener("scroll", this.handleScroll);
    }
  }
};
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>


<style>
.mobile {
  display: none;
  width: 100%;
  justify-content: space-between;
  align-items: center;
  height: 4em;
  z-index: 9;
  background: #fff;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em;
  height: 50px;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 9;
  display: none;
}

#mobile__menuicon {
  display: inline-block;
  cursor: pointer;
  z-index: 9;
  margin: 1em;
}

.bar1,
.bar2,
.bar3 {
  width: 35px;
  height: 5px;
  background-color: #333;
  margin: 6px 0;
  transition: 0.4s;
}

.mobile__menuicon--open .bar1 {
  -webkit-transform: rotate(-45deg) translate(-9px, 6px);
  transform: rotate(-45deg) translate(-9px, 6px);
}

.mobile__menuicon--open .bar2 {
  opacity: 0;
}

.mobile__menuicon--open .bar3 {
  -webkit-transform: rotate(45deg) translate(-8px, -8px);
  transform: rotate(45deg) translate(-8px, -8px);
}

.header--scrolled {
  display: flex;
  background: #fff;
  box-shadow: 0 4px 6px #c3c3c3;
}

.nav {
  margin-right: 3em;
  display: flex;
  width: 100%;
  justify-content: space-around;
}

.nav__link {
  text-decoration: none;
  font-size: 1.5rem;
}
@media (max-width: 661px) {
  .header {
    padding: 0;
  }
  .nav {
    margin-right: 0;
    justify-content: space-evenly;
  }
  .nav__link {
    font-size: 1rem;
  }
}
@media (max-width: 440px) {
  .header--scrolled {
    flex-direction: column;
  }
  .mobile {
    display: flex;
  }
  .nav {
    flex-direction: column;
    height: 0;
    transform: translateY(-100vh);
    transition: all 0.5s ease;
    position: absolute;
    top: 3em;
    background: #fff;
    padding: 2em;
  }

  .nav__link {
    display: block;
    border-bottom: 1px solid;
    border-top: 1px solid;
    padding: 1em;
    margin: 1em;
    text-align: center;
  }

  .mobile__logo,
  .mobile__menuicon {
    padding: 0 1em;
  }
  .header.header--open .nav {
    height: auto;
    transform: translateY(0);
  }
}
</style>