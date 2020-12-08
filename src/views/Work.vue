<template>
  <section>
    <div id="main"></div>
    <div class="container work_portfolio">
      <div class="work_image">
        <img src="../assets/pic02.jpg" alt />
      </div>
      <div class="container">
        <div class="row">
          <div class="col-md-12 text-center">
            <div class="project_title">
              <h4>Multimedia Project</h4>
              <h5>Vídeo - Design - Web</h5>
            </div>
          </div>
          <div class="project_info">
            <p>
              The Olivia project, was a work developed for the university
              project multimedia chair. This work consisted of including all
              areas of the courses, Design, video / photography, and web
              developement appearing this way the Olivia brand.
            </p>
            <p>
              In this project we create a website, a graphic brand, and
              audiovisual content.
            </p>
          </div>
        </div>
      </div>
      <div class="container photogallery">
        <div class="row">
          <div class="col-md-12">
            <div class="gallery_work text-center">
              <h3>Gallery</h3>
              <hr />
              <h5>Photography</h5>
            </div>
          </div>
          <div class="container photo_gallery">
            <div class="row">
              <div class="col-md-6">
                <div class="gallery_photography">
                  <img src="../assets/photography1.jpg" alt />
                </div>
              </div>
              <div class="col-md-6">
                <div class="gallery_photography">
                  <img src="../assets/photography2.jpg" alt />
                </div>
              </div>
              <div class="col-md-6">
                <div class="gallery_photography">
                  <img src="../assets/photography3.jpg" alt />
                </div>
              </div>
              <div class="col-md-6">
                <div class="gallery_photography">
                  <img src="../assets/photography4.jpg" alt />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-md-6 p-0">
            <div class="logo_project">
              <img src="../assets/logo_olivia.jpg" alt />
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="logo_info">
              <h3>Logo</h3>
              <p>
                The name Olivia came from the Latin olive which translated means
                olive tree, this being the origin of olive oil, after a deeper
                analysis we came to the conclusion of the concept Olivia.
              </p>
              <p>
                In this logo we had to insert the brand mascot, a bird and had
                to represent an olive oil brand, so we decided to use a Latin
                style letter and give the letter O the appearance of an olive.
              </p>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="video_info">
              <h3>Vídeo</h3>
              <p>
                This short video aims to show our customers the entire process
                of making our oil, until it reaches the shelves of commercial
                surfaces.
              </p>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <iframe
              width="100%"
              height="100%"
              src="https://www.youtube.com/embed/jRAeLg0V90U"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            ></iframe>
          </div>
          <div class="col-md-6 p-0">
            <div class="website_link">
              <a href="https://acompanhia.pt/olivia/home/" target="_blank">
                <img src="../assets/wordpresslink.jpg" alt />
              </a>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="website_info">
              <h3>Website</h3>
              <p>
                The olivia brand has an online plateform where our customers can
                view our products and obtain information about our brand such as
                advertising videos and the process of olive oil manufacturing.
              </p>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="book_info">
              <h3>Olívia Book</h3>
              <p>
                This is a small book that aims to show children how the olíve
                oil is created, and explain the process of manufacture in a way
                more educational and easier to understand.
              </p>
            </div>
          </div>
          <div class="col-md-6 p-0">
            <div class="book_link">
              <a @click="onClickpdf()">
                <img src="../assets/book_olivia.jpg" alt />
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="container" style="padding: 2rem">
        <ul style="text-align: center">
          <li>
            <a class="animated-arrow" href="/">
              <span class="the-arrow -left">
                <span class="shaft"></span>
              </span>
              <span class="main">
                <span class="text">Go Back</span>
                <span class="the-arrow -right">
                  <span class="shaft"></span>
                </span>
              </span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "work",
  methods: {
    onClickpdf() {
      // eslint-disable-next-line no-undef
      axios({
        url: "http://localhost:8080/Livro.pdf",
        method: "GET",
        responseType: "blob",
      }).then((response) => {
        var fileUrl = window.URL.createObjectURL(new Blob([response.data]));
        var fileLink = document.createElement("a");
        fileLink.href = fileUrl;
        fileLink.setAttribute("download", "Livro.pdf");
        document.body.appendChild(fileLink);
        fileLink.click();
      });
    },
  },
};
</script>

<style lang="scss">
.navbar {
  display: none;
}
</style>