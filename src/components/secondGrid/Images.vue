<template>
  <section>
    <!-- 1st -->
    <div>
      <img src="../../assets/images/bg/1.jpg" alt="#" />
    </div>
    <!-- 2nd -->
    <About />

    <!-- 3rd -->
    <div>
      <img src="../../assets/images/bg/2.jpg" alt="#" />
    </div>
  </section>
</template>

<script>
import About from "../secondGrid/About.vue";
export default {
  name: "Images",
  components: { About },
};
</script>
