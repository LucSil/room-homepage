<template>
  <section id="first-grid">
    <Hero />
    <Main />
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
