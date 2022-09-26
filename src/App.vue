<template>
  <Header />
  <Main />
  <Footer />
</template>

<script>
  import Header from './components/Header.vue'
  import Main from './components/Main.vue'
  import Footer from './components/Footer.vue'

  export default {
    name: 'App',
    components: {
      Header,
      Main,
      Footer
    }
  }

</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap');

  #app {
    font-family: 'Lato', sans-serif;
  }

</style>
