<template>
  <app-header/>
  <router-view/>
  <!-- <app-footer/> -->
</template>

<script>
import AppHeader from '@/components/AppHeader.vue'
// import AppFooter from '@/components/AppFooter.vue'

export default {
  components: {
    AppHeader
    // AppFooter
  },
  data () {
    return {}
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #c2ffeb;
}

body {
  background-color: #141d18;
}

#nav {
  padding: 30px;
  margin-left: auto;
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

.fade-in {
  // overflow: auto;
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
  // padding-left: 50px;
}

.title-projects {
  color: #dadada;
  font-size: 75px;
  text-align: center;
  // padding-left: 50px;
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

.info-1 {
  display: flex;
  justify-content: center;
}

.info-2 {
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
</style>
