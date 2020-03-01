<template>
  <section class="section">
    <span id="services" class="anchor"></span>
    <div class="container">
      <h2 class="title">Our Services</h2>
      <div class="services">
        <div class="services__box" v-for="service in services" :key="service.title">
          <div class="services__head">
            <h3 class="services__title">{{service.title}}</h3>
            <p class="services__description">{{service.text}}</p>
          </div>
          <g-image
            class="services__image"
            :src="service.image"
            width="500"
            fit="contain"
            quality="70"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ServicesSection",
  data: function() {
    return {
      services: [
        {
          title: "shower doors",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/showerdoor.jpg"
        },
        {
          title: "glass railings",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/glassrailing.jpg"
        },
        {
          title: "storefronts",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/storefront.jpg"
        },
        {
          title: "glass partitions",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/glasspartition.jpg"
        },
        {
          title: "mirrors & shelves",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/mirrors-shelves.jpg"
        },
        {
          title: "store displays",
          text:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. A alias quo veritatis?",
          image: "/images/glassdisplay.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.services {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(30rem, 1fr));
  grid-gap: 2em;
}
.services__box {
  height: 20em;
  box-shadow: 0 4px 6px 0 #c3c3c3;
  display: flex;
  align-items: center;
  overflow: hidden;
}
.services__head {
  padding: 0 1em;
}
.services__head > h3 {
  margin: 0;
}
.services__title {
  font-size: 2em;
  text-transform: capitalize;
}
.services__description {
  font-size: 1.25em;
}
.services__image {
  width: 50%;
}
@media (max-width: 1030px) {
  .services {
    grid-template-columns: repeat(auto-fill, minmax(30rem, 1fr));
  }
  .services__box {
    align-items: center;
    overflow: hidden;
  }
}

@media (max-width: 768px) {
  .services {
    grid-template-columns: repeat(auto-fill, minmax(15rem, 1fr));
    grid-gap: 2em;
  }
  .services__box {
    height: unset;
    flex-direction: column;
    justify-content: space-between;
  }
  .services__image {
    width: 100%;
  }
}
@media (max-width: 650px) {
  .services {
    grid-template-columns: repeat(auto-fill, minmax(30rem, 1fr));
  }
  .services__box {
    align-items: flex-end;
  }
  .services__image {
    width: 50%;
  }
}
@media (max-width: 530px) {
  .services {
    display: block;
  }
  .services__box {
    align-items: center;
    margin-bottom: 1em;
  }
  .services__image {
    width: 100%;
  }
}
</style>