<template>
  <section>
    <!-- 1st -->
    <picture>
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

    <!-- 2nd -->
    <About />

    <!-- 3rd -->
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
  </section>
</template>

<script>
export default {
  name: "Images",
};
</script>
