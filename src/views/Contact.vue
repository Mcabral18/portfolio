<template>
  <footer>
    <section id="contact">
      <div class="container">
        <div class="row">
          <div class="col-12 text-center">
            <h2 class="contact__title">
              Get in
              <span style="color: rgb(109, 123, 162)">Touch</span>
            </h2>
          </div>
          <div class="col-sm-12 text-center">
            <div class="contact_quote">
              <h6>
                If you want to create amazing experience for people –
                <span style="color: #11354c"
                  >you are very welcome to contact me.</span
                >
              </h6>
            </div>
            <div class="contact_headline">
              <p>
                I am available for freelance projects and full-time employment.
              </p>
            </div>
          </div>
          <div class="contact__icons">
            <div class="phone__icon">
              <a target="_blank" href="tel:918388272">
                <i class="fas fa-phone"></i>
              </a>
            </div>
            <div class="email__icon">
              <a target="_blank" href="mailto: cabralovil@gmail.com">
                <i class="far fa-envelope"></i>
              </a>
            </div>
          </div>
        </div>
        <div class="copyright">
          <p>© PORTEFÓLIO | Marco Cabral</p>
        </div>
      </div>
      <!-- backto to top btn with show on scroll using pure code -->
      <button
        class="btn btn-to-top shadow-none"
        @click="scrollTop"
        :class="{ scrolltop: scroll > 1000 }"
        data-aos="fade-left"
        data-aos-anchor="#example-anchor"
        data-aos-offset="500"
        data-aos-duration="800"
      >
        <i class="fa fa-chevron-up"></i>
      </button>
    </section>
  </footer>
</template>

<script>
export default {
  name: "contact",
  data() {
    return {
      scroll: [],
    };
  },
  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  },
  methods: {
    //scroll top method
    scrollTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: "smooth",
      });
    },
    updateScroll() {
      this.scroll = window.scrollY;
    },
  },
};
</script>
