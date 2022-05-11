<template>
  <section id="first-grid">
    <Hero />
    <Main />
  </section>
</template>

<script>
import Hero from "./components/firstGrid/Hero.vue";
import Main from "./components/firstGrid/Main.vue";

export default {
  name: "App",
  components: {
    Hero,
    Main,
  },
};
</script>

<style></style>
