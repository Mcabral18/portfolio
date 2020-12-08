<template>
  <nav
    class="navbar fixed-top navbar-expand-lg navbar-light"
    :class="{ change_color: scrollPosition > 10 }"
  >
    <div class="container">
      <a class="navbar-brand" href="/">
        <img
          alt="image"
          class="logo-web logo-dark small-logo"
          src="../assets/logotipo.png"
        />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <a v-scroll-to="'#home'">Home</a>
          <a v-scroll-to="'#projects'">Portfolio</a>
          <a v-scroll-to="'#contact'">Contact</a>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      scrollPosition: [],
    };
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll); //change navbar color
  },
  methods: {
    // change nav color
    updateScroll() {
      this.scrollPosition = window.scrollY;
      // console.log(this.scrollPosition);
    },
  },
};
</script>

<style lang="scss" scoped>
.change_color {
  background: linear-gradient(#fff, #f8f9fa);
}
</style>