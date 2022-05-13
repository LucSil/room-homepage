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

    <!-- Navbar and Menu -->
    <div id="hero-items" class="absolute z-10 top-0 w-full">
      <nav class="mt-12">
        <!-- menu open and logo -->
        <div id="mobile-menu" class="flex items-center justify-center">
          <button @click="openMenu" id="hamburger" class="absolute left-0 ml-5">
            <ion-icon name="menu-sharp"></ion-icon>
          </button>
          <div>
            <img src="../../assets/images/svg/logo.svg" alt="menu button" />
          </div>
        </div>
      </nav>

      <!-- Modal Background -->
      <transition name="modal">
        <div v-if="menu" class="fixed inset-0 bg-black opacity-60 z-20"></div>
      </transition>

      <!-- menu close and nav-links -->
      <transition name="menu">
        <div
          v-if="menu"
          id="nav-menu-items"
          class="bg-white absolute z-30 top-0 w-full px-5 flex justify-between items-center py-10"
        >
          <button @click="closeMenu" id="close-menu" class="mr-14">
            <ion-icon name="close"></ion-icon>
          </button>
          <ul id="nav-links" class="flex justify-between items-center w-full">
            <li><a href="#">home</a></li>
            <li><a href="#">shop</a></li>
            <li><a href="#">about</a></li>
            <li><a href="#">contact</a></li>
          </ul>
        </div>
      </transition>
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
