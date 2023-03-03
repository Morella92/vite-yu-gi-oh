<script>
    import axios from 'axios'
    import Card from './Card.vue'
    import store from '../store'

    export default {
        components:{
            Card
        },

        data(){
            return{

                cards: [],
                store
            }
        },
        methods: {
            fetchCards(){
                console.log('cards')

                axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
                .then((res)=>{
                    console.log(res)
                    console.log(res.data)
                    console.log(res.data.data)

                    this.store.cards = res.data.data
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
        <div class="container">
            <div class="card-wrapper">
                <h2 class="wrapper-title">Card collection</h2>
                <ul class="grid">
                    <Card v-for="element in store.cards" :key="element.id" :card="element">
                    </Card>
                </ul>
            </div>
           
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../style/partials/_variables.scss' as *;

    .card-wrapper{
        margin-top: 30px;
        margin-bottom: 30px;
        border: 4px solid black;
    }

    .wrapper-title{
        padding: 20px;
        margin-bottom: 20px;
        background-color: black;
        color: white;
        text-transform: uppercase;
    }
    .grid{
        display: grid;
        grid-template-columns: repeat(5,1fr);
        gap: 30px;
    }
    .card-image{
        width: 150px;
    }
</style>