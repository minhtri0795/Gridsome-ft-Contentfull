<template>
  <Layout>
     <section class="section hero__section">
        <div class="hero__container">
          <div class="hero__paragraph">
            <h1 class="hero__title">Programing skills</h1>
            <p class="hero__desc">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
              reprehenderit in voluptate velit esse cillum dolore eu fugiat
              nulla pariatur.
            </p>
            <div class="hero__button-wapper">
              <a href="#" class="button hero__button float-right"
                >GET STARTED</a
              >
            </div>
          </div>
          <div class="hero__image hide-on-mobile">
            <img src="../images/hero-image.svg" alt="hero-image" />
          </div>
        </div>
      </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.hero__section {
  background-color: #fff;
  min-height: 100vh;
}
.hero__section .hero__container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 30px;
}
.hero__section .hero__paragraph {
  width: 35%;
  flex: 0 0 35%;
  margin-top: 30px;
}
.hero__section .hero__paragraph .hero__title {
  font-family: "PT Sans", sans-serif;
  font-size: 60px;
  line-height: 60px;
  margin-bottom: 0;
}
.hero__section .hero__paragraph .hero__desc {
  font-size: 20px;
  text-align: justify;
  margin-top: 30px;
  margin-bottom: 30px;
}
.hero__section .hero__image {
  max-width: 50%;
  flex: 0 0 50%;
}
.hero__section .hero__image img {
  width: 80%;
}
.button {
  font-family: "PT Sans", sans-serif;
  font-size: 20px;
  font-weight: 500;
  text-decoration: none;
  padding: 10px 20px;
  border-radius: 20px;
}
.hero__section .hero__button {
  background-color: #fc63a5;
  color: #fff;
  float: right;
}

.hero__section .hero__button:hover {
  background-color: #fa8ebd;
}
.hero__section .circle__image img {
  position: absolute;
}
.hero__section .circle__image #big-blue {
  bottom: 0;
  left: 0;
  transform: translate(-30%, 70%);
  width: 35%;
}
.hero__section .circle__image #small-blue {
  top: 0;
  right: 0;
  width: 16%;
  transform: translate(40%, -60%);
}
.hero__section .circle__image #big-pink {
  left: 12.5%;
  top: 0;
  width: 12.5%;
  transform: translateY(-60%);
}
.hero__section .circle__image #small-pink {
  left: 37.5%;
  top: 4%;
  width: 3%;
}
@media screen and (max-width: 1024px) {
  .hero__section .hero__container {
    margin-left: 40px;
  }
}
@media screen and (max-width: 767px) {
  .hide-on-mobile {
    display: none;
  }
  .hero__section .hero__container {
    margin: 30px auto 0 auto;
    padding: 0 20px;
  }
  .hero__section .hero__paragraph {
    max-width: 80%;
    flex: 0 0 80%;
  }
  .hero__section .hero__button {
    float: left;
  }
}

</style>
