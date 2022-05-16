<template>
  <section id="hero" class="relative">
    <!-- Background Image -->
    <agile :navButtons="false" ref="carousel">
      <!-- White Bg -->
      <picture id="one">
        <source
          media="(min-width:600px)"
          srcset="../../assets/images/bg/white-d.jpg"
        />
        <source
          media="(min-width:310px)"
          srcset="../../assets/images/bg/white-m.jpg"
        />
        <img src="../../assets/images/bg/white-d.jpg" alt="#" />
      </picture>

      <!-- Black Bg -->
      <picture id="two">
        <source
          media="(min-width:600px)"
          srcset="../../assets/images/bg/black-d.jpg"
        />
        <source
          media="(min-width:310px)"
          srcset="../../assets/images/bg/black-m.jpg"
        />
        <img src="../../assets/images/bg/black-d.jpg" alt="#" />
      </picture>

      <!-- Yellow Bg -->
      <picture id="three">
        <source
          media="(min-width:600px)"
          srcset="../../assets/images/bg/yellow-d.jpg"
        />
        <source
          media="(min-width:310px)"
          srcset="../../assets/images/bg/yellow-m.jpg"
        />
        <img src="../../assets/images/bg/yellow-d.jpg" alt="#" />
      </picture>
    </agile>

    <!-- Image Switch Buttons -->
    <div id="switch">
      <button @click="$refs.carousel.goToPrev()">
        <ion-icon id="previous" name="chevron-back-sharp"></ion-icon>
      </button>
      <button @click="$refs.carousel.goToNext()">
        <ion-icon id="next" name="chevron-forward-sharp"></ion-icon>
      </button>
    </div>

    <!-- NAVBAR -->
    <Navbar />
  </section>
</template>

<script>
import Navbar from "../Navbar.vue";
import { VueAgile } from "vue-agile";
export default {
  name: "Hero",
  components: { Navbar, agile: VueAgile },
  data() {
    return {
      val: 1,
    };
  },
  methods: {
    prev() {},
    next() {},
  },
};
</script>
