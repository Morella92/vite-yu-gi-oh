<script >
  import Header from './components/Header.vue'
  import Main from './components/Main.vue'
  import Footer from './components/Footer.vue'

  export default {

    components:{
      Header,
      Main,
      Footer
    }
  }
</script>

<template>
  <div>
    <Header/>
    <Main/>
    <Footer/>
  </div>
  
</template>

<style lang="scss">
  @use './style/general.scss';
  @use './style/partials/_variables.scss' as *;
  body{
    background-color: green;
  }
</style>
