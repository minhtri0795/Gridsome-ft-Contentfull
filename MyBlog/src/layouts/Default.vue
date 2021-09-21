<template>
  <div class="layout">
    <header class="header">
      <div class="logo">
        <g-link to="/">
        <img src="../images/logo.png" alt="">
        </g-link>
      </div>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
        <g-link class="nav__link" to="/blog/">Blog</g-link>
      </nav>
    </header>
    <slot></slot>
    <footer class="footer footer-1">
      <div class="wrapper">
        <div class="footer__container">
          <div class="footer__column">
            <h3 class="footer__title">Product</h3>
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">Icon Design</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Logo Design</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">UI/UX Design</a>
              </li>
            </ul>
          </div>
          <div class="footer__column">
            <h3 class="footer__title">Resource</h3>
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">Blog</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Support</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Newsletter</a>
              </li>
            </ul>
          </div>
          <div class="footer__column">
            <h3 class="footer__title">Community</h3>
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">Twitter</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Instagram</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Slack</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Dribbble</a>
              </li>
            </ul>
          </div>
          <div class="footer__column">
            <h3 class="footer__title">Support</h3>
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">My Acount</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Help & Support</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Contact Us</a>
              </li>
            </ul>
          </div>
          <div class="footer__column">
            <h3 class="footer__title">Company</h3>
            <ul class="footer__list">
              <li class="footer__item">
                <a href="#" class="footer__link">Privacy Policy</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Term of Service</a>
              </li>
              <li class="footer__item">
                <a href="#" class="footer__link">Code of Conduct</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="coppy-right">
          <a href="#">Made Remotely By TanahAir Studio. Copyright 2020</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
*{
  box-sizing: border-box;
}
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}
a{
  display: inline-block;
  color: inherit;
  text-decoration: none;
}
img{
  display: block;
  max-width: 100%;
}
.layout {
  /* max-width: 1200px; */
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
  padding: 0 40px;
}

.logo{
  height: 100%;
}
.logo img{
  width: 20%;
}
.nav__link {
  margin-left: 20px;
  color: rgb(48, 49, 51);
  font-size: 18px;
  font-weight: 500;
  transition: color 0.2s ease;
}
.nav__link:hover{
  color:rgba(48, 49, 51,0.5);
}
footer {
  font-family: "PT Sans", sans-serif;
}
.wrapper {
  max-width: 1200px;
  margin: 0 auto;
}
.footer__container {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: 120px;
}
.footer__container::before {
  position: absolute;
  content: "";
  width: 100%;
  height: 2px;
  background-color: #e5e5e5;
}
.footer__column {
  margin-top: 64px;
}
.footer__title {
  font-weight: bold;
  font-size: 16px;
  line-height: 22px;
  color: #283646;
}
.footer__list {
  margin: 0;
  padding: 0;
  list-style: none;
}
.footer__link {
  display: inline-block;
  font-size: 16px;
  font-weight: 500;
  color: #636d79;
  text-decoration: none;
  margin: 8px 0;
}
.footer__link:hover {
  color: #006cff;
}
.coppy-right {
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 150%;
  color: #636d79;
  padding-bottom: 80px;
  cursor: default;
}

</style>
