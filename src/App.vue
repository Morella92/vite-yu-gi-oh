<script >
  import Header from './components/Header.vue'
  import Main from './components/Main.vue'

  export default {

    components:{
      Header,
      Main
    }
  }
</script>

<template>
  <div>
    <Header/>
    <Main/>
  </div>
  
</template>

<style lang="scss">
  @use './style/general.scss';
  @use './style/partials/_variables.scss' as *;
</style>
