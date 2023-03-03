<script>
     export default {
    data() {
      return {
        title: 'Yu-Gi-Oh Api'
      }
    }
    
  }
</script>

<template>
    <header class="header">
        <div>
            <h1 class="header-title">
                {{ title }}
            </h1>
        </div>
    
    </header>
</template>

<style lang="scss" scoped>
    @use '../style/partials/_variables.sass' as *;
    .header{
        background-color: green;
    }

    .header-title{
        text-align: center;
        font-size: 2rem;
        color: white;
    }
</style>