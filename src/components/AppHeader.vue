<template>
  <header>
    <!-- <div class="me" @mouseover="hoverOverIconMe" @mouseleave="endHoverOverIconMe">
      <a v-if="hoveringMe" href="/"><img alt="Me logo" src="@/assets/me-bg-hover.png" /></a>
      <a v-else href="/"><img alt="Me logo" src="@/assets/me-bg.png" /></a>
    </div> -->
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/projects">Projects</router-link> |
      <router-link to="/specialties">Specialties</router-link> |
      <a href="https://discord.gg/ENs9zjrpe2" target="_blank">Discord</a>
    </div>
    <div id="mobileNav">
      <div class="hamburger" onclick="myFunction(this)" @click="showMenuSelections">
        <div class="bar1"></div>
        <div class="bar2"></div>
        <div class="bar3"></div>
      </div>
      <div class="menuSelections" v-if="showMobileMenu" @click="showMenuSelections">
        <router-link to="/">Home</router-link><br />
        <router-link to="/about">About</router-link><br />
        <router-link to="/projects">Projects</router-link><br />
        <router-link to="/specialties">Specialties</router-link><br />
        <a href="https://discord.gg/ENs9zjrpe2" target="_blank">Discord</a>
      </div>
    </div>
    <div class="icons">
      <div class="github" @mouseover="hoverOverIconGithub" @mouseleave="endHoverOverIconGithub">
        <a v-if="hoveringGithub" href="https://github.com/JasonK97" target="_blank"><img alt="Github icon" src="@/assets/github-hover.png" /></a>
        <a v-else href="https://github.com/JasonK97" target="_blank"><img alt="Github icon" src="@/assets/github.png" /></a>
      </div>
      <div class="linkedin" @mouseover="hoverOverIconLinkedin" @mouseleave="endHoverOverIconLinkedin">
        <a v-if="hoveringLinkedin" href="https://www.linkedin.com/in/jasonbkent/" target="_blank"><img alt="linkedin icon" src="@/assets/linkedin-hover.png" /></a>
        <a v-else href="https://www.linkedin.com/in/jasonbkent/" target="_blank"><img alt="linkedin icon" src="@/assets/linkedin.png" /></a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data () {
    return {
      hoveringMe: false,
      hoveringGithub: false,
      hoveringLinkedin: false,
      showMobileMenu: false
    }
  },
  methods: {
    hoverOverIconMe () {
      this.hoveringMe = true
    },
    endHoverOverIconMe () {
      this.hoveringMe = false
    },
    hoverOverIconGithub () {
      this.hoveringGithub = true
    },
    endHoverOverIconGithub () {
      this.hoveringGithub = false
    },
    hoverOverIconLinkedin () {
      this.hoveringLinkedin = true
    },
    endHoverOverIconLinkedin () {
      this.hoveringLinkedin = false
    },
    showMenuSelections () {
      this.showMobileMenu = !this.showMobileMenu
    }
  }
}
</script>

<style lang="scss">
@media only screen and (max-width: 600px) {
  div .icons {
    display: none;
  }

  #nav {
    display: none;
  }

  #mobileNav {
    display: inline-block;
    padding: 30px;
    margin-right: auto;

    a {
      font-weight: bold;
      color: #c2ffeb;
      text-decoration: none;
      font-size: 32px;

      &.router-link-exact-active {
        color:#409e82;
      }
    }
  }

  .hamburger {
    display: inline-block;
  }

  .bar1, .bar2, .bar3 {
    width: 35px;
    height: 5px;
    background-color: rgb(255, 255, 255);
    margin: 6px 0;
    transition: 0.4s;
  }

  // Rotate first bar
  .change .bar1 {
    -webkit-transform: rotate(-45deg) translate(44px, 65px);
    transform: rotate(-45deg) translate(44px, 65px);
    z-index: 3;
  }

  // Fade out the second bar
  .change .bar2 {
    opacity: 0;
    -webkit-transform: translate(50px, -60px);
    transform: translate(77px, 3px);
    z-index: 3;
  }

  // Rotate last bar
  .change .bar3 {
    -webkit-transform: rotate(45deg) translate(50px, -60px);
    transform: rotate(45deg) translate(50px, -60px);
    z-index: 3;
  }

  .menuSelections {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    padding-top: 90px;
    padding-left: 45px;
    line-height: 2;
    text-align: left;
    opacity: 1;
    // pointer-events: none;
    background: rgba(0, 0, 0, .7);
    transition: all ease 1s;
  }

  .menuSelections:target {
    opacity: 1;
    pointer-events: auto;
  }

  .menuSelections {
    // overflow: auto;
    animation: fadeIn linear .5s;
    -webkit-animation: fadeIn linear .5s;
    -moz-animation: fadeIn linear .5s;
    -o-animation: fadeIn linear .5s;
    -ms-animation: fadeIn linear .5s;
  }

  // Fade In
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
}
</style>
