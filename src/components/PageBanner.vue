<template>
  <div class="page-banner">
    <h1>{{title}}</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </div>
</template>

<script>
export default {
  name: "PageBanner",
  props: ["title"]
};
</script>

<style scoped>
.page-banner {
  background: grey;
  padding: 4em 1em 2em;
}
</style>