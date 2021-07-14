<template>
  <header>
    <div id="mobileNav">
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/projects">Projects</router-link></li>
        <li><router-link to="/specialties">Specialties</router-link></li>
        <div class="social-media">
          <ul>
            <li><a href="https://github.com/JasonK97" target="_blank"><i class="fab fa-github"></i></a></li>
            <li><a href="https://www.linkedin.com/in/jasonbkent/" target="_blank"><i class="fab fa-linkedin"></i></a></li>
            <li><a href="https://twitter.com/JasonKent_" target="_blank"><i class="fab fa-twitter"></i></a></li>
            <li><a href="https://discord.gg/ENs9zjrpe2" target="_blank"><i class="fab fa-discord"></i></a></li>
          </ul>
        </div>
      </ul>
    </div>
    <!-- <div class="social-media">
      <a href="https://github.com/JasonK97" target="_blank"><i class="fab fa-github"></i></a>
      <a href="https://www.linkedin.com/in/jasonbkent/" target="_blank"><i class="fab fa-linkedin"></i></a>
      <a href="https://twitter.com/JasonKent_" target="_blank"><i class="fab fa-twitter"></i></a>
      <a href="https://discord.gg/ENs9zjrpe2" target="_blank"><i class="fab fa-discord"></i></a>
    </div> -->
  </header>
</template>

<style lang="scss">
#mobileNav {
  padding: 10px 0 0 0;
  ul {
    list-style: none;
    width: 200px;
    padding-left: 0px;
    li {
      font-size: 2rem;
      margin-bottom: 20px;
      cursor: pointer;
      &:hover {
        color: #111;
      }
    }
  }
  .social-media {
    position: absolute;
    bottom: 40px;
    a {
      margin: 0 20px 0 0;
      color: #fff;
      font-size: 2rem;
    }
  }
}
</style>
