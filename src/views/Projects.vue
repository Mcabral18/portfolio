<template>
  <section class="project" id="projects">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="project__title mb-5">
            My
            <span style="color: rgb(109, 123, 162)">Portfolio</span>
          </h2>
          <hr class="mb-5" />
        </div>
      </div>
    </div>
    <div class="container portfolio_work pb-5" style="width: 70%">
      <div class="row no-gutters">
        <div class="col-md-12 mt-5">
          <div class="row no-gutters align-items-center">
            <div class="col-md-5 work_one">
              <img src="../assets/olivia.jpg" alt="" />
            </div>
            <div class="col-md-7">
              <div class="text pt-5 pl-0 pl-lg-5 pl-md-4">
                <div class="px-4 px-lg-4">
                  <div class="desc">
                    <h6 class="work_title">Web • Design</h6>
                    <h4 class="work_title_description mb-3">
                      Multimedia Project
                    </h4>
                    <div class="work_description">
                      <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing
                        elit. Sit consequatur tempore dolorum. Necessitatibus
                        incidunt magnam excepturi iste velit numquam, adipisci,
                        quaerat sit beatae totam, dolorem omnis. Aut id est
                        exercitationem!
                      </p>
                      <button
                        @click="redirectToWork()"
                        class="custom-btn btn-3"
                      >
                        <span>View Work</span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="col-md-12">
          <div class="row no-gutters align-items-center">
            <div class="col-md-5 order-md-last img work_two">
              <img src="../assets/planetiers.jpg" alt="" />
            </div>
            <div class="col-md-7">
              <div class="text pt-5 pr-md-5">
                <div class="pb-4 px-4 px-lg-4">
                  <div class="descleft">
                    <h6 class="workleft_title">Web Development</h6>
                    <h4 class="workleft_title_description mb-3">
                      Planetiers World Gathering
                    </h4>
                    <div class="workleft_description">
                      <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing
                        elit. Sit consequatur tempore dolorum. Necessitatibus
                        incidunt magnam excepturi iste velit numquam, adipisci,
                        quaerat sit beatae totam, dolorem omnis. Aut id est
                        exercitationem!
                      </p>
                      <button class="custom-btn btn-3" @click="redirect()">
                        <span>View Work</span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-md-12">
          <div class="row no-gutters align-items-center">
            <div class="col-md-5 work_three">
              <img src="../assets/movie_app.png" alt="" />
            </div>
            <div class="col-md-7">
              <div class="text pt-5 pl-0 pl-lg-5 pl-md-4">
                <div class="pb-4 px-4 px-lg-4">
                  <div class="desc">
                    <h6 class="work_title">Web Development</h6>
                    <h4 class="work_title_description mb-3">Movies App</h4>
                    <div class="work_description">
                      <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing
                        elit. Sit consequatur tempore dolorum. Necessitatibus
                        incidunt magnam excepturi iste velit numquam, adipisci,
                        quaerat sit beatae totam, dolorem omnis. Aut id est
                        exercitationem!
                      </p>
                      <button @click="redirectGit()" class="custom-btn btn-3">
                        <span>View Work</span>
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "projects",
  methods: {
    redirectToWork() {
      this.$router.push({
        path: "/work",
      });
    },
    redirect(
      link = "http://www.planetiersnewgeneration.com/temp/",
      target = "_blank"
    ) {
      window.open(link, target);
    },
    redirectGit(
      link = "https://github.com/Mcabral18/Movie-App",
      target = "_blank"
    ) {
      window.open(link, target);
    },
  },
};
</script>
