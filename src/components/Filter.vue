<template>
    <div class="container">
        <input class="input-style" type="text" placeholder="Cerca la tua carta" v-model="store.search"
            @keyup.enter="$emit('searchCard')"> 

        <select v-model="store.raceOfCard" @change="$emit('selectRace')" class="select-style">
            <option value="">Seleziona il tipo di carta</option>
            <option v-for="race in raceOptions" :value="race" :key="race">
                {{ race }}
            </option>
        
        </select>
    </div>

</template>

<script>
    import store from '../store'

    export default {

        data(){
            return{
                store,

                raceOptions: [
                    'Normal',
                    'Equip',
                    'Continuous',
                    'Quick-Play'
                ]
            }
        },
        
        methods: {

            
        }
    }
</script>

<style lang="scss" scoped>
    .input-style{
        line-height: 40px;
        padding: 0 20px;
        border: 2px solid black;
        margin-top: 25px;
    }

    .select-style{
        padding: 10px 10px;
        line-height: 40px;
        margin-left: 15px;
    }
</style>