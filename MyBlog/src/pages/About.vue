<template>
  <Layout>
    <section class="about__section">
      <div class="about-wrapper">
        <div class="about__card">
          <h2 class="about__title">ABOUT</h2>
         <div class="about_-content">
            <div class="col left">
                <h1>We develop digital strategies, products and services.</h1>
            </div>
            <div class="col right">
              <h3><span>Saigon Digital are WordPress web design specialists who deliver fast, flexible, user centric, SEO optimised, secure & scalable digital platforms that empower your business.</span></h3>
            </div>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'About us'
  }
}
</script>
<style>
.about__card {
  background: #006cff;
  color: #fff;
  margin: 60px auto;
  text-align: center;
  padding: 56px 36px;
  border-radius: 12px;
  width: fit-content;
}
.about_-content{
  display: flex;
  justify-content: center;
}
.about__title{
  margin:0;
  font-size: 12px;
  font-weight: 900;
  margin-bottom: 36px;
}
.about_-content .col{
  max-width: 48%;
  flex: 0 0 48%;
  margin: 0 15px;
}
.about_-content .col.left h1{
  margin: 0;
  font-size: 50px;
  font-weight: 700;
  line-height: 55px;
  text-align: right;
}
.about_-content .col.right h3{
  margin: 0;
  font-size: 26px;
  font-weight: 400;
  font-family: serif;
  text-align: left;
}
</style>