<template>
  <section id="home">
    <particles />
    <header class="container">
      <div class="home">
        <div class="container v-home">
          <div class="home__content">
            <h1>
              I´m
              <span style="color: rgb(109 123 162)">Marco</span>
            </h1>
            <vue-typer
              text="Front-end Developer"
              erase-style="clear"
              initial-action="typing"
            ></vue-typer>
            <div class="social__icons">
              <div class="linkdin__icon">
                <a
                  target="_blank"
                  href="https://www.linkedin.com/in/marco-cabral/"
                >
                  <i class="fab fa-linkedin-in"></i>
                </a>
              </div>
              <div class="github__icon">
                <a target="_blank" href="https://github.com/Mcabral18">
                  <i class="fab fa-github"></i>
                </a>
              </div>
              <div class="google__icon">
                <a href="#">
                  <i class="fab fa-google-plus-g"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div class="mouse"></div>
    </header>
    <about />
    <projects />
    <contact />
  </section>
</template>

<script>
import Particles from "../components/Particles.vue";
import About from "./About.vue";
import Contact from "./Contact.vue";
import Projects from "./Projects.vue";
export default {
  name: "Home",
  components: {
    Particles,
    About,
    Contact,
    Projects,
  },
};
</script>
