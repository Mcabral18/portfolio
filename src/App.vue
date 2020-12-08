<template>
  <div id="app">
    <router-view />
    <preloader />
    <nav-bar />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Preloader from "./components/Preloader.vue";

export default {
  components: {
    NavBar,
    Preloader,
  },
};
</script>

<style lang="scss" src="./styles//style.scss">
</style>
