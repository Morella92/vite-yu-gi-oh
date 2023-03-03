<script>
    export default {
        props:{
            card:{
                type: Object,
                required: true
            }
        }
    }
</script>

<template>
    <li class="col-style">
        <img class="card-image" :src="card.card_images[0].image_url" alt="">
        <h3 class="card-title">{{ card.name }}</h3>
        <p class="card-description">{{ card.archetype }}</p>
    </li>
                   
</template>

<style lang="scss" scoped>
    .col-style{
        background-color: yellow;
        border: 2px solid black;
    }

    .card-title{
        text-align: center;
        font-size: 20px;
        padding: 10px;
    }

    .card-description{
        text-align: center;
        font-style: italic;
        font-size: 20px;
        padding: 10px;
    }
</style>