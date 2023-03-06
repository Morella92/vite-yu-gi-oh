<template>
    <div class="container">
        <input class="input-style" type="text" placeholder="Cerca la tua carta" v-model="store.search"
            @keyup.enter="$emit('searchCard')" @keydown.enter.prevent="$emit('searchArchetype')"> 

    </div>

</template>

<script>
    import store from '../store'

    export default {

        data(){
            return{
                store,

            }
        },
        
    }
</script>

<style lang="scss" scoped>
    .input-style{
        line-height: 40px;
        padding: 0 20px;
        border: 2px solid black;
        margin-top: 25px;
    }
</style>