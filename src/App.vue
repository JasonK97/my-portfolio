<template>
  <navigation @click="showNav = !showNav"/>
  <div class="slide" :class="{'open':showNav}">
    <div class="top-bar">
      <div class="navigation-icon" v-if="mobileView" @click="showNav = !showNav">
        <img id="hamburger" src="@/assets/menu.png" alt="menu icon" />
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
  color: #c2ffeb;
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
  display: flex;
  justify-content: center;
}

.info-left {
  margin-top: 45px;
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
  .info-right {
    display: flex;
  }
  .info-left {
    display: flex;
  }
}
</style>
