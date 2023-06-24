<script>
import AppPokemonCard from './AppPokemonCard.vue';
import {store} from '../store.js';

export default {
    components: {
        AppPokemonCard
    },
    data() {
        return{
            store
        }
    },
}
</script>

<template >
    <div class="container d-flex justify-content-center align-items-center mt-4">
        <div class="row pokedex row justify-content-center p-3">
            <div v-for="(pokemon, index) in store.pokemonList" :key="index" class="col-6 col-md-4 col-lg-3">
                <AppPokemonCard :MyPokemon="pokemon" />
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.pokedex{
    overflow: auto;
    background-color: rgb(98, 102, 107);
    border-top: 30px solid #DEDEDE;
    border-bottom: 30px solid #DEDEDE;
    border-left: 20px solid #DEDEDE;
    border-right:20px solid #DEDEDE;
    border-radius: 1rem;
    box-shadow: 10px 10px 20px  rgba(0, 0, 0, 0.575);
}
</style>