<script>
    import axios from 'axios'

    export default {

        data(){
            return{

                cards: [],

            }
        },
        methods: {
            fetchCards(){
                console.log('cards')

                axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
                .then((res)=>{
                    console.log(res)
                    console.log(res.data)
                    console.log(res.data.data)

                    this.cards = res.data.data
                })
            }
        },

        created() {
            
            this.fetchCards()
        },
    }
</script>

<template>
    <main>
        <div>
            <ul>
                <li v-for="card in cards" :key="card.id">
                    <img class="card-image" :src="card.card_images[0].image_url" alt="">
                    <h3>{{ card.name }}</h3>
                    <p>{{ card.archetype }}</p>
                </li>
            </ul>
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../style/partials/_variables.scss' as *;

    .card-image{
        width: 100px;
    }
</style>