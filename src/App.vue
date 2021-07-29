<template>
  <navigation @click="showNav = !showNav"/>
  <div class="slide" :class="{'open':showNav}">
    <div class="top-bar">
      <div class="navigation-icon" v-if="mobileView" @click="showNav = !showNav">
        <!-- <img id="hamburger" src="@/assets/menu.png" alt="menu icon" /> -->
        <div id="nav-icon3" :class="{'change':showNav}">
          <span></span>
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <app-header v-if="!mobileView"/>
      <router-view/>
    </div>
  </div>
  <!-- <app-footer/> -->
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
// import AppFooter from '@/components/AppFooter.vue'
import Navigation from '@/components/Navigation.vue'

export default {
  components: {
    AppHeader,
    // AppFooter,
    Navigation
  },
  data () {
    return {
      mobileView: true,
      showNav: false
    }
  },
  methods: {
    handleView () {
      this.mobileView = window.innerWidth <= 990
    }
  },
  created () {
    this.handleView()
    window.addEventListener('resize', this.handleView)
  }
}
</script>

<style lang="scss">
@import url("https://use.fontawesome.com/releases/v5.9.0/css/all.css");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #dadada;
}

body {
  background-color: #122b1d;
}

#nav {
  padding: 30px;
  // margin-left: auto;
  margin-right: auto;

  a {
    font-weight: bold;
    // color: #1e2c3a;
    color: #c2ffeb;
    text-decoration: none;

    &.router-link-exact-active {
      color:#409e82;
    }
  }

  a:hover {
    color: #07e6a3;
  }
}

#mobileNav {
  padding: 30px;
  // margin-left: auto;
  margin-right: auto;

  a {
    font-weight: bold;
    // color: #1e2c3a;
    color: #c2ffeb;
    text-decoration: none;

    &.router-link-exact-active {
      color:#409e82;
    }
  }

  a:hover {
    color: #07e6a3;
  }
}

#nav-icon3 {
  width: 60px;
  height: 45px;
  position: relative;
  margin: 25px;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .5s ease-in-out;
  -moz-transition: .5s ease-in-out;
  -o-transition: .5s ease-in-out;
  transition: .5s ease-in-out;
  cursor: pointer;
}

#nav-icon3 span {
  display: block;
  position: absolute;
  height: 9px;
  width: 100%;
  background: #dadada;
  border-radius: 9px;
  opacity: 1;
  left: 0;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: .25s ease-in-out;
  -moz-transition: .25s ease-in-out;
  -o-transition: .25s ease-in-out;
  transition: .25s ease-in-out;
}

#nav-icon3 span:nth-child(1) {
  top: 0px;
}

#nav-icon3 span:nth-child(2),#nav-icon3 span:nth-child(3) {
  top: 18px;
}

#nav-icon3 span:nth-child(4) {
  top: 36px;
}

#nav-icon3.change span:nth-child(1) {
  top: 18px;
  width: 0%;
  left: 50%;
}

#nav-icon3.change span:nth-child(2) {
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -o-transform: rotate(45deg);
  transform: rotate(45deg);
}

#nav-icon3.change span:nth-child(3) {
  -webkit-transform: rotate(-45deg);
  -moz-transform: rotate(-45deg);
  -o-transform: rotate(-45deg);
  transform: rotate(-45deg);
}

#nav-icon3.change span:nth-child(4) {
  top: 18px;
  width: 0%;
  left: 50%;
}

.icons {
  margin-left: auto;
  display: flex;
}

.icons img {
  height: 35px;
  width: 35px;
  padding: 20px;
}

header {
  display: flex;
  padding: .5rem 1rem;

  p {
    margin-left: 1rem;
  }
}

header img {
  height: 75px;
  width: 75px;
}

#navigation-icon {
  padding: 10px 10px 20px;
  // margin-right: auto;
  cursor: pointer;
}

#hamburger {
  padding-left: 20px;
  cursor: pointer;
}

.slide {
  position: absolute;
  top: 0px;
  left: 0px;
  min-height: 100%;
  min-width: 100%;
  background-color: #141d18;
  transition: 1s transform cubic-bezier(0,.12,.14,1);
}

.fade-in {
  text-align: center;
  animation: fadeIn linear 2s;
  -webkit-animation: fadeIn linear 2s;
  -moz-animation: fadeIn linear 2s;
  -o-animation: fadeIn linear 2s;
  -ms-animation: fadeIn linear 2s;
}

@keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-moz-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-webkit-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-o-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

@-ms-keyframes fadeIn {
  0% {opacity:0;}
  100% {opacity:1;}
}

.title {
  color: #dadada;
  font-size: 112px;
  text-align: center;
}

.title-projects {
  color: #dadada;
  font-size: 75px;
  text-align: center;
}

.meLogo {
  height: 400px;
  width: 400px;
}

.mobile-content {
  text-align: center;
  font-weight: bold;
}

.p-content {
  font-weight: bold;
  line-height: 1.6;
}

.p-content-right {
  font-weight: bold;
  line-height: 1.6;
  text-align: left;
  margin-left: 45px;
  margin-top: 55px;
}

.p-content-left {
  font-weight: bold;
  line-height: 1.6;
  text-align: right;
  margin-right: 45px;
  margin-top: 55px;
}

.info-right {
  margin-top: auto;
  margin-bottom: auto;
  display: flex;
  justify-content: center;
}

.info-left {
  margin-top: auto;
  margin-bottom: auto;
  display: flex;
  justify-content: center;
}

.content {
  padding: 15px;
}

.allucent-logo {
  height: 50px;
  width: auto;
  margin-top: 55px;
}

.bullet-heads {
  height: 250px;
  width: auto;
  border-radius: 20px;
}

.mtmmusic-logo {
  height: 250px;
  width: auto;
  border-radius: 300px;
}

.nature-calls {
  height: 300px;
  width: auto;
  border-radius: 20px;
}

.chess-logo {
  height: 150px;
  width: auto;
}

.logos {
  padding: 10px;
  margin-top: 50px;
}

.open {
  transform: translateX(250px);
}

@media (max-width: 990px) {
  #app {
    font-size: 24px;
    p {
      margin-left: 10%;
      margin-right: 10%;
    }
  }

  .allucent-logo-mobile {
    height: 50px;
    width: auto;
  }

  .info-right {
    display: flex;
  }
  .info-left {
    display: flex;
  }
}
</style>
