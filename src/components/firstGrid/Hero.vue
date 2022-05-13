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
  </section>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {
      menu: false,
    };
  },
  methods: {
    openMenu() {
      if (!this.menu) {
        this.menu = true;
        document.body.classList.add("overflow-y-hidden");
      }
    },
    closeMenu() {
      if (this.menu) {
        this.menu = false;
        document.body.classList.remove("overflow-y-hidden");
      }
    },
  },
};
</script>

<style>
/* Modal Transition */
.modal-enter-from,
.modal-leave-to {
  transform: translateY(-200px);
  opacity: 0;
}
.modal-enter-active {
  transition: all 0.3s ease-in-out;
}
.modal-leave-active {
  transition: all 0.4s ease-in-out;
}

/* Mobile Menu Transition */
.menu-enter-from,
.menu-leave-to {
  transform: translateY(-200px);
  opacity: 0;
}
.menu-enter-active {
  transition: all 0.4s ease-in-out;
}
.menu-leave-active {
  transition: all 0.2s ease-in-out;
}
</style>
