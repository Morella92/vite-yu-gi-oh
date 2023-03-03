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
    @use '../style/partials/_variables.scss' as *;
    .header-title{
        text-align: center;
        font-size: 2rem;
        color: white;
        padding: 20px;
    }
</style>