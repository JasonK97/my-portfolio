<template>
  <footer>
    <p>Copyright &copy; {{ year }} </p>
  </footer>
</template>

<script>
export default {
  data () {
    return {
      year: new Date().getFullYear()
    }
  }
}
</script>

<style lang="scss"></style>
