<template>
  <section class="lg:grid grid-cols-10">
    <!-- 1st -->
    <div class="col-span-3">
      <img src="../../assets/images/bg/1.jpg" alt="#" />
    </div>

    <!-- 2nd -->
    <About class="col-span-4" />

    <!-- 3rd -->
    <div class="col-span-3">
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
