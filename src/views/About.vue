<template>
  <div class="section_about" id="about">
    <div class="container">
      <div class="row">
        <div
          class="col-md-6"
          data-aos="fade-right"
          data-aos-easing="ease-in-sine"
          data-aos-offset="300"
          data-aos-duration="500"
        >
          <img class="brand" src="@/assets/photo.jpg" alt="brand" />
        </div>
        <div class="col-md-6">
          <div class="panel text-left">
            <h4 class="brand-title">
              <span style="color: #6d7ba2; font-size: 3rem">F</span>ront-end
              <span>D</span>eveloper
            </h4>
            <div class="discription__about">
              <p>
                Communication and multimedia student at the University of Trás
                Os Montes and Alto Douro. I am an ambitious person when it comes
                to the projects in wich i am inserted hardworking and always
                search for the solution for the problems i face.
              </p>
              <p>
                Communicative and always ready to learn and improve the speed
                and efficiency of project resolution.
              </p>
            </div>
            <div class="cv">
              <a class="btn btn-cv" @click="getCurriculum()">Curriculum</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    getCurriculum() {
      // eslint-disable-next-line no-undef
      axios({
        url: "curriculum.pdf",
        method: "GET",
        responseType: "blob",
      }).then((response) => {
        var fileUrl = window.URL.createObjectURL(new Blob([response.data]));
        var fileLink = document.createElement("a");
        fileLink.href = fileUrl;
        fileLink.setAttribute("download", "curriculum.pdf");
        document.body.appendChild(fileLink);
        fileLink.click();
      });
    },
  },
};
</script>