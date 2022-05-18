<template>
  <section class="px-10 py-16 lg:py-0">
    <!-- Div containing title and further information -->
    <div class="relative lg:top-[30%]">
      <agile :navButtons="false" ref="carousel">
        <!-- Slide 1 -->
        <div class="mainText">
          <h1>Discover innovative ways to decorate</h1>
          <p>
            We provide unmatched quality, comfort, and style for property owners
            across the country. Our experts combine form and function in
            bringing your vision to life. Create a room in your own style with
            our collection and make your property a reflection of you and what
            you love.
          </p>
        </div>

        <!-- Slide 2 -->
        <div class="mainText">
          <h1>We are available all across the globe</h1>
          <p>
            With stores all over the world, it's easy for you to find furniture
            for your home or place of business. Locally, we're in most major
            cities throughout the country. Find the branch nearest you using our
            store locator. Any questions? Don't hesitate to contact us today.
          </p>
        </div>

        <!-- Slide 3 -->
        <div class="mainText">
          <h1>Manufactured with the best materials</h1>
          <p>
            Our modern furniture store provide a high level of quality. Our
            company has invested in advanced technology to ensure that every
            product is made as perfect and as consistent as possible. With three
            decades of experience in this industry, we understand what customers
            want for their home and office.
          </p>
        </div>
      </agile>
      <div class="flex items-center">
        <span class="text-base tracking-[0.5rem]">SHOP NOW</span>
        <span class="text-3xl text-gray-500 ml-10">&#10230;</span>
      </div>
    </div>

    <!-- Link to "SHOP NOW" -->
  </section>
</template>

<script>
import { VueAgile } from "vue-agile";

export default {
  name: "Main",
  components: { agile: VueAgile },
};
</script>
