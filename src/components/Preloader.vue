<template>
  <transition name="fade" mode="out-in">
    <div v-if="show" class="preloader">
      <div id="loader">
        <div class="inner rotate-one"></div>
        <div class="inner rotate-two"></div>
        <div class="inner rotate-three"></div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "preloader",
  data() {
    return {
      show: true,
    };
  },
  mounted() {
    if (this.show) this.showToggle();
  },
  methods: {
    showToggle() {
      setTimeout(() => {
        this.show = false;
      }, 1000);
    },
  },
};
</script>

<style lang="scss" scoped>
.preloader {
  width: 100vw;
  height: 100vh;
  background: rgba(255, 255, 255, 1);
  position: fixed;
  top: 0;
  z-index: 10000;
}
#loader {
  width: 100px;
  height: 80px;
  position: fixed;
  top: 50%;
  left: 50%;
  margin-top: -40px;
  margin-left: -50px;
}
.inner {
  -webkit-animation: rotate 0.8s linear infinite;
  -moz-animation: rotate 0.8s linear infinite;
  animation: rotate 0.8s linear infinite;
  margin-top: 20px;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  position: absolute;
}
.rotate-one {
  left: 50%;
  margin-left: -25px;
  border-top: 2px solid #1c1c1c;
}
.rotate-two {
  top: -10px;
  left: 30px;
  border-left: 2px solid #1c1c1c;
}
.rotate-three {
  top: -10px;
  right: 30px;
  border-right: 2px solid rgba#1c1c1c;
}
@-webkit-keyframes rotate {
  0% {
    -webkit-transform: rotateZ(0deg);
  }
  100% {
    -webkit-transform: rotateZ(360deg);
  }
}
@-moz-keyframes rotate {
  0% {
    -moz-transform: rotateZ(0deg);
  }
  100% {
    -moz-transform: rotateZ(360deg);
  }
}
@keyframes rotate {
  0% {
    transform: rotateZ(0deg);
  }
  100% {
    transform: rotateZ(360deg);
  }
}
</style>