<template>
  <section
    v-lazy:background-image="
      require('../../assets/images/test-background-new.jpg')
    "
    class="about"
  >
    <div class="about-content animate__animated animate__slideInRight">
      <div class="about-description">
        <p class="about-desc-text animate__animated animate__slideInDown">
          I'm a software engineer with over 2 years of software development
          experience focused on front-end development.
        </p>
        <p class="about-desc-text animate__animated animate__slideInDown">
          I graduated with a bachelor's degree in Informatics from Bandung
          Institute of Technology.
        </p>
        <a
          href="mailto:cjunho9868@gmail.com"
          class="anchor-btn btn-cv animate__animated animate__fadeInDown"
          >Contact Me</a
        >
      </div>
      <div class="about-links">
        <ul>
          <li
            class="about-link-items animate__animated animate__bounceInDown duration-4"
          >
            <a href="mailto:cjunho9868@gmail.com"
              ><i class="fa fa-envelope"></i
            ></a>
          </li>
          <li
            class="about-link-items animate__animated animate__bounceInDown duration-3"
          >
            <a target="_blank" href="https://linkedin.com/in/junchh"
              ><i class="fab fa-linkedin"></i
            ></a>
          </li>
          <li
            class="about-link-items animate__animated animate__bounceInDown duration-2"
          >
            <a target="_blank" href="https://github.com/junchh"
              ><i class="fab fa-github"></i
            ></a>
          </li>
        </ul>
      </div>
      <div class="coding-illustration">
        <v-lazy-image
          :src="require('../../assets/images/coding-illustration.png')"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans&display=swap");
section.about {
  height: 100vh;
  width: 100vw;
  z-index: 5;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  background-color: #646496;
  background-blend-mode: lighten;
  position: absolute;
  overflow: hidden;

  animation: fadein 0.15s;
  -moz-animation: fadein 0.15s; /* Firefox */
  -webkit-animation: fadein 0.15s; /* Safari and Chrome */
  -o-animation: fadein 0.15s; /* Opera */
}

.about-content {
  width: 1050px;
  height: 100vh;
  background-color: #fff;
  position: absolute;
  right: 0;
}

.about-description {
  width: 850px;
  margin: auto;
  margin-top: 90px;
}

.about-desc-text {
  font-family: "IBM Plex Sans", sans-serif;
  font-size: 3rem;
  line-height: 55px;
  margin-bottom: 60px;
}

.about-links {
  position: absolute;
  left: 0;
  bottom: 0;

  margin-left: 10px;
  margin-bottom: 40px;
}

.duration-1 {
  --animate-duration: 0.9s;
}

.duration-2 {
  --animate-duration: 1.2s;
}

.duration-3 {
  --animate-duration: 1.5s;
}

.duration-4 {
  --animate-duration: 1.8s;
}

.about-link-items {
  font-size: 2.3rem;
  padding: 12.5px;
}

.about-link-items a {
  color: #2e2a2a;
  transition: color 0.1s;
}

.about-link-items a:hover {
  color: #d3d3f5;
}

.coding-illustration {
  position: absolute;
  bottom: 0;
  right: 0;
  margin-right: 80px;
  z-index: -1;
}

.coding-illustration > img {
  width: 350px;
}

.about-box2 {
  position: absolute;
  width: 100px;
  height: 100px;
  background-color: #d3d3f5;
  bottom: 0;
  right: 520px;
}

.about-box1 {
  position: absolute;
  width: 220px;
  height: 220px;
  background-color: #dedeff;
  bottom: 130px;
  right: 520px;
}

.anchor-btn {
  padding: 15px 50px 15px 50px;
  text-align: center;
  cursor: pointer;
}

img[lazy="loaded"] {
  opacity: 0;
  animation-name: fadein;
  animation-duration: 0.7s;
  animation-iteration-count: 1;
  animation-fill-mode: forwards;
  animation-direction: normal;
  animation-timing-function: ease-out;
  @keyframes fadein {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
}

@media screen and (max-width: 1100px) {
  .about-content {
    width: 100%;
  }

  .about-description {
    width: calc(100% - 100px);
  }

  .about-desc-text {
    font-size: 2.5rem;
    margin-bottom: 30px;
  }

  .about-links {
    margin-left: 0;
  }
}

@media screen and (max-width: 700px) {
  .about-desc-text {
    font-size: 2rem;
    line-height: 35px;
  }

  .coding-illustration {
    display: none;
  }
}

@media screen and (max-height: 450px) {
  .coding-illustration {
    display: none;
  }

  .about-description {
    margin-left: 70px;
  }
}
</style>
