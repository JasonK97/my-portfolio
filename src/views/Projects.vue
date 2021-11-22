<template>
  <div class="fade-in">
    <h1 class="title-projects">Learning Experience Projects</h1>
    <div class="mobile-projects" v-if="mobileView">
      <div><hr /><br /><br />
        <a href="https://shop.leisuretimeinc.com/" target="_blank"><img class="chess-logo" alt="Leisure Time Inc. logo" src="@/assets/download.png"/></a>
        <p class="mobile-content">
          Leisure Time Inc. is a company that sells all things relaxing. From Hot Tubs <br />
          to Grills, and Fireplaces to Stoves for heating your home. I am working on the <br />
          new website for Leisure Time Inc. using React.js, GraphQL, Prismic, and Shopify. <br />
        </p><br /><hr /><br />
        <a href="https://www.allucent.io/" target="_blank"><img class="allucent-logo-mobile" alt="allucent logo" src="@/assets/allucent-logo.png"/></a>
        <p class="mobile-content">
          Undergrad 14-week internship with allucent. Web Development in
          Vue.js, Firebase, and Tailwind.css. I helped implement a
          Training page for allucent users to learn how to use their Web
          Application. Also, a dynamic table has been introduced for company
          admins to share training tips during planning sessions.
        </p><br /><hr /><br />
      </div>
      <div>
        <a href="https://www.bulletheads.org" target="_blank"><img class="bullet-heads" alt="Bulletheads clan logo" src="@/assets/bthd-logo.png"/></a>
        <p class="mobile-content">
          The Bulletheads Clan is a Destiny Gaming Community accross all platforms
          including Xbox, PlayStation, and PC. This website I helped build upon
          in Vue.js using a Firebase backend and communication to the Bungie.net
          API for Clan management.
        </p><br /><hr /><br />
      </div>
      <div>
        <a href="https://github.com/JasonK97/milk-toast-man-website" target="_blank"><img class="mtmmusic-logo" alt="milk toast man logo" src="@/assets/mtmmusic-logo.png"/></a>
        <p class="mobile-content">
          This website was built for my brother, a practicing Family Physician in Eastern
          Idaho, who writes and produces music on the side. Using the Vue.js framework and
          some more advanced CSS functions, this website features a music player usable
          throughout the site linked to the milk toast man bandcamp page.
        </p><br /><hr /><br />
      </div>
      <div>
        <a href="https://github.com/JasonK97/Java-App" target="_blank"><img class="nature-calls" alt="Nature Calls logo" src="@/assets/nature-calls.png"/></a>
        <p class="mobile-content">
          Nature Calls is an Android Application built in Java using Android Studio.
          This was a collaborative project with a Firebase backend looking to help
          students on the BYU-Idaho campus rate restrooms so that no one needs
          to use a nasty bathroom while on-campus.
        </p><br /><hr /><br />
      </div>
    </div>
    <!-----------------Desktop View----------------->
    <div class="desktop-projects" v-else>
      <div class="info-left">
        <p class="p-content-right">
          Leisure Time Inc. is a company that sells all things relaxing. From Hot Tubs <br />
          to Grills, and Fireplaces to Stoves for heating your home. I am working on the <br />
          new website for Leisure Time Inc. using React.js, GraphQL, Prismic, and Shopify. <br />
        </p>
        <a href="https://shop.leisuretimeinc.com/" target="_blank"><img class="chess-logo" alt="Leisure Time Inc. logo" src="@/assets/download.png"/></a>
      </div>
      <div class="info-right">
        <a href="https://www.allucent.io/" target="_blank"><img class="allucent-logo" alt="allucent logo" src="@/assets/allucent-logo.png"/></a>
        <p class="p-content-right">
          Undergrad 14-week internship with allucent. Web Development in <br />
          Vue.js, Firebase, and Tailwind.css. I helped implement a <br />
          Training page for allucent users to learn how to use their Web <br />
          Application. Also, a dynamic table has been introduced for company <br />
          admins to share training tips during planning sessions.
        </p>
      </div>
      <div class="info-left">
        <p class="p-content-left">
          The Bulletheads Clan is a Destiny Gaming Community accross all platforms <br />
          including Xbox, PlayStation, and PC. This website I helped build upon <br />
          in Vue.js using a Firebase backend and communication to the Bungie.net <br />
          API for Clan management.
        </p>
        <a href="https://www.bulletheads.org" target="_blank"><img class="bullet-heads" alt="Bulletheads clan logo" src="@/assets/bthd-logo.png"/></a>
      </div>
      <div class="info-right">
        <a href="https://github.com/JasonK97/milk-toast-man-website" target="_blank"><img class="mtmmusic-logo" alt="milk toast man logo" src="@/assets/mtmmusic-logo.png"/></a>
        <p class="p-content-right">
          This website was built for my brother, a practicing Family Physician in Eastern <br />
          Idaho, who writes and produces music on the side. Using the Vue.js framework and <br />
          some more advanced CSS functions, this website features a music player usable <br />
          throughout the site linked to the milk toast man bandcamp page.
        </p>
      </div>
      <div class="info-left">
        <p class="p-content-left">
          Nature Calls is an Android Application built in Java using Android Studio. <br />
          This was a collaborative project with a Firebase backend looking to help <br />
          students on the BYU-Idaho campus rate restrooms so that no one needs <br />
          to use a nasty bathroom while on-campus.
        </p>
        <a href="https://github.com/JasonK97/Java-App" target="_blank"><img class="nature-calls" alt="Nature Calls logo" src="@/assets/nature-calls.png"/></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      mobileView: true
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

<style lang="scss"></style>
