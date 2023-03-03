<script>
    import store from '../store'
    export default {
        data(){
            return{
                store
            }
        }
    }

</script>

<template>
    <footer class="footer">
        <div class="container">
            <span class="cards-number">
                Numero di carte: {{ store.cards.length }}
            </span>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
    .footer{
        background-color: black;
        position: sticky;
        bottom: 0;
        padding: 20px;
    }

    .cards-number{
        color: white;
        font-size: 20px;
        font-weight: bold;
        font-style: italic;
    }
</style>