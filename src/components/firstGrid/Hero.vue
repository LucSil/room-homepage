<template>
  <section id="hero" class="relative">
    <!-- Background Image -->
    <picture>
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

    <!-- Image Switch Buttons -->
    <div id="switch">
      <button>
        <ion-icon id="previous" name="chevron-back-sharp"></ion-icon>
      </button>
      <button>
        <ion-icon id="next" name="chevron-forward-sharp"></ion-icon>
      </button>
    </div>

    <!-- NAVBAR -->
    <Navbar />
  </section>
</template>

<script>
import Navbar from "../Navbar.vue";
export default {
  name: "Hero",
  components: { Navbar },
};
</script>
