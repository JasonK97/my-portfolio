<template>
  <header>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/projects">Projects</router-link> |
      <router-link to="/specialties">Specialties</router-link> |
      <a href="https://discord.gg/ENs9zjrpe2" target="_blank">Join my Discord</a>
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
      <div class="twitter" @mouseover="hoverOverIconTwitter" @mouseleave="endHoverOverIconTwitter">
        <a v-if="hoveringTwitter" href="https://twitter.com/JasonKent_" target="_blank"><img alt="twitter icon" src="@/assets/twitter-hover.png" /></a>
        <a v-else href="https://twitter.com/JasonKent_" target="_blank"><img alt="twitter icon" src="@/assets/twitter.png" /></a>
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
      hoveringTwitter: false,
      showMobileMenu: false
    }
  },
  methods: {
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
    hoverOverIconTwitter () {
      this.hoveringTwitter = true
    },
    endHoverOverIconTwitter () {
      this.hoveringTwitter = false
    }
  }
}
</script>

<style lang="scss"></style>
