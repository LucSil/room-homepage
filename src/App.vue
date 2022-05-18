<template>
  <section id="first-grid" class="lg:grid grid-cols-5">
    <Hero class="col-start-1 col-end-4" />
    <Main class="col-span-2" />
  </section>
  <Images />
</template>

<script>
import Hero from "./components/firstGrid/Hero.vue";
import Main from "./components/firstGrid/Main.vue";
import Images from "./components/secondGrid/Images.vue";

export default {
  name: "App",
  components: {
    Hero,
    Main,
    Images,
  },
};
</script>

<style></style>
